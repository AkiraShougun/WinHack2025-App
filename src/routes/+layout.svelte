<script>
    import { balance } from "./store";
</script>

<link rel="stylesheet" href="/src/css/main.css" />

<header>
    <div class="header-container">
        <h1 class="header-title">The Ultimate Play & Earn Hub</h1>
        <p class="header-subtitle">Play games, earn points, and redeem rewards!</p>
        <nav>
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/grocery">Grocery</a></li>
                <li><a href="/trivia">Trivia</a></li>
                <li><a href="/wheel">Wheel</a></li>
            </ul>
        </nav>
        <div class="balance-display">
            <span>Balance: <strong>{$balance}</strong></span>
        </div>
    </div>
</header>

<main>
    <slot />
</main>

<footer>
    <div>
        <p>Made with <span style="color: red;">&#10084;</span> by: Diaa Al Saleh, Hia Al Saleh, Piotr Ciastek, Joanne Hou</p>
    </div>
</footer>
