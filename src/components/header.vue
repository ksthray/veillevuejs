<template>
  <div id="header">
    <h1>{{title}}</h1>
  </div>
</template>
<script>
export default {
  name: "Header",
  props: ["title"],
};
</script>

<style>
#header {
  background: #ccc;
  display: flex;
  text-align: center;
  justify-content: center;
  padding: 20px;
}
</style>