<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <font-awesome-icon icon="plus" /> Add Appointment
    <div v-for="apt in appointments" v-bind:key="apt">
          <h3>{{apt.petName}}</h3>
          <p>{{apt.aptNotes}}</p>
    </div>
  </div>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
export default {
  name: "App",
  data: function () {
    return {
      title: "Appointments List",
      appointments: [
        {
          petName: "Spot",
          petOwner: "Constance Smith",
          aptDate: "2017-07-24 08:30",
          aptNotes: "This German Shepherd is having some back pain",
        },
        {
          petName: "Goldie",
          petOwner: "Barot Bellingham",
          aptDate: "2017-07-22 15:50",
          aptNotes: "This Goldfish has some weird spots in the belly",
        },
        {
          petName: "Mitten",
          petOwner: "Hillary Goldwyn",
          aptDate: "2017-07-21 9:15",
          aptNotes: "Cat has excessive hairballs",
        },
        {
          petName: "Buffy",
          petOwner: "Hassum Harrod",
          aptDate: "2017-07-20 15:30",
          aptNotes:
            "This Chihuahua has not eaten for three days and is lethargic",
        },
      ],
    };
  },
  components: {
    FontAwesomeIcon,
  },
};
</script>
