<script>
  import MarqueeTextWidget from "svelte-marquee-text-widget";
  function handleObserver(x) {
    console.info(x.detail.observing);
  }

  let area;
  let i = 0;
  let pauseOnHover = false;
</script>

<div class=" container mx-auto px-4 grid content-center pt-0 md:py-10">
  <div
    class="flex flex-col lg:flex-row md:mx-12 lg:mx-0 2xl:mx-24 drop-shadow-xl"
  >
    <div class=" lg:w-1/2 mr-5 grid content-center w-100 my-5 m-5">
      <img
        class="transition border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl"
        src="/about/photo-of-mike.webp"
        alt=""
      />
    </div>
    <div
      class="grid content-between p-10 lg:w-1/2 w-100 my-none my-auto cursor-default"
    >
      <span>
        <h1
          class="border-b-4 border-appleblue text-3xl font-semibold py-5 mb-5"
        >
          Meet Mike Tran, The Web Wizard 🔮 ~!
        </h1>
        <p class="text-2xl">
          If you’re seeking a someone who can creativity craft websites that
          goes above and beyond the call to action, that push the limits of
          technology and ensuring an everlasting quality, I might be you’re guy!
        </p>
      </span>

      <p class="text-xl">
        <br />
        <a
          class="hover:text-appleblue"
          href="https://www.linkedin.com/in/michael-tran-20462112a/">LinkedIn</a
        >
        |
        <a
          class="hover:text-appleblue"
          href="/about/Michael Tran Resume_CV.pdf">Resume</a
        >
      </p>
    </div>
  </div>
</div>

<div
  class="flex justify-center items-center flex-col my-12 animate-bounce mt-32"
>
  <h2 class="text-3xl font-semibold">More About Me</h2>
  <img
    class=""
    src="/base/icons/arrow-down.svg"
    alt="arrow pointing down to learn more about me!"
  />
</div>

