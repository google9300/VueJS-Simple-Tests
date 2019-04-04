<template>
  <div class="hello">
    <p :class="{active: isActive}">Name</p>
    <p>{{isActive ? 'Active' : 'Not Active'}}</p>
    <button :class="{active: isActive}" @click="isActive=!isActive">CLICK ME</button>
    <br>
    <p :class="{active: isActive}" v-if="visible">First Paragraph</p>
    <p :class="{active: isActive}">Secound Paragraph</p>
    <button v-on:click="visible=!visible">{{visible?'Hide':'Show'}}</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data: function() {
    return { isActive: false, visible: false };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p {
  background-color: black;
  color: white;
}
p.active {
  background-color: yellowgreen;
  color: red;
}
</style>
