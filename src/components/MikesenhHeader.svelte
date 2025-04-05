<script>
import Typewriter from "svelte-typewriter";
</script>

<div class="relative w-full overflow-hidden flex items-center justify-center">
  <!-- Marquee text behind image -->
  <div class="absolute top-1/2 w-full transform -translate-y-1/2 z-0">
    <p class="marquee text-center md:text-5xl text-3xl mt-3 font-bold select-none">
      while(alive)&#123;&nbsp;<span style="color:#63bc48">eat(goodFood);</span>&nbsp;<span style="color:#039ede;">sleep(onIt);</span>&nbsp;<span style="color:#fab826;">code(forFun);</span>&nbsp;<span style="color:#e13b3f;">create(withLove);&nbsp;</span>&#125;
    </p>
  </div>

  <!-- Fully opaque centered image on top -->
  <div class="relative">
    <img
width="762"
      height="256"
      src=/base/move-machines.webp
      alt="Center Image"
      class="px-5 my-5 sm:h-48 md:h-64 hover:scale-105 transition active:scale-95 select-none"
    />
  </div>
</div>

<div class="h-32 mb-10">
  ‎ ‎
  <Typewriter mode="loopOnce" cursor={false} element="span">
    <h1 class="text-center md:text-5xl text-3xl mt-3 font-bold select-none">
      Hi I'm Michael Hoang Tran!
    </h1>
    <h1 class="text-center md:text-5xl text-3xl mt-3 font-bold select-none">
      ... And I'm Here to Bring Your Vision to Life!
    </h1>
    <h1 class="text-center md:text-5xl text-3xl mt-3 font-bold select-none">
      I'm a Designer / Developer / Artisan...
    </h1>
    <!-- <h1 class="text-center md:text-5xl text-3xl mt-3 font-bold select-none">
      ... And I make websites so cool, even penguins want to surf them!
    </h1>
    <h1 class="text-center md:text-5xl text-3xl mt-3 font-bold select-none">
      Start only 75$ per page design, 75$ per page developed & launched!
    </h1> -->
    <span>
    <h1 class="text-center md:text-5xl text-3xl mt-3 font-bold select-none">
      www.mikesenh.com
    </h1>
  </span>
  </Typewriter>
  <p class="text-center text-xl mb-5 mt-3 select-none ">
    ‎ ‎
    <Typewriter mode="loopOnce" cursor={false} delay={12000} element="span">
      <span>
        Where I Mike; Design & Develope Things
      </span>
    </Typewriter>
  </p>
</div>

<style>
  @keyframes marquee {
    0% { transform: translateX(100%); }
    100% { transform: translateX(-100%); }
  }

  .marquee {
    animation: marquee 20s linear infinite;
    white-space: nowrap;
  }
</style>
