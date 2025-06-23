<script>
  import ButtonSelection from "../reusableComponents/ButtonSelection.svelte";
  const { nextStep } = $props();

  const values = $state([
    { id: 0, text: "Morning", icon: "/morning.svg", selected: false },
    { id: 1, text: "Afternoon", icon: "/afternoon.svg", selected: false },
    { id: 2, text: "Night", icon: "/night.svg", selected: false },
    { id: 3, text: "Anytime", icon: "/clock.svg", selected: false },
  ]);

  let prevId = $state(-1);

  $effect(() => {
    // Si la última opción se selecciona, deselecciona las otras
    if (values[3].selected) {
      values.forEach((item, index) => { if (index !== 3) item.selected = false; });
      prevId = 3;
    }
    // Si la última estaba seleccionada y ahora no, y alguna otra se selecciona, deselecciona la última
    if (prevId === 3 && values.slice(0, 3).some(item => item.selected)) {
      values[3].selected = false;
    }
    // Si las tres primeras están seleccionadas, selecciona solo la última y deselecciona las demás
    if (values.slice(0, 3).every(item => item.selected)) {
      values.forEach((item, index) => item.selected = (index === 3));
      prevId = 3;
    }
  });

</script>

<section>
  <h1>What's your main goal?</h1>
  <div class="flex flex-col items-center px-10 *:w-full">
    <ButtonSelection {values} {nextStep} />
  </div>
</section>
