<script>
  let openIndex = null; // Index of currently opened item (null if none)

  const items = [
    { question: 'Question 1', answer: 'Answer 1' },
    { question: 'Question 2', answer: 'Answer 2' },
    { question: 'Question 3', answer: 'Answer 3' },
    { question: 'Question 4', answer: 'Answer 4' },
    { question: 'Question 5', answer: 'Answer 5' },
    { question: 'Question 6', answer: 'Answer 6' }
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
  <div class="item cursor-pointer p-3 border-white border-b"  on:keydown on:click={() => toggleItem(index)}>
    <h3 class="flex justify-between">{item.question}
    {#if openIndex === index}
    <span>Open</span>
    {:else}
    <span>Close</span>
    {/if}
    </h3>
    {#if openIndex === index}
      <p>{item.answer}</p>
    {/if}
  </div>
{/each}

<style>
  
  h3 {
    margin: 0;
  }
  p {
    margin: 0;
    padding: 10px 0;
  }
</style>