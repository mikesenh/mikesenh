<script>
    export let extra_string = 'extra_string={?}'
    export let title_string = 'title_string={?}'
    export let desc_string = 'desc_string={?}'
    export let link_href = 'link_href={?}'
    export let btn_string = 'btn_string={?}'
</script>

<div class="container mx-auto my-12">
    <!-- <h3 class="lg:mx-10 mx-5 text-3xl font-bold mb-5 ">Recent Work</h3> -->
    <div class="grid lg:grid-cols-2 col-cols-1 mx-5">
      <a
        class=" place-self-center mb-5 hover:scale-105 transition"
        href={link_href}
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
          {extra_string}
        </p>
        <h4 class="text-3xl my-2 font-semibold">{title_string}</h4>
        <p class="text-lg mb-5">
          {desc_string}
        </p>
        <span>
          <div class="flex">
            <a
              class="text-center border-almostwhite text-gray-800 bg-white text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-myblue hover:-translate-y-1 hover:drop-shadow-md transition"
              href={link_href}>{btn_string}</a
            >

            <br />
            <br />
          </div>
        </span>
      </div>
    </div>
  </div>

  <style>
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