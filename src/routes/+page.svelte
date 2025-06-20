<script>
  import StepIndicator from "../lib/components/customExperience/StepIndicator.svelte";
  import Step1 from "$lib/components/customExperience/Step1.svelte";
  import Step2 from "$lib/components/customExperience/Step2.svelte";
  import Step3 from "$lib/components/customExperience/Step3.svelte";
  import Step4 from "$lib/components/customExperience/Step4.svelte";

  let currentStep = $state(0);

  const nextStep = () => {
    currentStep += 1;
  };

  const previousStep = () => {
    if (currentStep > 0) {
      currentStep -= 1;
    }
  };
</script>

<main>
  <header>
    <StepIndicator {currentStep} />

    <div>
      <h1>Welcome to Habitdy!</h1>
      <p>
        Let's start creating your custom user experience and the Habits you want
        to track.
      </p>
    </div>
  </header>

  <section>
    {#if currentStep === 0}
      <Step1 {nextStep} />
    {:else if currentStep === 1}
      <Step2 {nextStep} />
    {:else if currentStep === 2}
      <Step3 {nextStep} />
    {:else if currentStep === 3}
      <Step4 {nextStep} />
    {/if}
  </section>
</main>

<style>
  :global(body) {
    user-select: none;
  }
</style>
