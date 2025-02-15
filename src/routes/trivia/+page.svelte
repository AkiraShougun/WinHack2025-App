<link rel="stylesheet" href="/src/routes/css/main.css" />

<script>
    let questions = [
        { question: "What is the capital of France?", answer: "Paris" },
        { question: "What is 2 + 2?", answer: "4" },
        { question: "What is the largest planet in our solar system?", answer: "Jupiter" }
    ];
    let currentQuestionIndex = 0;
    let userAnswer = "";
    let showAnswer = false;

    function checkAnswer() {
        showAnswer = true;
    }

    function nextQuestion() {
        currentQuestionIndex = (currentQuestionIndex + 1) % questions.length;
        userAnswer = "";
        showAnswer = false;
    }
</script>

<main>
<div>
    <h2>{questions[currentQuestionIndex].question}</h2>
    <input type="text" bind:value={userAnswer} placeholder="Your answer" />
    <button on:click={checkAnswer}>Check Answer</button>
    {#if showAnswer}
        <p>{userAnswer === questions[currentQuestionIndex].answer ? "Correct!" : "Wrong!"}</p>
        <p>The correct answer is: {questions[currentQuestionIndex].answer}</p>
        <button on:click={nextQuestion}>Next Question</button>
    {/if}
</div>
</main>