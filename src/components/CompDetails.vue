<template>
  <div>
    <span>ID:</span>
    <span>{{ comp.id }}</span>
  </div>
  <div>
    <span>ARTIKEL ID:</span>
    <span>{{ comp.articleNumber }}</span>
  </div>
  <div>
    <span>ORDER NR:</span>
    <span>{{ comp.orderNumber }}</span>
  </div>
  <div>
    <span>Birthdate:</span>
    <span>{{ comp.birthdate }}</span>
  </div>
  <div>
    <span>Location:</span>
    <span>{{ comp.location }}</span>
  </div>
  <CustomButton text="Startseite" @click="this.$emit('disableDetails')"/>
</template>

<script>
import CustomButton from "@/components/CustomButton";

export default {
  data() {
    return {
      comp: Object
    }
  },
  inject: ['comps'],
  name: "CompDetails",
  components: {
    CustomButton
  },
  watch: {
    searchId: {
      handler(newId) {
        this.loadComp(newId)
      },
      immediate: true
    }
  },
  props: {
    searchId: Number
  },
  methods: {
    loadComp(id) {
      //alert(`New Id ${this.comps[id].articleNumber} ${id}`)
      this.comp = this.comps[parseInt(id) - 1]
    }
  }

}
</script>

<style scoped>

</style>