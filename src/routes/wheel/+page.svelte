<script>
  import { balance } from "../store";

  let message = "";

  const Spin = () => {
    const random = Math.floor(Math.random() * 100);
    if (random < 10) {
      balance.update(n => n + 100);
      message = "You won 100";
    } else if (random < 30) {
      balance.update(n => n + 50);
      message = "You won 50";
    } else if (random < 60) {
      balance.update(n => n + 20);
      message = "You won 20";
    } else {
      balance.update(n => 0);
      message = "You lost everything!";
    }
  };
</script>
<div>
<h1 class="page-title">Wheel</h1>
  <img src="/200w.gif" alt="Wheel" class="wheel-image" />
  <h1 class="section-title">Spin the wheel</h1>
  <button class="spin-button" on:click={Spin}>Spin</button>
  <p class="result-message">{message}</p>
</div>

<style>
  .wheel-image {
    width: 200px;
    height: 200px;
    margin: 20px;
  }
  div {
    font-size: larger;
    color: blueviolet;
    padding: 200px;
    max-width: 800px;
    border-radius: 20px;
    background-color: var(--light-background);
    box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.15);
    margin: 0 auto; /* Center horizontally */
    text-align: center; /* Center text and inline elements */
  }
</style>