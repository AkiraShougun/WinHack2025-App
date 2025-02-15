<script>
    import { balance } from "./store";
</script>

<header>
    <h1>Welcome to SvelteKit</h1>
    <nav>
        <span class="balance">Balance: {$balance}</span>
        <a href="/">Home</a>
        <a href="/grocery">Grocery</a>
        <a href="/trivia">Trivia</a>
        <a href="/wheel">Wheel</a>
    </nav>
</header>

<main>
    <slot />
</main>

<footer>
    <p>&copy; 2025 WinHack2025-App. All Rights Reserved.</p>
</footer>
