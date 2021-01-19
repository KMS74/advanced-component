<template>
  <div class="container quote">
    <slot name="title"></slot>
    <hr id="sperator" />
    <slot name="text"> </slot>
  </div>
</template>

<script>
export default {
  // dynamic component lifecycle hooks
  activated() {
    console.log("Quote Component Activated");
  },
  deactivated() {
    console.log("Quote Component Deacrivated");
  },
};
</script>

<style >
.quote {
  background-color: #f1f1f1;
  padding: 40px 20px;
  text-align: center;
  margin-top: 40px;
  margin-bottom: 40px ;
  box-shadow: 1px 1px 2px #ccc;
  border: 1px solid #ddd;
  border-radius: 10px;
}
.quote h1 {
  color: #007bff;
  font-weight: bold;
  margin: 15px 0;
}
.quote p {
  font-size: 1.2rem;
  font-style: italic;
}
#sperator {
  width: 50%;
  color: #343a40;
  border: 0.5px solid #343a40;
}
</style>