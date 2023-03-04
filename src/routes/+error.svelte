<script>
    import { page } from '$app/stores';
    let colour = '/base/machines.webp';
	function handleMouseOver(e) {
		colour = '/base/move-machines.webp';
	}
	function handleMouseOut(e) {
		colour = '/base/machines.webp';
	}
	const onFocus =()=>isFocused=true;
	const onBlur =()=>isFocused=false;

  let fact = "Please, click on the image above to receive a random fact about software, computers or internet";

  function changeFact() {
    let randomNumber = Math.floor(Math.random() * 15) + 1;
    
    switch (randomNumber) {
      case 1: fact = "<b>Cunningham's Law</b> - the best way to get the right answer on the internet is not to ask a question; it's to post the wrong answer.";
      break;
      case 2: fact = "<b>Moore's Law</b> - This states that the number of transistors that can be placed on a microchip will double approximately every 18-24 months, leading to exponential growth in computing power and reduction in cost.";
      break;
      case 3: fact = "<b>Metcalfe's Law</b> - This law states that the value of a network is proportional to the square of the number of nodes in the network, meaning that the larger a network grows, the more valuable it becomes.";
      break;
      case 4: fact = "<b>Reed's Law</b> - This law states that the utility of large networks, particularly social networks, can grow exponentially with the size of the network due to the creation of diverse and valuable sub-groups.";
      break;
      case 5: fact = "<b>Zipf's Law</b> - This law states that in a large sample of data, a few items (such as words in a language, or websites on the internet) will occur much more frequently than the majority of the items.";
      break;
      case 6: fact = `<b>Parkinson's Law</b> - This states that "work expands to fill the time available for its completion." In other words, tasks will tend to take up as much time as is allotted for them, regardless of whether that amount of time is reasonable or not.`;
      break;
      case 7: fact = "<b>Dunbar's Number</b> - This is a theoretical limit to the number of stable social relationships that an individual can maintain, which is estimated to be around 150. This has implications for social networks and online communities, as users may struggle to keep up with a large number of connections.";
      break;
      case 8: fact = "<b>The Law of Diminishing Marginal Utility</b> - This law states that as the amount of a good or service increases, the marginal utility derived from each additional unit decreases. This can be applied to technology, where the excitement and usefulness of a new product may decrease over time as it becomes more ubiquitous.";
      break;
      case 9: fact = `<b>Amara's Law</b> - This law states that "we tend to overestimate the effect of a technology in the short run and underestimate the effect in the long run." This highlights the difficulty of predicting the long-term impact of new technologies.`;
      break;
      case 10: fact = "<b>The Law of Requisite Variety</b> - This law states that in any system, the degree of control exercised over the system is proportional to the number and diversity of the elements in the system. This has implications for the design and management of complex systems, such as those found in technology and the internet.";
      break;
      case 11: fact = "<b>The Law of Unintended Consequences</b> - This law states that actions of people—and especially of government—always have effects that are unanticipated or unintended. This can be seen in the ways that technology and the internet have had unintended consequences for privacy, security, and other aspects of society.";
      break;
      case 12: fact = "<b>The Law of Conservation of Complexity</b> - This law states that complexity cannot be destroyed, only transformed or moved elsewhere. This has implications for the design of technology systems, as efforts to simplify a system in one area may result in added complexity in another area.";
      break;
      case 13: fact = "<b>The Iron Law of Oligarchy</b> - This law states that in any organization, power will tend to become concentrated in the hands of a small group of people. This can be seen in the concentration of power and influence in the technology industry, where a few large companies dominate the market.";
      break;
      case 14: fact = "<b>The Network Effect</b> - This is the idea that the value of a product or service increases as more people use it. This is a key driver of the growth of many technology products and services, as the more people use them, the more valuable they become.";
      break;
      case 15: fact = "<b>The Halo Effect</b> - This is the phenomenon where the perception of one aspect of a product or service affects the perception of other aspects. This can be seen in the way that the popularity and reputation of a technology brand can affect people's perceptions of the quality and value of their products and services.";
      break;
    }

  }

  </script>

  <div class="pb-10">
  <h1 class="text-center text-3xl mb-3 mx-5">
    <b>
      
    ERROR_NUM: {$page.status} 
  </b>
  <p class="text-center text-2xl mx-5 mt-2">Sorry, there seems to be a problem with our servers, you're internet or both.</p>
  <span class="flex justify-center">
  <img on:click={changeFact} on:mouseover={handleMouseOver} on:mouseout={handleMouseOut} on:keydown={onBlur} on:blur={onBlur} on:focus={onFocus} class="my-16 h-28 sm:h-48 md:h-64 hover:scale-105 transition active:scale-95" src={colour} alt="">
</span>
  

<p class="text-center text-2xl mx-5 mt-2 sm:mx-20 mx-32"> 
  {@html fact}
  <!-- <b>Cunningham's Law</b> - the best way to get the right answer on the internet is not to ask a question; it's to post the wrong answer.</p> -->


</div>