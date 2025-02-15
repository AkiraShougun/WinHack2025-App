<script>
    import { balance } from "../store";
  
    // Function to update balance
    const increaseBalance = () => {
      balance.update(n => n + 10);
    };

    
  </script>

<h1>Wheel</h1>

<h1>Balance: {$balance}</h1>
<button on:click={increaseBalance}>Increase Balance</button>
