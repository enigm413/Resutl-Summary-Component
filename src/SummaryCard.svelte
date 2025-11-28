<!---------------------------->
<!-- Summary Card Component -->
<!---------------------------->

<script>
  // Define the Necessary Component
  import SummaryItem from "./SummaryItem.svelte";

  // Define the function to Fetch Data
  async function fetchData() {
    const response = await fetch("./assets/data.json");
    const data = await response.json();
    return data;
  }
</script>

<!-- Define Structure Of Summary Card Component -->
<div class="summary-card">
  <h2 class="summary-title">Summary</h2>
  <ul class="summary-list">
    <!-- Await Block To Asynchronous Code -->
    {#await fetchData() then summaryList}
      <!--Each Block to Iterate Summary Item  -->
      {#each summaryList as summaryItem (summaryItem.category)}
        <SummaryItem {...summaryItem} />
      {/each}
    {/await}
  </ul>

  <button class="btn">Continue</button>
</div>

<!-- Define styles Of Summary Card Component -->
<style>
  .summary-card {
    padding: 3.6rem 2.8rem;
  }

  .summary-title {
    font-size: 2rem;
    font-weight: 700;
    color: hsl(224, 30%, 27%);
    letter-spacing: 0.5px;
    margin-bottom: 2.4rem;
  }

  .summary-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 2rem;
    margin-bottom: 2.8rem;
  }

  .btn {
    background-color: hsl(224, 30%, 27%);
    color: hsl(0, 0%, 100%);
    padding: 1.2rem 2.4rem;
    width: 100%;
    border-radius: 2rem;
    font-weight: 500;
    font-size: 1.4rem;
    letter-spacing: 0.9px;
    cursor: pointer;
    border: none;
  }

  .btn:hover {
    background-color: hsla(256, 72%, 46%, 1);
    color: hsl(0, 0%, 100%);
  }
</style>
