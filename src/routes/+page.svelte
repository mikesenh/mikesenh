<script>
  import Typewriter from "svelte-typewriter";
  import MarqueeTextWidget from "svelte-marquee-text-widget";
  import { onMount } from "svelte";
  import DisplayProject from "../components/DisplayProject.svelte";
  import NoDisplayProject from "../components/NoDisplayProject.svelte";
  import WhyMeBlock from "../components/WhyMeBlock.svelte";
  let touchMarquee = false;
  function marqueePause() {
    touchMarquee = true;
  }

  let headline = "UX/UI Designer, with a Affinity for Web Development";
  let subheading = `...and I’m passionate about developing & designing digital products package with an amazing experiences.`;

  function textSwap() {
    let randomNumber = Math.floor(Math.random() * 3) + 1;
    let rememberNumber = randomNumber;
    while (rememberNumber == randomNumber) {
      randomNumber = Math.floor(Math.random() * 3) + 1;
      console.log(`CP2: ${rememberNumber} = ${randomNumber}`);
    }
    rememberNumber = randomNumber;

    switch (randomNumber) {
      case 1:
        headline = "Hello! I'm Michael Tran.";
        subheading =
          "I create websites that are so cool, even penguins will want to surf on them! 🐧";
        break;
      case 2:
        headline = "Hi! I'm Michael Tran.";
        subheading =
          "Welcome to my corner of the web, where I showcase what I've designed or developed. 🍵";
        break;
      case 3:
        headline =
          "Greatings! I'm Michael Tran.";
        subheading = "...and I’m passionate about developing and designing digital products packaged with amazing experiences. ✨";
        break;
    }
  }

  onMount(async () => {
    textSwap();
  });

  let powerUp = false;

  let colour = "/base/move-machines.webp";
  function handleMouseOver(e) {
    colour = "/base/move-machines.webp";
  }
  function handleMouseOut(e) {
    colour = "/base/machines.webp";
  }
  const onFocus = () => (isFocused = true);
  const onBlur = () => (isFocused = false);

  function scrollIntoView({ target }) {
    const el = document.querySelector(target.getAttribute("href"));
    if (!el) return;
    el.scrollIntoView({
      behavior: "smooth",
    });
  }
</script>

<!-- bg-[url('/base/bg-transblue.png')] -->
<div class="bg-contain pb-10">
  <div class="mx-auto container">
    <div class="flex justify-center">
      <!-- <div class="flex items-center mb-4">
    <input bind:checked={powerUp} id="default-checkbox" type="checkbox" value="" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
    <label for="default-checkbox" class="ml-2 text-xl font-medium text-gray-900 dark:text-gray-300">Power Up!</label>
</div> -->
    </div>
    <div class="flex justify-center">
      <button on:click={textSwap}>
        <!-- <img on:mouseover={handleMouseOut} on:mouseout={handleMouseOver} on:keydown={onBlur} on:blur={onBlur} on:focus={onFocus} class="px-5 my-5 sm:h-48 md:h-64 hover:scale-105 transition active:scale-95 select-none" src={colour} alt=""> -->

        <img
          width="762"
          height="256"
          class="px-5 my-5 sm:h-48 md:h-64 hover:scale-105 transition active:scale-95 select-none"
          src="/base/move-machines.webp"
          alt="3 retro machines in a svg vector format"
        />
      </button>
    </div>

    <h1 class="text-center md:text-4xl text-3xl mt-3 font-bold select-none">
      ‎ ‎
      <Typewriter mode="loopOnce" cursor={false} element="span">
        <span>
          {headline}
        </span>
      </Typewriter>
    </h1>

    <p class="text-center text-xl mb-5 mt-3 select-none">
      ‎ ‎
      <Typewriter mode="loopOnce" cursor={false} delay={2000} element="span">
        <span>
          {subheading}
        </span>
      </Typewriter>
    </p>
    <div class="flex justify-center">
      <a
        class="text-gray-800 bg-white border-myblue border-gray-300 text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-myblue hover:-translate-y-1 hover:drop-shadow-md transition"
        href="/work"
      >
        My Work</a
      >
    </div>
  </div>
</div>

