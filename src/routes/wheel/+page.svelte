<script>
  import { balance } from "../store";

  // Function to update balance
  const increaseBalance = () => {
    balance.update(n => n + 10);
  };
</script>

<div class="wheel-container">
<h1>Wheel</h1>
<div class="balance-container">
  <h2>Balance: <span class="balance">${$balance}</span></h2>
</div>
<button class="increase-button" onclick={increaseBalance}>Increase Balance</button>
</div>
