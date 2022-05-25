<template>
  <span>Suche nach ID:</span>
  <input type="text" v-model="inputId">
  <CustomButton text="Suche" @click="searchForId(inputId)"></CustomButton>
</template>

<script>
import CustomButton from "@/components/CustomButton";
export default {
  data() {
    return {
      inputId: ''
    }
  },
  name: "SearchBar",
  components: {CustomButton},

  methods: {
    searchForId(id) {
      this.$emit('searched', id)
    }
  }
}
</script>

<style scoped>

</style>