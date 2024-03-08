<template>
  <div id="home">
    <div class="globus">
      <img class="g_item" src="../assets/img/Ellipse 142.svg" alt="" />
      <span class="g_item axis axis1"></span>
      <span class="g_item axis axis2"></span>
      <span class="g_item axis axis3"></span>
      <h3 class="g_item">Styable</h3>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
#home {
  width: 500px;
  height: 500px;
  background-color: #1e1e1e;
}
.globus {
  height: 300px;
  position: relative;
  border: 1px solid red;
  .g_item {
    color: #20ce70;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate3d(-50%, -50%, 0);
  }
  .axis {
    width: 250px;
    height: 250px;
    border: 1px solid #20ce70;
    border-radius: 50%;
  }
  .axis1 {
    transform: translate3d(-50%, -50%, 0) rotateX(65deg) rotateY(55deg);
    animation-name: anim_axis1;
    animation-duration: 3s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
  }
  .axis2 {
    transform: translate3d(-50%, -50%, 0) rotateX(-75deg) rotateY(40deg);
    animation-name: anim_axis2;
    animation-duration: 3s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
  }
  .axis3 {
    transform: translate3d(-50%, -50%, 0) rotateX(75deg) rotateY(165deg) rotateZ(50deg);
    animation-name: anim_axis3;
    animation-duration: 3s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
  }
}
@keyframes anim_axis1 {
  from {
    transform: translate3d(-50%, -50%, 0) rotateX(65deg) rotateY(0deg);
  }
  to {
    transform: translate3d(-50%, -50%, 0) rotateX(65deg) rotateY(360deg);
  }
}
@keyframes anim_axis2 {
  from {
    transform: translate3d(-50%, -50%, 0) rotateX(-75deg) rotateY(0deg);
  }
  to {
    transform: translate3d(-50%, -50%, 0) rotateX(-75deg) rotateY(360deg);
  }
}
@keyframes anim_axis3 {
  from {
    transform: translate3d(-50%, -50%, 0) rotateX(0deg) rotateZ(50deg) rotateY(-165deg);
  }
  to {
    transform: translate3d(-50%, -50%, 0) rotateX(360deg) rotateZ(50deg) rotateY(-165deg);
  }
}
</style>
