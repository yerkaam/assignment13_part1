
<template>
  <div class="timeline">
     <div v-for="(event, index) in sortedEvents" :key="index" class="event" @click="toggleDetails(index)">
       <h2>{{ event.title }}</h2>
       <h3>{{ event.date }}</h3>
       <p v-if="event.showDetails">{{ event.description }}</p>
     </div>
  </div>
 </template>
 
 <script>
 export default {
  props: {
     events: {
       type: Array,
       required: true
     }
  },
  data() {
     return {
       sortedEvents: []
     };
  },
  methods: {
     sortEvents() {
       this.sortedEvents = this.events.sort((a, b) => new Date(a.date) - new Date(b.date));
     },
     toggleDetails(index) {
       this.sortedEvents[index].showDetails = !this.sortedEvents[index].showDetails;
     }
  },
  mounted() {
     this.sortEvents();
     this.sortedEvents.forEach(event => {
       Vue.set(event, 'showDetails', false);
     });
  }
 };
 </script>
 
 <style scoped>
 .timeline {
   background-color:rgb(195, 209, 6);
   padding: 20px;
   margin: 20px;
   border-radius: 10px;
 }
 
 .event {
   background-color:rgb(29, 25, 155);
   padding: 20px;
   margin: 20px;
   border-radius: 10px;
   cursor: pointer;
   transition: transform 0.3s ease, box-shadow 0.3s ease;
 }
 
 .event:hover {
   transform: scale(1.05);
   box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
 }
 
 .event h2 {
   margin-bottom: 10px;
   color:aliceblue;
 }
 
 .event h3 {
   margin-bottom: 15px;
   color:rgb(50, 160, 66);
 }
 
 .event p {
   display: none;
   color:aliceblue;
 }
 
 .event:hover p {
   display: block;
 }
 </style>