<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3 v-if="goalVisibility">{{ goal }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button @click="toggleGoalVisibility">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script>
// import { ref } from 'vue'
// import { reactive } from 'vue'
export default {
  //Options API:
  data() {
    return {
      goal: 'Finish course!',
      goalVisibility: false,
    };
  },
  methods: {
    toggleGoalVisibility() {
      this.goalVisibility = !this.goalVisibility;
    },
  },

  //Composition API
  // setup() {
  //   // const courseGoal = ref('Finish course!');
  //   // const goalIsVisible = ref(false);
  //   // const courseData = ref({
  //   //   goal: 'Finish course!',
  //   //   goalVisibility: false,
  //   // });
  //   const courseData = reactive({
  //     goal: 'finish course!',
  //     goalVisibility: false,
  //   });
  //   function toggleGoalVisibility() {
  //     // goalIsVisible.value = !goalIsVisible.value;
  //     // courseData.value.goalVisibility = !courseData.value.goalVisibility;
  //     courseData.goalVisibility = !courseData.goalVisibility;
  //   }
  //   return {
  //     // goal: courseData.value.goal,
  //     goal: courseData.goal,
  //     courseData: courseData,
  //     toggleGoalVisibility: toggleGoalVisibility,
  //   };
  // },
};
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>