<!-- bg-[url('/base/bg-transblue-flip.png')] -->
<div class="my-5">
  <MarqueeTextWidget duration={20} repeat={5} paused={touchMarquee}>
    <div
      class="flex mb-7 mt-3"
      on:mouseover={() => {
        touchMarquee = true;
      }}
      on:mouseout={() => {
        touchMarquee = false;
      }}
      on:focus={onFocus}
      on:blur={onBlur}
    >
      <div
        class="w-96 flex border-4 border-almostwhite select-none bg-white rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
      >
        <span class="ml-3 mr-3 cursor-default">
          <h2 class="flex justify-between text-2xl font-semibold">
            <span class="self-center mr-3 mb-2"> UX/UI Designed </span>
            <img
              class="h-12 mb-2"
              src="/base/icons/human-focus-design.webp"
              alt=""
            />
          </h2>
          <p class="mb-2">
            If you have a vision, I can bring it to life by prototyping every idea, down to the looks, feels, and functions!
          </p>
        </span>
      </div>

      <div
        class="w-96 flex border-4 border-almostwhite select-none bg-white rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
      >
        <span class="ml-3 mr-3 cursor-default">
          <h2 class="flex justify-between text-2xl font-semibold">
            <span class="self-center mr-3 mb-2"> Site Maintenance </span>
            <img
              class="h-12 mb-2"
              src="/base/icons/combo-dev-designer.webp"
              alt=""
            />
          </h2>
          <p class="mb-2">
            If you already have a website, rest assured that I can keep it in good shape. You can count on me to keep everything straight!
          </p>
        </span>
      </div>

      <div
        class="w-96 flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
      >
        <span class="ml-3 mr-3 cursor-default">
          <h2 class="flex justify-between text-2xl font-semibold">
            <span class="self-center mr-3 mb-2"> Web Developement </span>
            <img
              class="h-12 mb-2"
              src="/base/icons/computational-coder.webp"
              alt=""
            />
          </h2>
          <p class="mb-2">
            If you're in the market for handcrafted websites with features that go beyond a typical website, I might be your guy!
          </p>
        </span>
      </div>
    </div>
  </MarqueeTextWidget>
