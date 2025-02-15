<script lang="ts">
    import { balance } from "../routes/store";
  
    let {name,price} = $props();
  const Buy = () => {
    balance.update(n => n - price);
  };

</script>

<div>
    <h1>{name}</h1>
    <p>{price}</p>
    <button onclick={Buy}>Buy</button>
</div>