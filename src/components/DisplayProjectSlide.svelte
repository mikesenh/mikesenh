<script>
    export let img_src = '/project/thumbnail.png'
    export let img_alt = 'Error 418 : Server Refuse to Brew'
    export let title_string = 'title_string={?}'
    export let link_href = 'link_href={?}'
    export let extra_string = "extra_string={?}";
</script>

<div
class="group hover:scale-105 transition bg-white p-5 rounded-2xl drop-shadow-xl m-3 mb-12 w-90"
>
<div class="flex justify-between">
  <span>
    <p class="text-lg">{extra_string}</p>
    <h2 class="text-2xl font-semibold ">{title_string}</h2>
  </span>
  <a href={link_href}>
  <button class="transition scale-110 hover:scale-125">
    <img
      class="transition-color border-greyblack border-[3px] rounded-full p-1 "
      src="/base/icons/upward-arrow.svg"
      alt={`view ${title_string}`}
    />
    </button>
  </a>
</div>
<div class="mb-4"></div>
<!-- <p class="text-base border-t-[3px] py-3 mt-3 border-appleblue ">
  {desc_string}
</p> -->
<a href={link_href}>
  <div class="img-click-container transition  hover:scale-100">
    <img
      class="rounded-2xl w-full img-click-image"
      src={img_src}
      alt={img_alt}
    />
   
  </div>
</a>
</div>