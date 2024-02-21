<script>
  import DisplayProjectSlide from "../../components/DisplayProjectSlide.svelte";

  import "../../app.css";

  import { Splide, SplideSlide, SplideTrack } from "@splidejs/svelte-splide";
  // Default theme
  import "@splidejs/svelte-splide/css";

  let slideShowing = 3;
  $: innerWidth = 0;

  $: if (innerWidth <= 768) {
    slideShowing = 1;
  } else if (innerWidth <= 1024) {
    slideShowing = 2;
  } else {
    slideShowing = 3;
  }
</script>

<svelte:window bind:innerWidth />
<!-- {slideShowing}
{innerWidth} -->

<div class="flex justify-center">
  <span>
    <div class="flex justify-center">
      <img
        class="h-64 hover:translate-y-3 transition active:-translate-y-3"
        src="/base/move-macintosh.webp"
        alt=""
      />
    </div>
    <h1 class="text-center text-6xl font-extrabold mt-5 mb-2">
      Featured Projects
    </h1>
    <p class="text-center text-lg">
      Crafted with love, a custom creation with a dash of technology!
    </p>
  </span>
</div>

<div class="">
  <Splide
    hasTrack={false}
    options={{
      type: "loop",
      pagination: false,
      perPage: slideShowing,
      perMove: 1,
    }}
    aria-label="My Favorite Images"
  >
    <div class="flex justify-center space-x-5 my-6 splide__arrows">
      <button
        class="splide__arrow--prev btn-yellow transition focus:translate-y-0 focus:drop-shadow-none hover:-translate-y-1 focus:bg-black hover:shadow-[4px_4px_1px_rgba(0,0,0,0.25)] border-appleyellow text-base border-[3px] px-16 py-1 rounded-3xl uppercase font-semibold"
        >Return</button
      >
      <button
        class="splide__arrow--next btn-blue transition hover:-translate-y-1 hover:shadow-[4px_4px_1px_rgba(0,0,0,0.25)] border-appleblue text-base border-[3px] px-16 py-1 rounded-3xl uppercase font-semibold"
        >Next</button
      >
    </div>
<!-- 
  * I was here
	? what happen
	TODO: DO THIS!
	! What going on here!
	% sadasdasd s
	 -->
    <SplideTrack>
      <SplideSlide>
        <div
          class="group hover:scale-105 transition bg-white p-5 rounded-2xl drop-shadow-xl m-3 mb-12"
        >
          <div class="flex justify-between">
            <span>
              <p class="text-lg">Case Study</p>
              <h2 class="text-2xl font-semibold ">Design Process</h2>
            </span>
            <button class="transition scale-110 hover:scale-125">
              <img
                class="transition-color border-greyblack border-[3px] rounded-full p-1 "
                src="/base/icons/upward-arrow.svg"
                alt=""
              /></button
            >
          </div>
          <p class="text-base border-t-[3px] py-3 mt-3 border-appleblue ">
            Donec rutrum congue leo eget malesuada.
          </p>
          <a href="/">
            <div class="img-click-container transition  hover:scale-100">
              <img
                class="rounded-2xl w-full img-click-image"
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
        </div>
      </SplideSlide>
      <SplideSlide>
        
        <DisplayProjectSlide
    img_src="/project/autosew/thumbnail.webp"
    img_alt="project: The Grace Company work: UX, UI & Web Development"
    extra_string="iOS / UX Design / UX Research/ UI Design"
    title_string="AutoSew Software"
    desc_string="In this project, I'd designed the UI of a quilting/sewing software. I was given the chance to conduct user research, delve into UX design, and ultimately visualize what the software could become."
    link_href="/work/project-autosew"
  />
      </SplideSlide>
      <SplideSlide>
        <div
          class="group hover:scale-105 transition bg-white p-5 rounded-xl drop-shadow-xl m-3 mb-12"
        >
          <div class="flex justify-between">
            <span>
              <p class="text-lg">Case Study</p>
              <h2 class="text-2xl font-semibold ">Design Process</h2>
            </span>
            <button class="transition scale-110 hover:scale-125">
              <img
                class="transition-color border-greyblack border-[3px] rounded-full p-1 "
                src="/base/icons/upward-arrow.svg"
                alt=""
              /></button
            >
          </div>
          <p class="text-base border-t-[3px] py-3 mt-3 border-appleblue ">
            Donec rutrum congue leo eget malesuada.
          </p>
          <a href="/">
            <div class="img-click-container transition  hover:scale-100">
              <img
                class="rounded-2xl w-full img-click-image"
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
        </div>
      </SplideSlide>
    </SplideTrack>
  </Splide>
</div>

<style>
  .btn-yellow {
    background-color: #ffffff;
    border-radius: 16px;
    border-color: #fbb826;
    border-width: 4px;
    padding: 0.5rem 1.5rem;
    border-radius: 9999px;

    transition: 0.25s;
  }

  .btn-yellow:hover {
    background-color: #fbb826;
    border-color: #1d1d1f;

    transform: translateY(-0.25rem);

    filter: drop-shadow(4px 4px 1px rgba(0, 0, 0, 0.25));
  }

  .btn-yellow:focus {
    border-radius: 16px;
    border-color: #6e6e73;
    background-color: #f6f8fa;
    border-width: 4px;
    padding: 0.5rem 1.5rem;
    border-radius: 9999px;

    transition: 0.15s;
    transform: translateY(0rem);
    filter: none;
  }

  .btn-blue {
    background-color: #ffffff;
    border-radius: 16px;
    border-color: #009edc;
    border-width: 4px;
    padding: 0.5rem 1.5rem;
    border-radius: 9999px;

    transition: 0.25s;
  }

  .btn-blue:hover {
    background-color: #009edc;
    border-color: #1d1d1f;

    transform: translateY(-0.25rem);
    filter: drop-shadow(4px 4px 1px rgba(0, 0, 0, 0.25));
  }

  .btn-blue:focus {
    border-radius: 16px;
    border-color: #6e6e73;
    background-color: #f6f8fa;
    border-width: 4px;
    padding: 0.5rem 1.5rem;
    border-radius: 9999px;

    transition: 0.15s;
    transform: translateY(0rem);
    filter: none;
  }

  .img-click-container {
    position: relative;
    width: 100%;
  }

  .img-click-image {
    display: block;
    width: 100%;
    height: auto;
  }

  /* .img-overlay {
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
  } */

  /* .img-click-container:hover .img-overlay {
    opacity: 1;
  } */

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
