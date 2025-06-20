<script>
  const { nextStep } = $props();
  // You may want to handle selected checkboxes here
  // let selected = [];
</script>

<section>
  <h1>Which habits would you like to build?</h1>
  <form
    class="flex flex-col gap-6 px-10 *:w-full"
    onsubmit={(event) => {
      event.preventDefault();
      // Handle form submission, e.g., collect selected habits
      nextStep(); // Proceed to the next step
    }}
  >
    <fieldset>
      <legend>Physical Health</legend>
      <label
        ><input type="checkbox" name="habit" value="exercise" /> Exercise regularly</label
      >
      <label
        ><input type="checkbox" name="habit" value="drink_water" /> Drink more water</label
      >
      <label
        ><input type="checkbox" name="habit" value="sleep" /> Sleep 7-8 hours every
        night</label
      >
      <label
        ><input type="checkbox" name="habit" value="eat_fruits_veggies" /> Eat more
        fruits and vegetables</label
      >
      <label
        ><input type="checkbox" name="habit" value="reduce_sugar" /> Reduce sugar
        intake</label
      >
    </fieldset>
    <fieldset>
      <legend>Mental Wellbeing</legend>
      <label
        ><input type="checkbox" name="habit" value="meditate" /> Meditate or practice
        mindfulness</label
      >
      <label
        ><input type="checkbox" name="habit" value="journaling" /> Journal (writing
        daily)</label
      >
      <label
        ><input type="checkbox" name="habit" value="reduce_social_media" /> Reduce
        time on social media</label
      >
      <label
        ><input type="checkbox" name="habit" value="breathing_breaks" /> Take breathing
        breaks during the day</label
      >
    </fieldset>
    <fieldset>
      <legend>📈 Productivity & Focus</legend>
      <label
        ><input type="checkbox" name="habit" value="plan_day" /> Plan the day in
        the morning</label
      >
      <label
        ><input type="checkbox" name="habit" value="read" /> Read 10 minutes a day</label
      >
      <label
        ><input type="checkbox" name="habit" value="wake_up_early" /> Wake up early</label
      >
      <label
        ><input type="checkbox" name="habit" value="no_multitasking" /> Avoid multitasking
        (one task at a time)</label
      >
    </fieldset>
    <fieldset>
      <legend>🌱 Personal Growth</legend>
      <label
        ><input type="checkbox" name="habit" value="learn_new" /> Learn something
        new every day</label
      >
      <label
        ><input type="checkbox" name="habit" value="gratitude" /> Practice gratitude</label
      >
      <label
        ><input type="checkbox" name="habit" value="listen_podcasts" /> Listen to
        educational podcasts</label
      >
      <label
        ><input type="checkbox" name="habit" value="study_language" /> Study a language
        15 minutes a day</label
      >
    </fieldset>
    <fieldset>
      <legend>👥 Relationships & Connection</legend>
      <label
        ><input type="checkbox" name="habit" value="call_loved_one" /> Call a loved
        one every week</label
      >
      <label>
        <input type="checkbox" name="habit" value="family_time" /> Spend screen-free
        time with family</label
      >
      <label>
        <input type="checkbox" name="habit" value="act_of_kindness" /> Do a daily
        act of kindness</label
      >
    </fieldset>
    <button type="submit">Next</button>
  </form>
</section>

<style>
  form {
    margin-top: 1rem;
  }
  fieldset {
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    padding: 1rem;
  }
  legend {
    font-weight: bold;
    margin-bottom: 0.5rem;
  }
  label {
    display: flex;
    align-items: center;
    margin-bottom: 0.5rem;
    gap: 0.5rem;
    font-size: 1rem;
  }
  button[type="submit"] {
    background-color: #3b82f6;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    margin-top: 1rem;
  }
</style>
