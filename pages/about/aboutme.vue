<template>
  <div class="header-section text-center">
    Scroll down to see some parallax effects
  </div>
  <section class="pSection overflow-y-scroll h-screen">
    <div class="container max-w-screen-xl p-4 mx-auto">
      <div class="pContent bg-green-500 text-white py-4 px-6">
        <p>
          BLAHBLAHBLAHBLAHBLAHBLAHBLAHBLAHBLAH
        </p>
      
      </div>
    </div>
    <img class="pImage" :src="imageUrl" alt="Filler image" />
  </section>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

export default {
  data() {
    return {
      imageUrl: "https://picsum.photos/1200/526?random=1",
      greensockIconUrl:
        "https://s3-us-west-2.amazonaws.com/s.cdpn.io/16327/scroll-trigger-logo-light.svg",
    };
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    gsap.to(".pImage", {
      yPercent: -50,
      ease: "none",
      scrollTrigger: {
        trigger: ".pSection",
        scrub: true,
      },
    });
    gsap.to(".pContent", {
      yPercent: -10,
      ease: "none",
      scrollTrigger: {
        trigger: ".pSection",
        scrub: true,
      },
    });
  },
};
</script>
<style>
.header-section {
  text-align: center;
}
.pSection {
  position: relative;
  overflow-y: auto;
  height: 100vh;
}
.container {
  padding: 1rem;
  margin: 0 auto;
  max-width: 1070px;
  position: relative;
  z-index: 1;
}
.pContent {
  width: 65%;
  position: relative;
  background-color: rgba(238, 0, 255, 0.8);
  color: white;
  padding: 40px 60px;
}
.pImage {
  width: 70%;
  position: relative;
  top: 0;
  right: 0;
  max-height: 900px;
}
</style>
