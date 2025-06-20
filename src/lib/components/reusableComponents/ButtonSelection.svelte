<script lang="ts">

  const { values, nextStep } = $props();

  let canContinue: boolean = $state(false);
</script>

<div>
  <div class="flex flex-col justify-center items-center">
    {#each values as item}
      <button class="" onclick={() => canContinue = true}>
        <img src={item.icon} alt="icon" />
        {item.text}
      </button>
    {/each}
    <button disabled={!canContinue} onclick={nextStep}>
        Continue
    </button>
  </div>

  

</div>

<style>
  button {
    background-color: #3b82f6;
    color: white;
    cursor: pointer;
    transition-duration: 0.3s;
    width: 60%;
    max-width: 640px;

    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 10px 20px;
    margin-block: 1em;
  }
  button:disabled {
    background-color: #e5e7eb;
    color: #f3f4f6;
    cursor: not-allowed;
  }

  @media (max-width: 640px) {
    button {
      width: 100%;
    }
  }
</style>
