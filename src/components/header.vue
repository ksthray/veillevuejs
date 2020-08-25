<template>
  <div id="header">
    <h1>{{title}}</h1>
    <p>{{desc}}</p>
  </div>
</template>
<script>
export default {
  name: "Header",
  props: ["title", "desc"],
};
</script>

<style>
#header {
  background: #ccc;
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  padding: 20px;
}
</style>