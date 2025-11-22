<!-------------------------->
<!-- Define App Component -->
<!-------------------------->

<script>
  // Import Necesarry Component
  import ResultCard from "./ResultCard.svelte";
  import SummaryCard from "./SummaryCard.svelte";
</script>

<!-- Define Structure Of App Component -->
<section class="result-summary-component">
  <ResultCard />
  <SummaryCard />
</section>

<!-- Define styles Of App Component -->
<style>
  .result-summary-component {
    max-width: 64rem;
    margin: 9.6rem auto;
    background-color: hsl(0, 0%, 100%);
    display: grid;
    grid-template-columns: 1fr 1fr;
    border-radius: 2.4rem;
    overflow: hidden;
  }
</style>
