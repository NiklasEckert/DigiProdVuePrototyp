<template>
  <h2>Alle Komponenten</h2>
  <table>
    <thead>
      <tr>
        <th>ID</th>
        <th>Article Number</th>
        <th>Order Number</th>
        <th>Birthdate</th>
        <th>Location</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="comp in comps" :key="comp.id">
        <td>{{ comp.id }}</td>
        <td>{{ comp.articleNumber }}</td>
        <td>{{ comp.orderNumber }}</td>
        <td>{{ comp.birthdate }}</td>
        <td>{{ comp.location }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  inject: ['comps'],
  name: "CompList"
}
</script>

<style scoped>

</style>