<template>
  <button class="custombtn">{{ text }}</button>
</template>

<script>
export default {
  name: "CustomButton",
  props: {
    text: String
  }
}
</script>

<style scoped>
  .custombtn {
    border: 1px solid black;
    border-radius: 3px;
    cursor: pointer;
  }
</style>