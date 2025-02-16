<script>
    import {goto} from '$app/navigation';
</script>

<div>
    <div class="features">
        <h2 class="section-title">Explore Our Features</h2>
            <button onclick={() => goto('/grocery')}>Grocery</button>
            <button onclick={() => goto('/trivia')}>Trivia</button>
            <button onclick={() => goto('/wheel')}>Wheel</button>
    </div>
</div>