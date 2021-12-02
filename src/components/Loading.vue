<template>
  <div id="loading">
    <!-- <div class="lds-hourglass"></div> -->
    <div class="loadingio-spinner-interwind-k36yuzsg7r">
      <div class="ldio-ypwhcpp650g">
        <div>
          <div>
            <div><div></div></div>
          </div>
          <div>
            <div><div></div></div>
          </div>
        </div>
      </div>
    </div>
    <p>Cargando proyectos...</p>
  </div>
</template>

<style scoped>
/* .lds-hourglass {
  display: inline-block;
  position: relative;
  width: 80px;
  height: 80px;
}
.lds-hourglass:after {
  content: " ";
  display: block;
  border-radius: 50%;
  width: 0;
  height: 0;
  margin: 8px;
  box-sizing: border-box;
  border: 32px solid #fff;
  border-color: #616161 transparent #616161 transparent;
  animation: lds-hourglass 1.2s infinite;
}
@keyframes lds-hourglass {
  0% {
    transform: rotate(0);
    animation-timing-function: cubic-bezier(0.55, 0.055, 0.675, 0.19);
  }
  50% {
    transform: rotate(900deg);
    animation-timing-function: cubic-bezier(0.215, 0.61, 0.355, 1);
  }
  100% {
    transform: rotate(1800deg);
  }
} */

@keyframes ldio-ypwhcpp650g-r {
  0%,
  100% {
    animation-timing-function: cubic-bezier(0.2 0 0.8 0.8);
  }
  50% {
    animation-timing-function: cubic-bezier(0.2 0.2 0.8 1);
  }
  0% {
    transform: rotate(0deg);
  }
  50% {
    transform: rotate(180deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
@keyframes ldio-ypwhcpp650g-s {
  0%,
  100% {
    animation-timing-function: cubic-bezier(0.2 0 0.8 0.8);
  }
  50% {
    animation-timing-function: cubic-bezier(0.2 0.2 0.8 1);
  }
  0% {
    transform: translate(-30px, -30px) scale(0);
  }
  50% {
    transform: translate(-30px, -30px) scale(1);
  }
  100% {
    transform: translate(-30px, -30px) scale(0);
  }
}
.ldio-ypwhcpp650g > div {
  transform: translate(0px, -15px);
}
.ldio-ypwhcpp650g > div > div {
  animation: ldio-ypwhcpp650g-r 1s linear infinite;
  transform-origin: 100px 100px;
}
.ldio-ypwhcpp650g > div > div > div {
  position: absolute;
  transform: translate(100px, 82px);
}
.ldio-ypwhcpp650g > div > div > div > div {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: #fe718d;
  animation: ldio-ypwhcpp650g-s 1s linear infinite;
}
.ldio-ypwhcpp650g > div > div:last-child {
  animation-delay: -0.5s;
}
.ldio-ypwhcpp650g > div > div:last-child > div > div {
  animation-delay: -0.5s;
  background: #46dff0;
}
.loadingio-spinner-interwind-k36yuzsg7r {
  width: 200px;
  height: 200px;
  display: inline-block;
  overflow: hidden;
  background: #ffffff;
}
.ldio-ypwhcpp650g {
  width: 100%;
  height: 100%;
  position: relative;
  transform: translateZ(0) scale(1);
  backface-visibility: hidden;
  transform-origin: 0 0; /* see note above */
}
.ldio-ypwhcpp650g div {
  box-sizing: content-box;
}
</style>
