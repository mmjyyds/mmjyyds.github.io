<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8" />
<title>18歲確認</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+TC&display=swap');

  html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Noto Sans TC', "Microsoft JhengHei", sans-serif;
  }

  body {
    background: linear-gradient(to bottom, #fff0f6, #ffe6f0);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding-top: 20vh;
    overflow: hidden;
    position: relative;
  }

  #enterBox {
    background-color: #fff200;
    border: 2px solid black;
    padding: 20px 50px;
    font-size: 28px;
    color: black;
    font-weight: bold;
    cursor: pointer;
    border-radius: 10px;
    box-shadow: 0 0 10px #b0a000aa;
    transition: 0.3s;
    user-select: none;
    z-index: 10;
  }

  .message {
    margin-top: 20px;
    font-size: 22px;
    color: #a52a5a;
    text-align: center;
    display: none;
  }

  #girlPhoto {
    margin-top: 15px;
    width: 250px;
    height: auto;
    border-radius: 15px;
    box-shadow: 0 0 15px #ff69b4aa;
    animation: pulseGirl 2s infinite;
  }

  @keyframes pulseGirl {
    0%   { transform: scale(1); }
    50%  { transform: scale(1.1); }
    100% { transform: scale(1); }
  }

  .sakura {
    position: fixed;
    top: -10px;
    width: 20px;
    height: 20px;
    background-image: url('https://cdn-icons-png.flaticon.com/512/616/616408.png');
    background-size: contain;
    background-repeat: no-repeat;
    opacity: 0.8;
    animation-name: fall;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
    pointer-events: none;
  }

  @keyframes fall {
    0% {
      transform: translateY(0) rotate(0deg);
      opacity: 0.8;
    }
    100% {
      transform: translateY(100vh) rotate(360deg);
      opacity: 0;
    }
  }

  #manImage {
    display: none;
    max-width: 90vw;
    max-height: 90vh;
    border-radius: 12px;
    box-shadow: 0 0 20px #333;
    transition: all 0.5s ease;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 50;
  }

  /* 全屏样式 */
  #manImage.fullscreen {
    width: 100vw;
    height: 100vh;
    max-width: none;
    max-height: none;
    border-radius: 0;
    object-fit: contain;
  }

  #finalMsg {
    display: none;
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: #8B0000; /* 深血红 */
    font-size: 72px;
    font-weight: 900;
    font-family: "Microsoft JhengHei", 'Noto Sans TC', sans-serif;
    text-shadow:
      3px 3px 7px black,
      -3px -3px 7px black;
    white-space: nowrap;
    user-select: none;
    z-index: 10001;
    text-align: center;
  }

  /* 血迹背景层 */
  #bloodSplatter {
    display: none;
    position: fixed;
    top: 0; left: 0;
    width: 100vw; height: 100vh;
    background: black;
    z-index: 9999;
  }

  /* 血迹斑点 - 用多个半透明红色斑点模拟血迹泼溅 */
  #bloodSplatter::before {
    content: "";
    position: absolute;
    top: 10%;
    left: 20%;
    width: 150px;
    height: 150px;
    background: radial-gradient(circle, rgba(139,0,0,0.8) 30%, transparent 70%);
    filter: blur(15px);
    transform: rotate(-20deg);
    box-shadow:
      300px 100px 20px 10px rgba(139,0,0,0.6),
      600px 50px 25px 15px rgba(139,0,0,0.7),
      800px 200px 30px 20px rgba(139,0,0,0.5),
      100px 300px 40px 10px rgba(139,0,0,0.7);
  }
</style>
</head>
<body>

  <div id="enterBox">滿18歲進入</div>
  <img id="girlPhoto" src="https://img14.360buyimg.com/pop/jfs/t1/157693/32/47044/57831/66de8349F1b583f8d/ce5435d0958a2ca0.jpg" alt="性感女生" />

  <div id="msg1" class="message">別看了孩子</div>
  <div id="msg2" class="message">在看就完了</div>
  <div id="msg3" class="message">你maozi叔叔就是那么没的</div>

  <img id="manImage" src="https://b0.bdstatic.com/ugc/a9QnRRkMeKvO3x_CXIogKA26715936698549b8f73bcc0ef0bf7b3b.jpg" alt="虛脫男" />

  <div id="bloodSplatter"></div>

  <div id="finalMsg">再看把你唧唧剁咯👿</div>

<script>
  let sakuraInterval;

  function createSakura() {
    const sakura = document.createElement('div');
    sakura.classList.add('sakura');
    sakura.style.left = Math.random() * window.innerWidth + 'px';
    sakura.style.animationDuration = (5 + Math.random() * 5) + 's';
    sakura.style.fontSize = (10 + Math.random() * 20) + 'px';
    sakura.style.opacity = Math.random();
    document.body.appendChild(sakura);
    sakura.addEventListener('animationend', () => sakura.remove());
  }

  sakuraInterval = setInterval(createSakura, 300);

  document.getElementById("enterBox").onclick = function() {
    // 点击按钮后立即隐藏按钮和美女图
    document.getElementById("enterBox").style.display = "none";
    document.getElementById("girlPhoto").style.display = "none";

    // 假装加载2秒（无提示）
    setTimeout(() => {
      // 2秒后显示提示文字（间隔放慢）
      document.getElementById("msg1").style.display = "block";
      setTimeout(() => {
        document.getElementById("msg2").style.display = "block";
      }, 1200);
      setTimeout(() => {
        document.getElementById("msg3").style.display = "block";
      }, 2400);

      clearInterval(sakuraInterval);
      document.querySelectorAll('.sakura').forEach(el => el.remove());

      // 等最后一句显示2秒后才显示虚脱男图片
      setTimeout(() => {
        const manImg = document.getElementById("manImage");
        manImg.style.display = "block";
        manImg.classList.add("fullscreen");

        // 虚脱男图片显示2秒后隐藏图片，显示血迹背景和血红字
        setTimeout(() => {
          manImg.style.display = "none";

          // 黑背景 + 血迹泼溅层显示
          const blood = document.getElementById("bloodSplatter");
          blood.style.display = "block";

          // 血红字体显示
          document.getElementById("finalMsg").style.display = "block";

          // 把body背景改成纯黑色，防止看到渐变
          document.body.style.background = "black";

        }, 2000);

      }, 2400 + 2000); // 最后一句显示时间 + 2秒停留
    }, 2000);
  }
</script>

</body>
</html>