</div>

   <div
    class="flex sm:flex-row flex-col justify-center mt-5"
  >
    
    <span class="grid content-center mt-10">
      <span>
        <h3 class="text-4xl text-center font-bold mb-2">Reasons to Bring Me Onboard</h3>
        <p class="text-xl text-center mb-4">Knowledge / Specialization</p>
      </span>
    </span>
  </div>

  <div
    class="flex sm:flex-row flex-col justify-center mt-5 2xl:mx-52 lg:mx-48 md:mx-32 mx-10 my-5 mb-12"
  >
    
    <span class="grid content-center 2xl:grid-cols-3 md:grid-cols-2 sm:grid-cols-1 gap-12 mx-5">
      <WhyMeBlock
      img_src = '/home/why_me_1.webp'
      img_alt = 'User Experience Design graphic'
      title_string = 'User Experience Design'
      extra_string = "I focus on crafting meaningful user experiences, providing you with designs that prioritize user satisfaction."
      />
      <WhyMeBlock
      img_src = '/home/why_me_2.webp'
      img_alt = 'Conversion Optimization graphic'
      title_string = 'Conversion Optimization'
      extra_string = "I've studied the methods to convert a visitor into a customer, aiming to boost your revenue!"
      />
      <WhyMeBlock
      img_src = '/home/why_me_3.webp'
      img_alt = 'Responsive Design graphic'
      title_string = 'Responsive Design'
      extra_string = "I specialize in creating digital products that effortlessly adapt to any device, ensuring a seamless experience."
      />
      <WhyMeBlock
      img_src = '/home/why_me_4.webp'
      img_alt = 'Multiple Generative Variations graphic'
      title_string = 'Multiple Generative Variations'
      extra_string = "I am committed to ensuring your satisfaction with my work by offering you a variety of options to choose from!"
      />
      <WhyMeBlock
      img_src = '/home/why_me_5.webp'
      img_alt = 'Search Engine Optimized graphic'
      title_string = 'Search Engine Optimized'
      extra_string = "I integrate SEO strategies into my designs, ensuring you have a high-ranking website."
      />
      <WhyMeBlock
      img_src = '/home/why_me_6.webp'
      img_alt = 'One-Stop-Shop Solutions graphic'
      title_string = 'One-Stop-Shop Solutions'
      extra_string = "I offer all-inclusive design services and ongoing support. Just let me know!"
      />
  </span>

  <!-- <div
    id="scrolldown-ideas"
    class="flex sm:flex-row flex-col justify-center mt-5 mx-5"
  >
    <img class="sm:w-1/6 w-1/4" src="/base/move-macintosh.webp" alt="" />
    <span class="grid content-center">
      <span>
        <h3 class="text-3xl">Ideas I've Brought to Life!</h3>
        <p class="texl-base">Powered by Code and Creativity</p>
      </span>
    </span>
  </div> -->

  <!-- <div class="container mx-auto my-12">
   
    <div class="grid lg:grid-cols-2 col-cols-1 mx-5">
      <a
        class=" place-self-center mb-5 hover:scale-105 transition"
        href="/work/project-grace"
      >
        <div class="img-click-container transition hover:scale-100">
          <img
            class="rounded-2xl w-full img-click-image border-almostblack drop-shadow-2xl"
            src="/project/grace/thumbnail.png"
            alt="project grace company web design ui design"
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
        <p class="text-base">
          Web Design / Web Development / UX Design / UI Design
        </p>
        <h4 class="text-3xl my-2 font-semibold">The Grace Company</h4>
        <p class="text-lg mb-5">
          In this project, I undertook the mission to enhance and modernize The
          Grace Company's website, aligning it with contemporary design trends.
          By implementing a cohesive design system, the website underwent a
          transformation that not only resulted in increased sales but also
          positioned the company as a cutting-edge leader in the quilting
          machine and frame industry.
        </p>
        <span>
          <div class="flex">
            <a
              class="text-center border-almostwhite text-gray-800 bg-white text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-myblue hover:-translate-y-1 hover:drop-shadow-md transition"
              href="/work/project-grace">View Case Study</a
            >

            <br />
            <br />
          </div>
        </span>
      </div>
    </div>
  </div> -->

  <!-- <DisplayProject
    img_src="/project/autosew/thumbnail.webp"
    img_alt="project: The Grace Company work: UX, UI & Web Development"
    extra_string="iOS / UX Design / UX Research/ UI Design"
    title_string="AutoSew Software"
    desc_string="In this project, I'd designed the UI of a quilting/sewing software. I was given the chance to conduct user research, delve into UX design, and ultimately visualize what the software could become."
    link_href="/work/project-autosew"
    btn_string="View Case Study"
    option_char="R"
    is_disable="false"
  />

  <DisplayProject
    img_src="/project/grace/thumbnail.png"
    img_alt="project: The Grace Company work: UX, UI & Web Development"
    extra_string="Web Design / Web Development / UX Design / UI Design / Branding"
    title_string="The Grace Company"
    desc_string="In this project, I undertook the mission to enhance and modernize The
  Grace Company's website, aligning it with contemporary design trends.
  By implementing a cohesive design system, the website underwent a
  transformation that not only resulted in increased sales but also
  positioned the company as a cutting-edge leader in the quilting
  machine and frame industry."
    link_href="/work/project-grace"
    btn_string="View Case Study"
    option_char="L"
    is_disable="false"
  />

  <DisplayProject
    img_src="/project/toys/thumbnail.webp"
    img_alt="project: The Grace Company work: UX, UI & Web Development"
    extra_string="Web Design / UI Design"
    title_string="Incredibly Interconnectable Toys"
    desc_string="In this project, my main focus was to redesign the website for Incredibly Interconnectable Toys, infusing it with a fresh and captivating aesthetic. The aim was to provide an enhanced user experience, enticing visitors to explore the world of toys in a unique and engaging way. "
    link_href="/work/project-iit"
    btn_string="View Design"
    option_char="R"
    is_disable="true"
  />

  <DisplayProject
    img_src="/project/agawa/thumbnail.webp"
    img_alt="agawa thumbnail - japanese restaurant website"
    extra_string="Web Design / UI Design / Branding"
    title_string="Agawa"
    desc_string="In this project, I am designing a visually captivating and user-friendly website for a Japanese restaurant, with a focus on expanding their customer base by accommodating both English and Japanese languages. The primary goal is to create an immersive online experience that reflects the rich cultural heritage of Japan while ensuring seamless navigation and functionality for visitors."
    link_href="/work/project-agawa"
    btn_string="View Design"
    option_char="L"
    is_disable="true"
  /> -->
</div>

<style>
  /* .fa-arrow-left {
    -webkit-animation: bounceLeft 2s infinite;
    animation: bounceLeft 2s infinite;
  } */

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

  /* .img-click-container {
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
  } */
</style>
