<script>
  import Typewriter from "svelte-typewriter";
  import MarqueeTextWidget from "svelte-marquee-text-widget";
  let pauseOnHover = false;
</script>

<div class="mx-auto container">
  <div class="grid sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-2 pb-10">
    <img
      class="place-self-center pb-10 hover:rotate-6 transition active:-rotate-6 lg:hidden"
      src="/base/move-monitor.webp"
      alt=""
    />
    <div class="place-self-center sm:p-5 lg:p-10 xl:p-32">
      <Typewriter mode="loopOnce" cursor={false} element="span">
        <h1 class="md:text-4xl text-3xl font-bold leading-10">
          UX/UI Designer, with a Affinity for Web Development
        </h1>
        <h1 class="md:text-4xl text-3xl font-bold leading-10">
          Front End Developer, with a Spark of UX/UI Design
        </h1>
      </Typewriter>
      <p class="text-xl my-5">
        ...and I’m passionate about developing & designing digital products
        package with an amazing experiences.
      </p>
      <div class="flex">
        <a
          class="text-gray-800 bg-white border-almostwhite border-gray-300 text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-myblue hover:-translate-y-1 hover:drop-shadow-md transition"
          href="/work"
        >
          Showcase</a
        >
        <img
          class="ml-2 fa-arrow-left"
          src="/base/icons/arrow-point-left.svg"
          alt="arrow pointing to my work"
        />
      </div>
    </div>

    <img
      class="place-self-center pb-10 hidden lg:block hover:rotate-6 transition active:-rotate-6 mr-5"
      src="/base/move-monitor.webp"
      alt=""
    />
  </div>
</div>

<MarqueeTextWidget duration={20} repeat={3} paused={pauseOnHover}>
  <div class="flex mb-7 mt-3">
    <div 
      class="flex border-4 border-almostwhite bg-black rounded-2xl drop-shadow-xl p-5 mx-3 hover:hover:scale-105  hover:drop-shadow-xl transition ease-in-out"
    >
      <span class="ml-3 mr-3 cursor-default">
        <h2 class="flex justify-between text-2xl font-semibold">
          <span class="self-center mr-3"> human-focus-design </span>
          <img class="h-12" src="/base/icons/human-focus-design.webp" alt="" />
        </h2>
      </span>
    </div>

    <div
      class="flex border-4 border-almostwhite bg-white rounded-2xl drop-shadow-xl p-5 mx-3 hover:hover:scale-105  hover:drop-shadow-xl transition ease-in-out"
    >
      <span class="ml-3 mr-3 cursor-default">
        <h2 class="flex justify-between text-2xl font-semibold">
          <span class="self-center mr-3"> combo-dev-designer </span>
          <img class="h-12" src="/base/icons/combo-dev-designer.webp" alt="" />
        </h2>
      </span>
    </div>

    <div
      class="flex border-4 border-almostwhite bg-white rounded-2xl drop-shadow-xl p-5 mx-3 hover:hover:scale-105  hover:drop-shadow-xl transition ease-in-out"
    >
      <span class="ml-3 mr-3 cursor-default">
        <h2 class="flex justify-between text-2xl font-semibold">
          <span class="self-center mr-3"> problem-solver </span>
          <img class="h-12" src="/base/icons/computational-coder.webp" alt="" />
        </h2>
      </span>
    </div>
  </div>
</MarqueeTextWidget>

<div class="container mx-auto my-12">
  <h3 class="lg:mx-10 mx-5 text-3xl font-bold mb-5 ">Recent Work</h3>
  <div class="grid lg:grid-cols-2 col-cols-1 md:mx-20 mx-5 ">
    <a class="mx-5 place-self-center mb-5 hover:scale-105 transition" href="/">
      <div class="img-click-container transition hover:scale-100 ">
        <img
          class="rounded-2xl w-full img-click-image border-[11px] border-almostblack  drop-shadow-2xl"
          src="/base/air.png"
          alt=""
        />
        <div class="img-overlay">
          <div class="img-click-content mt-2">
            <div class="flex justify-center mb-3">
              <img class="" src="/base/icons/eye-icon.svg" alt="" />
            </div>
          </div>
        </div>
      </div>
    </a>

    <div class="place-self-center lg:mx-11 md:mx-5">
      <p class="text-base">Case Study</p>
      <h4 class="text-3xl my-2 font-semibold">Design Process</h4>
      <p class="text-sm mb-5">
        Problem solving. At the end of this phase you’ll have a pixel perfect
        design for your app or website. During the transition from wireframes
        into the final design I create prototypes simulating final end results
        before development.
      </p>
      <span>
        <div class="flex flex-col">
          <a
            class="text-center text-gray-800 bg-white text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-myblue hover:-translate-y-1 hover:drop-shadow-md transition"
            href="/">View Case</a
          >
          <a class="text-center hover:font-bold transition mt-2" href="/"
            >Explore Works</a
          >

          <br />
          <br />
        </div>
      </span>
    </div>
  </div>
</div>

<style>
  .fa-arrow-left {
    -webkit-animation: bounceLeft 2s infinite;
    animation: bounceLeft 2s infinite;
  }

  @-webkit-keyframes bounceLeft {
    0%,
    20%,
    50%,
    80%,
    100% {
      -webkit-transform: translateX(0);
      transform: translateX(0);
    }
    40% {
      -webkit-transform: translateX(30px);
      transform: translateX(30px);
    }
    60% {
      -webkit-transform: translateX(15px);
      transform: translateX(15px);
    }
  }
  @-moz-keyframes bounceLeft {
    0%,
    20%,
    50%,
    80%,
    100% {
      transform: translateX(0);
    }
    40% {
      transform: translateX(30px);
    }
    60% {
      transform: translateX(15px);
    }
  }
  @keyframes bounceLeft {
    0%,
    20%,
    50%,
    80%,
    100% {
      -ms-transform: translateX(0);
      transform: translateX(0);
    }
    40% {
      -ms-transform: translateX(30px);
      transform: translateX(30px);
    }
    60% {
      -ms-transform: translateX(15px);
      transform: translateX(15px);
    }
  }

  /*
.code {
  background: #263238;
  color: #eff;
  padding: 1rem 3rem;
  margin: 1rem;
  position: relative;
  border-radius: 0.25rem;
  counter-reset: step;
  counter-increment: step 0;
  transition: background 0.3s;
  outline: none;
}
.code:focus {
  background: #2e3d44;
}
.code p {
  position: relative;
  margin: 0.2rem;
  font-family: monospace;
  display: block;
  white-space: pre;
}
.code p::before {
  position: absolute;
  top: 0;
  left: -1.75rem;
  color: #50646d;
  user-select: none;
  content: counter(step);
  counter-increment: step;
}

*/

  .img-click-container {
    position: relative;
    width: 100%;
  }

  .img-click-image {
    display: block;
    width: 100%;
    height: auto;
  }

  .img-overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: 0.5s ease;
    background: rgba(0, 0, 0, 0.8);
    border-radius: 1rem;
  }

  .img-click-container:hover .img-overlay {
    opacity: 1;
  }

  .img-click-content {
    color: white;
    font-size: 20px;
    position: absolute;
    top: 50%;
    left: 50%;
    -webkit-transform: translate(-50%, -50%);
    -ms-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
    text-align: center;
  }
</style>
