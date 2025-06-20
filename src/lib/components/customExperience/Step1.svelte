<script>
  import ButtonSelection from "../reusableComponents/ButtonSelection.svelte";
  const { nextStep } = $props();

  const HEALTH = 0,
    STRESS = 1,
    PRODUCTIVITY = 2,
    GROWTH = 3,
    RELATIONSHIPS = 4,
    MONEY = 5,
    OTHER = 6;
    
</script>

<section>
  <h1>What's your main goal?</h1>

  <div class="flex flex-col items-center px-10 *:w-full">
    <ButtonSelection values={[
      { id: HEALTH, text: "Improve my health", icon: "/heart.svg" },
      { id: STRESS, text: "Reduce stress and improve mental wellbeing", icon: "/brain.svg" },
      { id: PRODUCTIVITY, text: "Be more productive", icon: "/clock.svg" },
      { id: GROWTH, text: "Personal growth", icon: "/hatGraduate.svg" },
      { id: RELATIONSHIPS, text: "Improve my relationships", icon: "/people.svg" },
      { id: MONEY, text: "Better manage my money", icon: "/wallet.svg" },
      { id: OTHER, text: "Other", icon: "/plus.svg" }
    ]} nextStep={nextStep} />
  </div>
</section>

