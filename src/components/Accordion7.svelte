<script>
  
    export let question_1 = 'question_1'
    export let question_2 = 'question_1'
    export let question_3 = 'question_1'
    export let question_4 = 'question_1'
    export let question_5 = "question_1";
    export let question_6 = "question_1";
    export let question_7 = "question_1";

    export let answer_1 = 'question_1'
    export let answer_2 = 'question_1'
    export let answer_3 = 'question_1'
    export let answer_4 = 'question_1'
    export let answer_5 = "question_1";
    export let answer_6 = "question_1";
    export let answer_7 = "question_1";

    let openIndex = null; // Index of currently opened item (null if none)
  
    const items = [
      { question: question_1, answer: answer_1 },
      { question: question_2, answer: answer_2 },
      { question: question_3, answer: answer_3 },
      { question: question_4, answer: answer_4 },
      { question: question_5, answer: answer_5 },
      { question: question_6, answer: answer_6 },
      { question: question_7, answer: answer_7 }
    ];
  
    function toggleItem(index) {
      if (openIndex === index) {
        openIndex = null;
      } else {
        openIndex = index;
      }
    }
  </script>
  
  {#each items as item, index}
    <div class="item cursor-pointer p-3 border-b " on:keydown on:click={() => toggleItem(index)}>
      <h3 class={`flex justify-between text-xl mx-2 ${openIndex === index ? 'font-semibold' : ''}`}>{item.question}
      {#if openIndex === index}
      <span class="w-36">
      <img src="/base/option_on.webp" alt="rainbow color showing on button">
      </span>
      {:else}
      <span class="w-36">
      <img src="/base/option_off.webp" alt="rainbow color showing on button">
    </span>
      {/if}
      </h3>
      {#if openIndex === index}
        <p class="mx-2 text-lg my-2">{item.answer}</p>
      {/if}
    </div>
  {/each}
  
  <style>
 .item {
  border-color : #d3d4d6
 }

 .item:last-child {
  border-bottom: none; /* Removes the bottom border from the last element */
}
  </style>