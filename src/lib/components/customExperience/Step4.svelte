<script>
  import ButtonSelection from "../reusableComponents/ButtonSelection.svelte";
  const { nextStep } = $props();

  const values = $state([
    {
      id: 0,
      text: "Minimalist and direct",
      icon: "/minimalist.svg",
      selected: false,
    },
    {
      id: 1,
      text: "Motivational with daily quotes",
      icon: "/motivational.svg",
      selected: false,
    },
    {
      id: 2,
      text: "Focused on statistics and progress",
      icon: "/statistics.svg",
      selected: false,
    },
  ]);

</script>

<section>
  <h1>Which style do you prefer?</h1>
  <div class="flex flex-col items-center px-10 *:w-full">
    <ButtonSelection {values} {nextStep} />
  </div>
</section>
