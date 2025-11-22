<!--------------------------->
<!-- Result Card Component -->
<!--------------------------->

<!-- Define structure Of Result Card Component -->
<div class="result-card">
  <h2 class="result-title">Your Result</h2>

  <div class="final-score-wrapper">
    <p class="final-score">76</p>
    <span class="max-score"> of 100</span>
  </div>

  <div class="comment-wrapper">
    <h3 class="comment-title">Great</h3>
    <p class="comment-description">
      You scored higher than 65% of the people who have taken these tests.
    </p>
  </div>
</div>

<!-- Define styles Of Result Card Component -->
<style>
  .result-card {
    background: linear-gradient(hsl(252, 100%, 67%), hsla(256, 72%, 46%, 1));
    color: hsl(241, 100%, 89%);
    padding: 3.2rem;
    border-radius: 2rem;
    text-align: center;
  }

  .result-title {
    font-size: 2rem;
    font-weight: 600;
    margin-bottom: 3.6rem;
    letter-spacing: 0.5px;
  }

  .final-score-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: linear-gradient(
      hsla(256, 72%, 46%, 1),
      hsla(256, 72%, 46%, 0.5)
    );
    margin: 0 auto;
    width: 65%;
    padding: 4rem 3.2rem;
    border-radius: 75%;
    margin-bottom: 4rem;
    box-shadow: 0 4rem 4rem hsla(256, 72%, 46%, 0.5);
  }

  .final-score {
    font-size: 4.9rem;
    font-weight: 700;
    color: hsl(0, 0%, 100%);
  }

  .max-score {
    margin-top: -0.4rem;
    font-size: 1.4rem;
  }

  .comment-wrapper {
    padding: 0 2rem;
  }

  .comment-title {
    font-size: 2.5rem;
    color: hsl(0, 0%, 100%);
    margin-bottom: 1.2rem;
  }

  .comment-description {
    line-height: 1.5;
  }
</style>
