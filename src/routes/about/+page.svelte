<script>
  import Accordion6 from "../../components/Accordion6.svelte";
  import MarqueeTextWidget from "svelte-marquee-text-widget";
  import Accordion7 from "../../components/Accordion7.svelte";
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
      class="grid content-between p-1 lg:w-1/2 w-100 my-none my-auto cursor-default"
    >
      <span>
        <h1
          class="border-b-4 border-appleblue text-3xl font-semibold py-5 mb-5"
        >
          About Me ( Michael Tran ) ✨
        </h1>
        <p class="text-xl">
          I've always had a love for drawing and creating art—a passion that has instilled in me a genuine joy for imagining and bringing things to life. However, despite my love for the craft, I grew up in a family that wasn't supportive. Consequently, I pursued a science-based degree. Nonetheless, the calling for design persisted within me, prompting me to work twice as hard. Over time, I've come to realize that I can't balance both paths, leading me to commit fully to following my dreams and passions while I still can.
        </p>
        <p class="text-xl mt-3">
          Give me a chance, and I won't let you down!
        </p>
      </span>

      <p class="text-xl text-left">
        <br />
        <a
          class="hover:text-appleblue underline"
          href="https://www.linkedin.com/in/michael-tran-20462112a/">LinkedIn</a
        >
        |
        <a
          class="hover:text-appleblue underline"
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
      <h2 class="text-4xl font-bold mb-3">My Core Values:</h2>
      <p class="text-lg mb-5">
        In essence, I prioritize delivering high-quality work, focusing on creating exceptional products, enhancing systems, and acting as a driving force to transform your ideas into reality.

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
          I believe in being a positive influence and making a meaningful impact in everything that I do. I'm confident that fostering a positive environment will result in high-quality work for everyone involved.
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
          I'm an academic at heart, driven to discover and understand things. I find fulfillment in acquiring new skills and knowledge to prepare myself for the challenges of the future.
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
          I strive for excellence in everything that I do, approaching tasks with careful consideration, a commitment to continuous improvement, and diligent maintenance. I am dedicated to producing high-quality work that you'll love.
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
          I'm organized and proficient at managing my time. I'll send updates, maintain a log of daily duties, track tasks, and overall ensure that everything is done in a timely manner, ensuring success!
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

<!-- <div
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
</div> -->

<div
  class="mx-5 md:mx-16 lg:mx-16 xl:mx-16 my-12 pb-6 2xl:mx-48 cursor-default"
>
  <h3 class="text-4xl text-center font-semibold">
    If you catch me in the wild, I’ll be...
  </h3>
  <p class="text-lg text-center">doing a bunch of stuff, but mostly I’ll be*</p>
  <div class="grid xl:grid-cols-4 md:grid-cols-2 grid-cols-1 gap-5 mt-10">
    <div>
      <img
        class=" border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl w-full"
        src="/about/viet-food.webp"
        alt=""
      />
      <p class="text-xl text-center mt-3">cooking exotic meals</p>
    </div>

    <div>
      <img
        class=" border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl w-full"
        src="/about/dnd.webp"
        alt=""
      />
      <p class="text-xl text-center mt-3">playing board games</p>
    </div>

    <div>
      <img
        class=" border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl w-full"
        src="/about/code.webp"
        alt=""
      />
      <p class="text-xl text-center mt-3">just researching</p>
    </div>

    <div>
      <img
        class=" border-8 border-almostblack rounded-3xl place-self-center mr-5 drop-shadow-2xl w-full"
        src="/about/clouds.webp"
        alt=""
      />
      <p class="text-xl text-center mt-3">getting some fresh air 😱</p>
    </div>
  </div>
</div>

<div
  class="mx-5 md:mx-16 lg:mx-16 xl:mx-16 my-12 pb-6 2xl:mx-48 cursor-default"
>
<h3 class="text-4xl text-center font-semibold">
  FAQs
</h3>
<p class="text-lg text-center">Frequently Asked Questions</p>

<div class="border-8 border-[#6E6E73] rounded-3xl mt-10">
<Accordion7
question_5="What Are Your Salary Expectations?" answer_5="I'm seeking a salary that aligns with industry standards. However, I am open to adjusting my expectations based on the benefits and opportunities your company offers."
question_4="What Programming Languages do you Know?" answer_4="I am proficient in the three primary web programming languages: HTML, CSS, and JavaScript. Additionally, I have experience with Python and have worked with frameworks such as React, Vue, and Svelte. I particularly enjoy using Svelte due to its simplicity."
question_3="How do you handle stress and pressure?" answer_3="I effectively manage stress by maintaining a high level of organization. Having a structured approach helps me navigate through challenging situations, knowing that I have the tools and steps to overcome any obstacle."
question_6="Where do you see yourself in five years?" answer_6="Honestly, I envision myself working for a company that I admire and that values me. Ideally, I'd like to have progressed to a senior-level position within the company."
question_2="Can you explain your development process?" answer_2="My development process starts with a thorough understanding of project requirements. I break tasks into manageable steps, coding and testing iteratively. Regular feedback from team members is crucial to ensure alignment with project goals before deploying the code"
question_1="Can you walk us through your design process?" answer_1="I begin my design process by envisioning the overall concept and creating a mood board to capture the project's essence. After sketching and rendering visual concepts, I seek approval for refinement based on feedback. Multiple iterations are conducted until the design reaches its completion, ensuring alignment with the visual representation and project goals."
question_7= "Tell me more about yourself?" answer_7="I'm a first-generation college student, proudly graduating summa cum laude. I've been in the workforce since the age of fourteen (for survival). Along the way, I picked up certifications in welding, and my childhood dream of being a chef led me to a genuine love for cooking. I actually double-majored twice, so I've earned four degrees. I'm also deeply loyal, and I love my family. Additionally, I enjoy consuming informational books, such as motivation books or just dense information books in general. I'm always online, consuming media, and I'm a night owl who forces myself to be a morning person."
/>
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
