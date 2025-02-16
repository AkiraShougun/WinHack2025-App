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

<style>
  div {
    padding: 20px;
    border-radius: 20px;
  background-color: var(--light-background);
  box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.15); 
  }
</style>