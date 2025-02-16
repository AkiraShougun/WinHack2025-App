<script>
    import { goto } from '$app/navigation';
</script>

<div class="features">
    <h2 class="section-title">Explore Our Features</h2>
    <div class="features-list">
        <button onclick={() => goto('/grocery')}>Grocery</button>
        <button onclick={() => goto('/trivia')}>Trivia</button>
        <button onclick={() => goto('/wheel')}>Wheel</button>
    </div>
</div>

<style>
    :root {
        --font-size-xl: 2em;
        --border-radius: 10px;
    }

    /* Features Section */
    .features {
        text-align: center;
        margin-top: 40px;
    }

    .features h2 {
        color: var(--primary-color);
        font-size: var(--font-size-xl);
        margin-bottom: 30px;
    }

    .features-list {
        max-width: 960px;
        margin: 80px auto;
        padding: 50px 40px;
        border-radius: 20px;
        background-color: var(--light-background);
        border: 1px solid #e0e0e0;
        box-shadow: 0px 12px 40px rgba(0, 0, 0, 0.1); 
        overflow: hidden;
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .features-list button {
        background: #f9f9f9;
        padding: 30px;
        font-size: 1.8em; 
        border-radius: var(--border-radius);
        box-shadow: 0px 6px 20px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease, box-shadow 0.3s ease, background-color 0.3s ease;
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        border: 1px solid #ddd;
        background-color: #65218a;
    }

    .features-list button:hover {
        transform: translateY(-8px);
        box-shadow: 0px 15px 40px rgba(0, 0, 0, 0.15); 
        background-color: #f8abf3;
    }

    .features-list button:focus {
        outline: none;
    }
</style>