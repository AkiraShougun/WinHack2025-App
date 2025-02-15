<script>
    import { balance } from "../store";
    const increaseBalance = () => {
      balance.update(n => n + 10);
    };

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

<h1>Wheel</h1>

<h1>Balance: {$balance}</h1>
<button onclick={increaseBalance}>Increase Balance</button>

<h1>Spin the wheel</h1>
<button onclick={Spin}>Spin</button>
<p>{message}</p>
