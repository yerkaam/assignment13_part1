<template>
  <div id="app">
    <Timeline :events="events" />
  </div>
</template>

<script>
import Timeline from "/Users/eraorynbaigmail.com/Desktop/assignment13/part1/src/Timeline.vue";

export default {
  name: "App",
  components: {
    Timeline,
  },
  data() {
    return {
      events: [
        {
          id: 1,
          title: "Event 1",
          date: "2023-01-01",
          description: "The concept of timelines transcends mere functionality; it is a visual storytelling device that allows us to comprehend the past, grasp the present, and envision the future. Our timeline component is more than a sequence of events; it is a canvas where history unfolds, projects evolve, and stories are told with elegance and precision.",
        },
        {
          id: 2,
          title: "Event 2",
          date: "2023-02-15",
          description: "Navigating through time should be intuitive, and our Vue.js timeline ensures just that. Each event is equipped with essential details – from dates to titles and comprehensive descriptions – facilitating a seamless journey through the narrative. The modular structure of the component allows for easy customization, aligning it with the unique aesthetics of diverse projects.",
        },
        {
          id: 3,
          title: "Event 3",
          date: "2023-02-18",
          description: "Navigating through time should be intuitive, and our Vue.js timeline ensures just that. Each event is equipped with essential details – from dates to titles and comprehensive descriptions – facilitating a seamless journey through the narrative. The modular structure of the component allows for easy customization, aligning it with the unique aesthetics of diverse projects.",
        },
        {
          id: 4,
          title: "Event 2",
          date: "2023-02-26",
          description: "As we embrace the significance of chronology, our Vue.js timeline component stands as a testament to the power of effective event representation, ensuring that every moment is not just remembered but celebrated in the grand tapestry of time.",
        },
      ],
    };
  },
};
</script>

<style>
#app {
  text-align: center;
  padding: 10px;
}
</style>