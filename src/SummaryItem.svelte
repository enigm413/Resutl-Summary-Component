<!--------------------------->
<!--Summary Item Component -->
<!--------------------------->

<script>
  // Define the props
  const { icon, category, score } = $props();
</script>

<!-- Define the structure of summary item component -->
<li class="summary-item item--{category.toLowerCase()}">
  <div class="item-title-wrapper">
    <img src={icon} alt="Reaction Icon" class="summary-icon" />
    <p class="item-title">{category}</p>
  </div>
  <p class="item-score">
    <span class="score-value">{score}</span> / 100
  </p>
</li>

<!-- Define styles Of Summary Item Component -->
<style>
  .summary-item {
    border-radius: 0.8rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1.2rem 2rem;
  }

  .item--reaction {
    background-color: hsla(0, 100%, 67%, 0.07);
    color: hsl(0, 100%, 67%);
  }

  .item--memory {
    background-color: hsla(39, 100%, 56%, 0.07);
    color: hsl(39, 100%, 56%);
  }

  .item--verbal {
    background-color: hsla(166, 100%, 37%, 0.07);
    color: hsl(166, 100%, 37%);
  }

  .item--visual {
    background-color: hsla(234, 85%, 45%, 0.07);
    color: hsl(234, 85%, 45%);
  }

  .item-title-wrapper {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.8rem;
  }

  .item-title {
    font-weight: 600;
    letter-spacing: 0.3px;
  }

  .item-score {
    color: hsla(0, 100%, 67%, 0.5);
    font-weight: 600;
  }

  .score-value {
    color: hsl(224, 30%, 27%);
    font-weight: 700;
  }
</style>
