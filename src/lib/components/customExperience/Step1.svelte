<script>
  import ButtonSelection from "../reusableComponents/ButtonSelection.svelte";
  const { nextStep } = $props();

  const values = $state([
    { id: 0, text: "Improve my health", icon: "/heart.svg", selected: false },
    { id: 1, text: "Reduce stress and improve mental wellbeing", icon: "/brain.svg", selected: false },
    { id: 2, text: "Be more productive", icon: "/clock.svg", selected: false },
    { id: 3, text: "Personal growth", icon: "/hatGraduate.svg", selected: false },
    { id: 4, text: "Improve my relationships", icon: "/people.svg", selected: false },
    { id: 5, text: "Better manage my money", icon: "/wallet.svg", selected: false },
    { id: 6, text: "Other", icon: "/plus.svg", selected: false }
  ]);
</script>

<section>
  <h1>What's your main goal?</h1>
  <div class="flex flex-col items-center px-10 *:w-full">
    <ButtonSelection {values} {nextStep} />
  </div>
</section>
