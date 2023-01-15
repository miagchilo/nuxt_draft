<template>
  <div>
    <div
      class="flex flex-col items-center justify-center h-screen text-center text-black upper-container"
    >
    
      <h1 class="text-5xl font-light leading-tight">
        NOT FOR OUR EGOS, BUT BECAUSE AWARDS ARE A MEASURE OF CREATIVITY,
        ORIGINALITY AND QUALITY. AIMING FOR AWARDS PUSHES US TO THINK DEEPER, GO
        FURTHER AND HAVE MEANINGFUL CONVERSATIONS ABOUT WHAT CREATIVITY IS.
      </h1>
    </div>
    <div class="relative h-screen ">
      <div
        class="cardImage opacity-0 h-screen flex items-center justify-center"
      >
        WE PLAY TO WIN
      </div>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

export default {
  mounted() {
    gsap
      .timeline({
        scrollTrigger: {
          trigger: ".upper-container",
          pin: true,
          start: "top top",
          end: "+=300%",
          scrub: 1,
        },
        defaults: {
          ease: "none",
        },
      })
      .to(
        ".cardImage",
        {
          delay: 0.1,
          scale: 5,
        },
        "start"
      )
      .to(
        ".cardImage",
        {
          delay: 0.4,
          opacity: 1,
        },
        "start"
      )
      .to(
        document.body,
        {
          delay: 0.3,
          backgroundColor: "#f0f0f0",
        },
        "start"
      )
      .to(
        ".upper-container h1",
        {
          scale: 5,
        },
        "start"
      )
      .to(
        ".upper-container h1",
        {
          opacity: 0,
        },
        "start"
      )
     
      .to(
        ".cardImage",
        {
          delay: 0.1,
          scale: 5,
        },
        "start"
      )
      .to(
        ".cardImage",
        {
          delay: 0.4,
          opacity: 1,
        },
        "start"
      )
      
  },
};
</script>
<style>
/** @format */
.card-center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

</style>
