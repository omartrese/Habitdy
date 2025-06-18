<script>
  const { nextStep } = $props();
</script>

<section>
  <h1>What style do you prefer?</h1>
  <p class="subtitle">Customize your experience with the style that motivates you the most.</p>
  <div class="flex flex-col items-center px-10 *:w-full gap-3">
    <button onclick={nextStep}>
      <span class="icon">✚</span> Minimalist and direct
    </button>
    <button onclick={nextStep}>
      Motivational with daily quotes
    </button>
    <button onclick={nextStep}>
      <span class="icon">📊</span> Focused on statistics and progress
    </button>
  </div>
  <button class="finish" disabled>Finish</button>
</section>

<style>
  h1 {
    margin-top: 0.5rem;
    margin-bottom: 0.25rem;
  }
  .subtitle {
    color: #6b7280;
    margin-bottom: 1.5rem;
  }
  button {
    background-color: #fff;
    color: #111827;
    border: 1px solid #e5e7eb;
    padding: 14px 20px;
    border-radius: 8px;
    cursor: pointer;
    margin: 0.25rem 0;
    font-size: 1rem;
    font-weight: 500;
    text-align: left;
    display: flex;
    align-items: center;
    gap: 0.75rem;
    transition: background 0.15s;
  }
  button:hover:not(:disabled) {
    background-color: #f3f4f6;
  }
  .icon {
    font-size: 1.3em;
    width: 1.5em;
    display: inline-block;
    text-align: center;
  }
  .finish {
    background: #f3f4f6;
    color: #9ca3af;
    border: none;
    margin-top: 2rem;
    width: 100%;
    cursor: not-allowed;
  }
</style>
