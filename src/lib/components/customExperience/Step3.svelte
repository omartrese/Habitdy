<script>
  import ButtonSelection from "../reusableComponents/ButtonSelection.svelte";

  const { nextStep } = $props();

  const MORNING = 0,
    AFTERNOON = 1,
    NIGHT = 2,
    DEPENDS = 3;

  let selected = $state(-1);
</script>

<section >
  <h1>When do you prefer to work on your habits?</h1>
  <ButtonSelection 
    values={[
      { id: MORNING, text: "In the morning", icon: "/sun.svg" },
      { id: AFTERNOON, text: "In the afternoon", icon: "/sunset.svg" },
      { id: NIGHT, text: "At night", icon: "/moon.svg" },
      { id: DEPENDS, text: "It depends on the day", icon: "/clock.svg" }
    ]}
    nextStep={nextStep}
  />
</section>

<style>
  h1 {
    margin-top: 0.5rem;
    margin-bottom: 0.25rem;
  }


</style>
