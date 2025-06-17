<script>
  import "../app.css";

  import { steps } from "$lib/StepData";
  import StepIndicator from "../lib/components/customExperience/StepIndicator.svelte";
  import Step1 from "$lib/components/customExperience/Step1.svelte";

  let currentStep = $state(0);

  const nextStep = () => {
    currentStep += 1;
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
    <Step1 {nextStep} />
  </section>
</main>
