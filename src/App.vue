<template>
  <div class="col-12">
    <div class="container">
      <button
        @click="selectedComponent = 'quoteApp'"
        class="btn btn-primary m-4"
      >
        Quote Component
      </button>
      <button
        @click="selectedComponent = 'counter'"
        class="btn btn-primary m-4"
      >
        Counter Component
      </button>
    </div>
    <keep-alive>
      <component :is="selectedComponent">
        <h1 slot="title">{{ quoteTitle }}</h1>
        <p slot="text">
          "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Recusandae
          quo, laboriosam nobis, non repellat quasi incidunt possimus veritatis
          vel, delectus atque repudiandae reiciendis eum magnam sequi
          consectetur ullam reprehenderit fuga"
        </p>
      </component>
    </keep-alive>
  </div>
</template>

<script>
import Quote from "./components/Quote.vue";
import Counter from "./components/Counter.vue";
export default {
  data() {
    return {
      quoteTitle: "Quote Title",
      selectedComponent: "quoteApp",
    };
  },
  components: {
    quoteApp: Quote,
    counter: Counter,
  },
};
</script>

<style>
</style>