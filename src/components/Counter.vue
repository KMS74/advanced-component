<template>
  <div class="container quote">
    <h2 class="mb-4">{{ counter }}</h2>
    <button class="btn btn-success mr-4" @click="counter++">increase counter</button>
    <button class="btn btn-danger mr-4" @click="counter--">increase counter</button>
    <button class="btn btn-light" @click="counter=0">reset counter</button>


  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0,
    };
  },
  // dynamic component lifecycle hooks
  activated() {
    console.log("Counter Component Activated");
  },
  deactivated() {
    console.log("Counter Component Deacrivated");
  },
};
</script>

<style>
</style>