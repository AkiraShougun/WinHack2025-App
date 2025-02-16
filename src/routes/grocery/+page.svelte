<script>
    import Item from "../../components/item.svelte";
    import './main.css';
</script>

<link rel="stylesheet" href="/src/routes/css/main.css" />

<h1>Grocery List</h1>

<div class="grocery-list">
    <Item name="Apple" price="1.50" />  
    <Item name="Banana" price="2.00" />  
    <Item name="Onion" price="1.00" />  
    <Item name="Lettuce" price="5.00" />
    <Item name="Tomato" price="3.00" />
    <Item name="Potato" price="2.50" />
    <Item name="Carrot" price="2.00" />
    <Item name="Cucumber" price="1.50" />
    <Item name="Broccoli" price="3.00" />
</div>

<style>
    h1 {
        text-align: center;
        font: 3em sans-serif;
        color: purple;
    }
    div {
        padding: 200px;
        max-width: 800px;
        border-radius: 20px;
        background-color: var(--light-background);
        box-shadow: 0px 10px 30px rgba(0, 0, 0, 0.15);
    }
    .grocery-list {
        display: grid;
        grid-template-columns: auto auto auto;
        gap: 20px;
        padding: 20px;
    }
</style>