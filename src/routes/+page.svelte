<script>
  import Typewriter from "svelte-typewriter";
  import MarqueeTextWidget from "svelte-marquee-text-widget";
  let touchMarquee = false;
  function marqueePause() {
    touchMarquee = true;
  }

  let powerUp = false;

  let colour = '/base/machines.webp';
	function handleMouseOver(e) {
		colour = '/base/move-machines.webp';
	}
	function handleMouseOut(e) {
		colour = '/base/machines.webp';
	}
	const onFocus =()=>isFocused=true;
	const onBlur =()=>isFocused=false;
</script>

<!-- bg-[url('/base/bg-transblue.png')] -->
<div class="bg-contain pb-10 ">
<div class="mx-auto container ">
  <div class="flex justify-center">
  <!-- <div class="flex items-center mb-4">
    <input bind:checked={powerUp} id="default-checkbox" type="checkbox" value="" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
    <label for="default-checkbox" class="ml-2 text-xl font-medium text-gray-900 dark:text-gray-300">Power Up!</label>
</div> -->
</div>
  <div class="flex justify-center">
  
    <img class="px-5 my-5 sm:h-48 md:h-64 hover:scale-105 transition active:scale-95 select-none" src="/base/move-machines.webp" alt="3 retro machines in a svg vector format">
    
  </div>
  
  
    <h1 class="text-center md:text-4xl text-3xl font-bold select-none">‎ ‎
      <Typewriter mode="loopOnce" cursor={false} element="span">
        <span>
        UX/UI Designer, with a Affinity for Web Development
      </span>
      <span>
        Front End Developer, with a Spark of UX/UI Design
      </span>
      </Typewriter>
    </h1>

    <p class="text-center text-xl my-5 select-none">‎ ‎
  <Typewriter mode="loopOnce" cursor={false} element="span">
    <span>
    ...and I’m passionate about developing & designing digital products
    package with an amazing experiences.
  </span>
</Typewriter>
</p>
  <div class="flex justify-center">
  <a
          class="text-gray-800 bg-white border-myblue border-gray-300 text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-myblue hover:-translate-y-1 hover:drop-shadow-md transition"
          href="/work"
        >
        Ideas I've brought to life</a
        >
      </div>
</div>
</div>

<!-- bg-[url('/base/bg-transblue-flip.png')] -->
<div class="">

<MarqueeTextWidget duration={20} repeat={5} paused={touchMarquee}>
  <div class="flex mb-7 mt-3" on:mouseover={()=>{touchMarquee = true}} on:mouseout={()=>{touchMarquee = false}} on:focus={onFocus} on:blur={onBlur}>
    <div 
      class="w-96 flex border-4 border-almostwhite select-none bg-white rounded-2xl  p-5 mx-3 hover:hover:scale-105 active:hover:scale-95  hover:drop-shadow-lg transition ease-in-out"
    >
      <span class="ml-3 mr-3 cursor-default">
        <h2 class="flex justify-between text-2xl font-semibold">
          <span class="self-center mr-3 mb-2"> UX/UI Designed </span>
          <img class="h-12 mb-2" src="/base/icons/human-focus-design.webp" alt="" />
        </h2>
        <p class="mb-2">If you have a vision, I can bring it to life by prototype every idea down to the looks, feels and functions!</p>
      </span>
    </div>

    <div
      class="w-96 flex border-4 border-almostwhite select-none bg-white rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
    >
      <span class="ml-3 mr-3 cursor-default">
        <h2 class="flex justify-between text-2xl font-semibold">
          <span class="self-center mr-3 mb-2"> Content Maintenance </span>
          <img class="h-12 mb-2" src="/base/icons/combo-dev-designer.webp" alt="" />
        </h2>
        <p class="mb-2">If you already have a website rest assure I can keep it in good shape, you can count on me to keep everything updated!</p>
      </span>
    </div>

    <div
      class="w-96 flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
    >
      <span class="ml-3 mr-3 cursor-default">
        <h2 class="flex justify-between text-2xl font-semibold">
          <span class="self-center mr-3 mb-2"> Web Developement </span>
          <img class="h-12 mb-3 mb-2" src="/base/icons/computational-coder.webp" alt="" />
        </h2>
        <p class="mb-2">If you're in the market for a handcrafted websites, with features that go beyond a typical website, I might be you're guy!</p>
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
      <p class="text-lg mb-5">
        Problem solving. At the end of this phase you’ll have a pixel perfect
        design for your app or website. During the transition from wireframes
        into the final design I create prototypes simulating final end results
        before development.
      </p>
      <span>
        <div class="flex">
          <a
            class="text-center border-almostwhite text-gray-800 bg-white text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-myblue hover:-translate-y-1 hover:drop-shadow-md transition"
            href="/">View Case Study</a
          >
         

          <br />
          <br />
        </div>
      </span>
    </div>
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
