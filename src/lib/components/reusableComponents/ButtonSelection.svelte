<script lang="ts">
  const { values, nextStep } = $props();

  let canContinue: boolean = $state(false);

  const toggleSelection = (item: any) => {
    item.selected = !item.selected;
    canContinue = values.some((value: any) => value.selected);
  };
</script>

<div>
  <div class="flex flex-col justify-center items-center">
    {#each values as item}
      <button
        class={item.selected ? "selected option" : "option"}
        onclick={() => toggleSelection(item)}
      >
        <span>
          <img src={item.icon} alt="icon" />
        </span>

        <span class="">{item.text}</span>
      </button>
    {/each}
    <button class="continue" disabled={!canContinue} onclick={nextStep}
      >Continue</button
    >
  </div>
</div>

<style>
  button {
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

  button.option {
    background-color: white;
    color: #111827;
    border: 1px solid #e5e7eb;
    border-radius: 16px;
    font-size: 1rem;
    font-weight: 500;
  }

  button.selected {
    background-color: #3b82f6;
    color: white;
    border-color: #2563eb;
  }

  button.continue {
    background-color: #22c55e;
    color: white;
  }

  button.continue:disabled {
    background-color: #f3f4f6;
    color: #9ca3af;
    cursor: not-allowed;
  }

  @media (max-width: 640px) {
    button {
      width: 100%;
    }
  }
</style>