<!--
<button on:click={() => (pauseOnHover = !pauseOnHover)}> 
	{#if pauseOnHover}
	Pause Marquee
	{:else}
	Start Marquee
{/if}
</button>
-->

<!-- <MarqueeTextWidget duration={20} repeat={5} paused={pauseOnHover}>
	<div class="flex mb-7 mt-3">
		<div
			class="flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
		>
			<span class="ml-3 mr-3 cursor-default">
				<h2 class="flex justify-between text-2xl font-semibold">
					<span class="self-center mr-3"> combo-dev-designer </span>
					<img class="h-12" src="/base/icons/combo-dev-designer.webp" alt="" />
				</h2>
			</span>
		</div>

		<div
			class="flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
		>
			<span class="ml-3 mr-3 cursor-default">
				<h2 class="flex justify-between text-2xl font-semibold">
					<span class="self-center mr-3"> growth-mindset </span>
					<img class="h-12" src="/base/icons/growth-minset.webp" alt="" />
				</h2>
			</span>
		</div>

		<div
			class="flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
		>
			<span class="ml-3 mr-3 cursor-default">
				<h2 class="flex justify-between text-2xl font-semibold">
					<span class="self-center mr-3"> key-communicator </span>
					<img class="h-12" src="/base/icons/key-communicator.webp" alt="" />
				</h2>
			</span>
		</div>
	</div>
</MarqueeTextWidget> -->

<div
  class="mx-5 md:mx-16 lg:mx-16 xl:mx-16 2xl:mx-48 my-12 pb-6 cursor-default"
>
  <div class="flex flex-col lg:flex-row md:flex-col">
    <div class="basis-2/3 mr-5">
      <h2 class="text-5xl font-bold mb-3">My Core Values:</h2>
      <p class="text-lg mb-5">
        In essence, I value doing good work that focuses on creating high-quality products, improving systems, and serving as a driving force to turn your ideas into reality.

      </p>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
      <div
        class="border-almostwhite select-none bg-white rounded-2xl px-5 shadow-xl border-4 p-5"
      >
        <div class="flex">
          <img class="h-12" src="/base/icons/happy-go-lucky.webp" alt="" />
          <span class="self-center mr-3 font-semibold ml-3 text-2xl"
            >Make a Positive Impact</span
          >
        </div>
        <p class="py-3 text-lg">
          I believe in being a good influence and making a positive impact in
          everything that I do. I believe a positive impact will lead to high
          quality work, for everyone involved.
        </p>
      </div>

      <div
        class="border-almostwhite select-none bg-white rounded-2xl px-5 shadow-xl border-4 p-5"
      >
        <div class="flex">
          <img class="h-12" src="/base/icons/growth-minset.webp" alt="" />
          <span class="self-center mr-3 font-semibold ml-3 text-2xl"
            >Learning & Growing</span
          >
        </div>
        <p class="py-3 text-lg">
          I’m an academic at heart, I seek to find and understand things, I find
          fulfillment in acquiring new skills and knowledge, to prepare myself
          for the challenges of the future.
        </p>
      </div>

      <div
        class="border-almostwhite select-none bg-white rounded-2xl px-5 shadow-xl border-4 p-5"
      >
        <div class="flex">
          <img
            class="h-12"
            src="/base/icons/making-things-happen.webp"
            alt=""
          />
          <span class="self-center mr-3 font-semibold ml-3 text-2xl"
            >Produce Quality Work</span
          >
        </div>
        <p class="py-3 text-lg">
          I strive for execellence in everything that I do, with careful
          consideration, improvement and maintenance. I'm dedicated to producing
          high-quality work that you'll love.
        </p>
      </div>

      <div
        class="border-almostwhite select-none bg-white rounded-2xl px-5 shadow-xl border-4 p-5"
      >
        <div class="flex">
          <img class="h-12" src="/base/icons/well-optimized.webp" alt="" />
          <span class="self-center mr-3 font-semibold ml-3 text-2xl"
            >Insure Results</span
          >
        </div>
        <p class="py-3 text-lg">
          I'm organized and proficient at managing my time, I’ll send updates,
          keep a log of daily duties, track tasks and overall make sure
          everything is done in a timely manner. Insuring sucess!
        </p>
      </div>
    </div>
  </div>
</div>

<!-- <MarqueeTextWidget duration={20} repeat={5} paused={pauseOnHover}>
	<div class="flex mb-7 mt-3">
		<div
			class="flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
		>
			<span class="ml-3 mr-3 cursor-default">
				<h2 class="flex justify-between text-2xl font-semibold">
					<span class="self-center mr-3"> happy-go-lucky </span>
					<img class="h-12" src="/base/icons/happy-go-lucky.webp" alt="" />
				</h2>
			</span>
		</div>

		<div
			class="flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
		>
			<span class="ml-3 mr-3 cursor-default">
				<h2 class="flex justify-between text-2xl font-semibold">
					<span class="self-center mr-3"> well-optimized </span>
					<img class="h-12" src="/base/icons/well-optimized.webp" alt="" />
				</h2>
			</span>
		</div>

		<div
			class="flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
		>
			<span class="ml-3 mr-3 cursor-default">
				<h2 class="flex justify-between text-2xl font-semibold">
					<span class="self-center mr-3"> making-things-happen </span>
					<img class="h-12" src="/base/icons/making-things-happen.webp" alt="" />
				</h2>
			</span>
		</div>
	</div>
</MarqueeTextWidget> -->

<div
  class="mx-5 md:mx-16 lg:mx-16 xl:mx-16 2xl:mx-48 my-12 pb-6 cursor-default"
>
  <h2 class="text-5xl font-semibold text-center">Résumé Summary</h2>
  <p class="text-lg mb-10 text-center">Curriculum Vitae</p>
  <div class="grid lg:grid-cols-3 grid-cols-1 gap-5">
    <div
      class="bg-white border-almostwhite transition p-10 rounded-2xl shadow-2xl border-4"
    >
      <div class="flex">
        <img class="h-12" src="/base/icons/inquisitive-alumni.webp" alt="" />
        <span class="self-center mr-3 font-semibold ml-3 text-2xl"
          >General Education
        </span>
      </div>
      <p class="mt-5 text-lg">
        <span class="font-semibold"> Bachelor of Science </span> - BS, Web
        Development & UX Design,
        <span class="font-semibold">Associate of Science</span>
        - AS, Computer Science & IT <br />
        <span class="font-semibold"> Focus Areas: </span> User Experience (UX), User
        Interaction Theory (UI), Full Stack Development
      </p>
    </div>

    <div
      class="bg-white border-almostwhite transition p-10 rounded-2xl shadow-2xl border-4"
    >
      <div class="flex">
        <img class="h-12" src="/base/icons/human-focus-design.webp" alt="" />
        <span class="self-center mr-3 font-semibold ml-3 text-2xl"
          >Ideal Design Tools</span
        >
      </div>
      <p class="mt-5 text-lg">
        <span class="font-semibold"> General Web Design: </span> Figma <br />
        <span class="font-semibold"> Digital Art: </span>Affinity Photo &
        Procreate <br />
        <span class="font-semibold"> Vector Assets: </span>Affinity Design &
        Figma <br />
        <span class="font-semibold"> Focus Areas: </span>UX Focus Design, Best
        Practices, Material Design
      </p>
    </div>

    <div
      class="bg-white border-almostwhite p-10 rounded-2xl shadow-2xl border-4"
    >
      <div class="flex">
        <img class="h-12" src="/base/icons/computational-coder.webp" alt="" />
        <span class="self-center mr-3 font-semibold ml-3 text-2xl"
          >Preferable Development</span
        >
      </div>
      <p class="mt-5 text-lg">
        <span class="font-semibold"> Coding Languages: </span>HTML,CSS &
        JavaScript
        <span class="font-semibold"> Framework/Compilers: </span>Svelte &
        Sveltekit <br />
        <span class="font-semibold"> Database: </span> MongoDB <br />
        <span class="font-semibold"> Focus Areas: </span>Loading Speed,
        Animation & Motion, Aesthetically Pleasing UI Development.
      </p>
    </div>
  </div>

  <div class="flex justify-center mt-10">
    <a
      class="text-gray-800 bg-white text-xl border-4 p-2 px-7 rounded-full border-zinc-700 border-applered hover:-translate-y-1 hover:drop-shadow-md transition"
      href="/about/Michael Tran Resume_CV.pdf"
      download
      ><img
        class="inline"
        src="/base/icons/download.svg"
        alt="michael's resume download"
      /> Resume Download
    </a>
  </div>
</div>

<div
  class="mx-5 md:mx-16 lg:mx-16 xl:mx-16 2xl:mx-10 my-12 pb-6 2xl:mx-48 cursor-default"
>
  <h3 class="text-5xl text-center font-semibold">
    If you catch me in the wild, I’ll be...
  </h3>
  <p class="text-lg text-center">doing a bunch of stuff, but mostly I’ll be*</p>
  <div class="grid xl:grid-cols-4 lg:grid-cols-2 grid-cols-2 gap-5 mt-10">
    <div>
      <img
        class=" border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl rounded-2xl w-full"
        src="/about/viet-food.webp"
        alt=""
      />
      <p class="text-xl text-center mt-3">cooking exotic meals</p>
    </div>

    <div>
      <img
        class=" border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl rounded-2xl w-full"
        src="/about/dnd.webp"
        alt=""
      />
      <p class="text-xl text-center mt-3">playing board games</p>
    </div>

    <div>
      <img
        class=" border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl rounded-2xl w-full"
        src="/about/code.webp"
        alt=""
      />
      <p class="text-xl text-center mt-3">just researching</p>
    </div>

    <div>
      <img
        class=" border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl rounded-2xl w-full"
        src="/about/clouds.webp"
        alt=""
      />
      <p class="text-xl text-center mt-3">getting some fresh air 😱</p>
    </div>
  </div>
</div>

<style>
  @keyframes -global-from-left {
    0% {
      transform: rotateX(50deg) translateX(-200vw) skewX(-50deg);
      opacity: 1;
    }
    100% {
      transform: rotateX(0deg) translateX(0) skewX(0deg);
      opacity: 1;
    }
  }

  @keyframes -global-from-right {
    0% {
      transform: rotateX(-50deg) translateX(200vw) skewX(50deg);
      opacity: 1;
    }
    100% {
      transform: rotateX(0deg) translateX(0) skewX(0deg);
      opacity: 1;
    }
  }

  @keyframes -global-puff-in-center {
    0% {
      transform: scale(2);
      filter: blur(4px);
      opacity: 0;
    }
    100% {
      transform: scale(1);
      filter: blur(0px);
      opacity: 1;
    }
  }

  @keyframes -global-fade-in {
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }
</style>
