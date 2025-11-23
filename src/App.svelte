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
  <div class="result-summary-contents">
    <ResultCard />
    <SummaryCard />
  </div>
</section>

<!-- Define styles Of App Component -->
<style>
  .result-summary-component {
    max-width: 64rem;
    margin: 12.8rem auto;
    padding: 0 3.2rem;
  }

  .result-summary-contents {
    background-color: hsl(0, 0%, 100%);
    display: grid;
    grid-template-columns: 1fr 1fr;
    border-radius: 3.2rem;
    overflow: hidden;
  }

  @media (max-width: 620px) {
    .result-summary-component {
      max-width: 32rem;
      padding: 0rem;
    }
    .result-summary-contents {
      grid-template-columns: 1fr;
    }
  }
</style>
