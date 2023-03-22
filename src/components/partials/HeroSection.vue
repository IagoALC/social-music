<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <q-page class="flex flex-center" id="videoBackground">
        <div :style="$q.screen.lt.lg ? 'width: 90%' : 'width: 60%'" class="text-white text-center">
          <q-card-section class="text-h3 text-weight-bold">Social Music</q-card-section>
          <q-card-section class="text-subtitle1">Log in or Sign up to start the fun</q-card-section>
          <q-card-section class="text-subtitle1">Be one with your music</q-card-section>
          <q-card-actions class="text-white justify-center">
            <q-btn to="login" flat class="bg-green text-weight-medium" style="width: 30%">Login</q-btn>
            <q-btn to="register" flat class="bg-blue text-weight-medium" style="width: 30%">Register</q-btn>
          </q-card-actions>
        </div>
        <div id="videoDarkOverlay"></div>
        <video id="myVideo" autoplay muted>
          <source src="/concert-1630.mp4" type="video/mp4" />
        </video>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
// import { ref } from 'vue'
</script>
<style lang="scss">
 #centerCallToAction {
    width: 100%;
    position: absolute;
    left: 50%;
    top: 50%;
    -webkit-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
  }
  #myVideo {
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    z-index: -2;
  }
  #videoDarkOverlay {
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    z-index: -1;
    background-color: rgba(0,0,0,0.65);
  }

</style>
