<script lang="ts">
  import { steps } from "$lib/StepData";

  const { currentStep } = $props();
</script>

<div>
  <div class="flex items-center justify-center *:p-2">
    {#each steps as step, index}
      <div class="flex items-center">
        <div
          class="w-8 h-8 rounded-full flex items-center justify-center mx-10 text-white font-bold {currentStep ==
          index
            ? 'bg-blue-500'
            : 'bg-gray-300'} {currentStep > index ? 'bg-green-500' : ''}"
        >
          {step}
        </div>
      </div>
    {/each}
  </div>
</div>
