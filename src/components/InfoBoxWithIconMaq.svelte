<script>
    export let title = "Web Developement"
    export let words = "If you're in the market for handcrafted websites with features that go beyond a typical website, I might be your guy!"
    export let img_src = "/base/icons/computational-coder.webp"
</script>

<div
        class="w-96 flex border-4 bg-white select-none border-almostwhite rounded-2xl p-5 mx-3 hover:hover:scale-105 active:hover:scale-95 hover:drop-shadow-lg transition ease-in-out"
      >
        <span class="ml-3 mr-3 cursor-default">
          <h2 class="flex justify-between text-2xl font-semibold">
            <span class="self-center mr-3 mb-2">{title}</span>
            <img
              class="h-12 mb-2"
              src={img_src}
              alt=""
            />
          </h2>
          <p class="mb-2">
            {words}
          </p>
        </span>
      </div>