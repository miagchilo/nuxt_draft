<template>
  <div>
    <div class="flex flex-col items-center justify-center h-screen text-center text-black">
      <span class="text-xl">(OUR AWARDS)</span>
      <h1 class="text-5xl font-light leading-tight">
        NOT FOR OUR EGOS, BUT BECAUSE AWARDS ARE A MEASURE OF CREATIVITY,
        ORIGINALITY AND QUALITY. AIMING FOR AWARDS PUSHES US TO THINK DEEPER, GO
        FURTHER AND HAVE MEANINGFUL CONVERSATIONS ABOUT WHAT CREATIVITY IS.
      </h1>
    </div>
    <div class="relative h-screen imageBoard">
      <img src="assets/img/img1.png" alt="" class="absolute scaleableImg1" /><img
        src="assets/img/img2.png"
        alt=""
        class="absolute scaleableImg2"
      /><img
        src="assets/img/img3.png"
        alt=""
        class="absolute scaleableImg3"
      /><img
        src="assets/img/img4.png"
        alt=""
        class="absolute scaleableImg4"
      /><img src="assets/img/img5.png" alt="" class="absolute scaleableImg5" />
      <div class="cardImage opacity-0 h-screen flex items-center justify-center">WE PLAY TO WIN</div>
    </div>
  </div>
</template>


<script>
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

export default {
  mounted() {
    gsap
      .timeline({
        scrollTrigger: {
          trigger: ".imageBoard",
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
    ".card-center",
    {
      delay: 0.1,
      scale: 5,
    },
    "start"
  )
  .to(
    ".card-center",
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
        ".scaleableImg1",
        {
          scale: 10,
          x: -1500,
        },
        "start"
      )
      .to(
        ".scaleableImg2",
        {
          scale: 10,
          x: -2500,
        },
        "start"
      )
      .to(
        ".scaleableImg3",
        {
          scale: 10,
          x: -2000,
        },
        "start"
      )
      .to(
        ".scaleableImg4",
        {
          scale: 10,
          x: 3000,
        },
        "start"
      )
      .to(
        ".scaleableImg5",
        {
          scale: 10,
          x: 2000,
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
      .to(".scaleableImg", {
        opacity: 0,
      });
  }
}
</script>
<style>
  /** @format */
  .card-center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
  .scaleableImg1 {
    top: 10%;
    left: 9%;
    width: 250px;
  }

  .scaleableImg2 {
    top: 35%;
    left: 30%;
    width: 250px;
  }
  .scaleableImg3 {
    top: 60%;
    left: 15%;
    width: 250px;
  }
  .scaleableImg4 {
    top: 60%;
    left: 70%;
    width: 250px;
  }
  .scaleableImg5 {
    top: 30%;
    left: 55%;
    width: 250px;
  }
  
</style>
