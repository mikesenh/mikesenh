<script>
  import DisplayProjectSlide from "../../components/DisplayProjectSlide.svelte";
  import { Splide, SplideSlide } from '@splidejs/svelte-splide';
  
</script>

<Splide options={ { rewind: true } } aria-label="Svelte Splide Example">
  <SplideSlide>
    <img src="image1.jpg" alt="Image 1"/>
  </SplideSlide>
  <SplideSlide>
    <img src="image2.jpg" alt="Image 2"/>
  </SplideSlide>
</Splide>
        
        

<style>

</style>
