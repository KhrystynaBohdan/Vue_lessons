<template>
<div class="backdrop">
<div class="modal">
  <p>modal content</p>
</div>
</div>
</template>

<script>
export default {
  name: "Modal"
};
</script>

<style scoped>
.modal{
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: aliceblue;
  border-radius: 20px;

}
.backdrop{
  top: 0;
  position: fixed;
  background: aquamarine;
  width: 100%;
  height: 100%;
}
</style>
