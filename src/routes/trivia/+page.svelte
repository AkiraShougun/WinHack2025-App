<script>
    import questions from "../../questionbank.json"
    import { balance } from "../store";
    let currentQuestionIndex = 0;
    let userAnswer = "";
    let showAnswer = false;

    const increaseBalance = () => {
      balance.update(n => n + 10);
    };

    function checkAnswer() {
        showAnswer = true;
        if (userAnswer === questions[currentQuestionIndex].answer) {
            increaseBalance();
        }
    }

    function nextQuestion() {
        currentQuestionIndex = (currentQuestionIndex + 1) % questions.length;
        userAnswer = "";
        showAnswer = false;
    }
</script>

<div class="quiz-container">
    <h2>{questions[currentQuestionIndex].question}</h2>
    
    <input type="text" bind:value={userAnswer} placeholder="Your answer" />
    
    <button on:click={checkAnswer}>Check Answer</button>

    {#if showAnswer}
        <p class="{userAnswer === questions[currentQuestionIndex].answer ? 'correct' : 'wrong'}">
            {userAnswer === questions[currentQuestionIndex].answer ? "Correct!" : "Wrong!"}
        </p>
        <p>The correct answer is: {questions[currentQuestionIndex].answer}</p>
        <button on:click={nextQuestion}>Next Question</button>
    {/if}
</div>