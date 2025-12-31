<!-- Debeatzgh Universal Embed Launcher -->
<script>
(function(){

/* ================= CONFIG ================= */
const DBZ_HOME = "https://debeatzgh1.github.io/1/";
const BTN_SIZE = 52;
const BTN_COLOR = "#0f2a44";

/* ================= STYLES ================= */
const css = `
#dbz-btn{
  position:fixed;
  right:16px;
  top:50%;
  transform:translateY(-50%);
  width:${BTN_SIZE}px;
  height:${BTN_SIZE}px;
  border-radius:50%;
  background:${BTN_COLOR};
  color:#fff;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:22px;
  cursor:pointer;
  z-index:999999;
  box-shadow:0 12px 30px rgba(0,0,0,.35);
  animation:dbzPulse 1.6s infinite;
}
@keyframes dbzPulse{
  0%,100%{transform:translateY(-50%) scale(1)}
  50%{transform:translateY(-50%) scale(1.08)}
}

#dbz-overlay{
  position:fixed;
  inset:0;
  background:rgba(0,0,0,.72);
  backdrop-filter:blur(6px);
  display:none;
  z-index:999998;
}

#dbz-box{
  position:absolute;
  inset:12px;
  background:#fff;
  border-radius:16px;
  overflow:hidden;
  display:flex;
  flex-direction:column;
}

#dbz-bar{
  background:${BTN_COLOR};
  color:#fff;
  padding:8px 12px;
  display:flex;
  justify-content:space-between;
  align-items:center;
  font-size:14px;
}

#dbz-bar button{
  background:none;
  border:none;
  color:#fff;
  font-size:16px;
  cursor:pointer;
  margin-left:6px;
}
`;
const style = document.createElement("style");
style.innerHTML = css;
document.head.appendChild(style);

/* ================= HTML ================= */
const html = `
<div id="dbz-btn" title="Open Debeatzgh Hub">☰</div>

<div id="dbz-overlay">
  <div id="dbz-box">
    <div id="dbz-bar">
      <div>
        <button id="dbz-back">⟵</button>
        <button id="dbz-forward">⟶</button>
      </div>
      <div>
        <button id="dbz-full">⛶</button>
        <button id="dbz-close">✕</button>
      </div>
    </div>
    <iframe id="dbz-frame" style="flex:1;border:none"></iframe>
  </div>
</div>
`;
document.body.insertAdjacentHTML("beforeend", html);

/* ================= LOGIC ================= */
const btn = document.getElementById("dbz-btn");
const overlay = document.getElementById("dbz-overlay");
const frame = document.getElementById("dbz-frame");
const box = document.getElementById("dbz-box");

btn.onclick = ()=>{
  frame.src = DBZ_HOME;
  overlay.style.display = "block";
};

document.getElementById("dbz-close").onclick = ()=>{
  overlay.style.display = "none";
  frame.src = "";
  if(document.fullscreenElement) document.exitFullscreen();
};

document.getElementById("dbz-back").onclick = ()=>{
  try{frame.contentWindow.history.back()}catch(e){}
};

document.getElementById("dbz-forward").onclick = ()=>{
  try{frame.contentWindow.history.forward()}catch(e){}
};

document.getElementById("dbz-full").onclick = ()=>{
  if(!document.fullscreenElement){
    box.requestFullscreen();
  }else{
    document.exitFullscreen();
  }
};

})();
</script>
<!-- End Debeatzgh Embed -->
