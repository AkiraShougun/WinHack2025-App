<script>
    import { balance } from "./store";
</script>

<link rel="stylesheet" href="/src/routes/css/main.css" />


<header>
    <div class="header-container">
        <h1>The Ultimate Play & Earn Hub</h1>
        <p>Play games, earn points, and redeem rewards!</p>
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
    <p>&copy; 2025 WinHack2025-App. All Rights Reserved.</p>
</footer>
