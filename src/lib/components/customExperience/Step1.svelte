<script>
  const { nextStep } = $props();
</script>

<section>
  <h1>What's your main goal?</h1>

  <div class="flex flex-col items-center px-10 *:w-full">
    <button onclick={nextStep}>Improve my health</button>
    <button onclick={nextStep}>
        Reduce stress and improve mental wellbeing
    </button>
    <button onclick={nextStep}>Be more productive</button>
    <button onclick={nextStep}>Personal growth</button>
    <button onclick={nextStep}>Improve my relationships</button>
    <button onclick={nextStep}>Better manage my money</button>
    <button onclick={nextStep}>Other</button>
  </div>
</section>

<style>
  button {
    background-color: #3b82f6;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    margin: 5px;
  }
</style>
