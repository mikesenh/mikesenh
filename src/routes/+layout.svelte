<script>
	import '../app.css';
	import { page } from '$app/stores';
  //import PageTransition from '../component/PageTransition.svelte';

  //class:bg-macsilver={$page.url.pathname === '/portfolio'} class:bg-lightmacintosh={$page.url.pathname === '/about'}
  let showMenu = false;

  function toggleNavbar() {
    showMenu = !showMenu;
  }

  let colour = '/base/mikesenh_logo.webp';
	
	function handleMouseOver(e) {
		colour = '/base/move-mikesenh_logo.webp';
	}
	function handleMouseOut(e) {
		colour = '/base/mikesenh_logo.webp';
	}
	const onFocus =()=>isFocused=true;
	const onBlur =()=>isFocused=false;
</script>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<svelte:head>
  <link rel="icon" type="image/svg" href="/base/mikesenh_logo-dark.webp" />
</svelte:head>

<div class="bg-macbook">
<div class="">
	
	<div>
	  <nav
		class=" container px-6 py-8 mx-auto md:flex md:justify-between md:items-center "
	  >
		<div class="flex items-center justify-between">
		  <a
			class="text-xl font-bold text-gray-800 md:text-2xl hover:text-blue-400"
			href="/"
			>
			<span tooltip="Mikesenh" flow="right">
				<img on:mouseover={handleMouseOver} on:mouseout={handleMouseOut} on:blur={onBlur} on:focus={onFocus}  class="h-14 lg:h-24 hover:scale-105 transition" src={colour} alt="">
				
				</span>
		  </a>
		  <!-- Mobile menu button -->
		  <button on:click={toggleNavbar} class="flex md:hidden">
			<button
			  type="button"
			  class="text-gray-800 hover:text-gray-400 focus:outline-none focus:text-gray-400"
			>
			  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
			  <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
			</svg>
			</button>
		  </button>
		</div>
  
		<!-- Mobile Menu open: "block", Menu closed: "hidden" -->
		<div
		  class="flex-col mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-5 md:mt-0 {showMenu
			? 'flex'
			: 'hidden'}"
		>
		<!-- <a class="text-gray-800 text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-applegreen hover:-translate-y-1 hover:drop-shadow-md transition" href="/home">Blog</a> -->
		  <a class="text-gray-800 border-almostwhite bg-white text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-myblue hover:-translate-y-1 hover:drop-shadow-md transition" href="/work">Work</a>
		  
		  <!-- <a class="text-gray-800 hover:text-blue-400" href="/blog">Blogs</a>
		  <a class="text-gray-800 hover:text-blue-400" href="/contact">Contact US</a> -->
		  <a class="text-gray-800 border-almostwhite bg-white text-xl border-4 p-2 px-7 rounded-full border-zinc-700 hover:border-appleyellow hover:-translate-y-1 hover:drop-shadow-md transition" href="/about">About Me</a>
		</div>
	  </nav>
	</div>
  </div>



<div class="scroll-smooth ">
	<!-- svelte code: class:bg-macbook={$page.url.pathname === '/about'}-->


<slot />

<div class="">
	
<div class="flex justify-center border-greyblack ">
	<div class="">
	<a
	class="text-xl font-bold text-gray-800 md:text-2xl hover:text-blue-400"
	href="/"
	>
	<span tooltip="Mikesenh" flow="right">
		<img on:mouseover={handleMouseOver} on:mouseout={handleMouseOut} on:blur={onBlur} on:focus={onFocus}  class="mb-3
		 h-14 lg:h-24 hover:scale-105 transition" src={colour} alt="">
		
		</span>
  </a>
</div>
</div>
<div class="flex justify-center mx-5">
	<div class="mb-5">
	
  <p >All rights reserved. – Designed & Coded by Michael Tran © 2023</p>
</div>
</div>


</div>
</div>
</div>



<style>
	@import url('https://fonts.googleapis.com/css2?family=Jost&display=swap');
  
	/* START TOOLTIP STYLES */
	[tooltip] {
	  position: relative;
	}
  
	/* Applies to all tooltips */
	[tooltip]::before,
	[tooltip]::after {
	  text-transform: none;
	  font-size: .9em;
	  line-height: 1;
	  user-select: none;
	  pointer-events: none;
	  position: absolute;
	  display: none;
	  opacity: 0;
	}
	[tooltip]::before {
	  content: '';
	  border: 5px solid transparent;
	  z-index: 1001;
	}
	[tooltip]::after {
	  content: attr(tooltip);
	  font-family: 'Jost', sans-serif;
	  text-align: center;
	  min-width: 3em;
	  max-width: 21em;
	  white-space: nowrap;
	  overflow: hidden;
	  text-overflow: ellipsis;
	  padding: 1ch 1.5ch;
	  border-radius: .3ch;
	  box-shadow: 0 1em 2em -.5em rgba(0, 0, 0, 0.35);
	  background: #333;
	  color: #fff;
	  z-index: 1000;
	}
  
	/* Make the tooltips respond to hover */
	[tooltip]:hover::before,
	[tooltip]:hover::after {
	  display: block;
	}
  
	/* don't show empty tooltips */
	[tooltip='']::before,
	[tooltip='']::after {
	  display: none !important;
	}
  
	/* FLOW: RIGHT */
[tooltip][flow^="right"]::before {
  top: 65%;
  border-left-width: 0;
  border-right-color: #333;
  right: calc(0em - 15px);
  -webkit-transform: translate(.5em, -50%);
  transform: translate(.5em, -50%);
}
[tooltip][flow^="right"]::after {
  top: 65%;
  left: calc(100% + 15px);
  -webkit-transform: translate(.5em, -50%);
  transform: translate(.5em, -50%);
}
  
	/* KEYFRAMES */
	@-webkit-keyframes tooltips-vert {
	  to {
		opacity: .9;
		-webkit-transform: translate(-50%, 0);
		transform: translate(-50%, 0);
	  }
	}
  
	@-webkit-keyframes tooltips-horz {
	  to {
		opacity: .9;
		-webkit-transform: translate(0, -50%);
		transform: translate(0, -50%);
	  }
	}
  
	@keyframes tooltips-vert {
	  to {
		opacity: .9;
		transform: translate(-50%, 0);
	  }
	}
  
	@keyframes tooltips-horz {
	  to {
		opacity: .9;
		transform: translate(0, -50%);
	  }
	}
  
	[tooltip][flow^="right"]:hover::before,
	[tooltip][flow^="right"]:hover::after {
	  -webkit-animation: tooltips-horz 300ms ease-out forwards;
	  animation: tooltips-horz 300ms ease-out forwards;
	}
  </style>
