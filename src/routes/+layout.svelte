<link rel="stylesheet" href="src/routes/main.css">

<script>
    import { balance } from "./store";
</script>

<main>
    <nav>Balance: {$balance}</nav>
    <slot />
</main>

