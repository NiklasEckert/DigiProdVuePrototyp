<template>
  <h1>Komponenten</h1>
  <SearchBar @searched="(id) => {this.showDetails = true; this.searchId = id;}"/>
  <CompDetails v-if="showDetails" :search-id="searchId" @disableDetails="() => {this.showDetails = false}"/>
  <CompList v-if="!showDetails"/>
</template>

<script>
import CompDetails from "@/components/CompDetails";
import SearchBar from "@/components/SearchBar";
import CompList from "@/components/CompList";
export default {
  data() {
    return {
      showDetails: false,
      searchId: Number
    }
  },
  name: "RootComp",
  components: {CompList, SearchBar, CompDetails}
}
</script>

<style scoped>

</style>