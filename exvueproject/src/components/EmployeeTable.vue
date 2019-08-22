<template>
  <div id="employee-table">
    <ul v-for="employee in employees" :key="employee.id">
      <li>{{employee.name}}</li>
      <li>{{employee.email}}</li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "employee-table",
  props: {
    employees: Array
  }
};
</script>
<style scoped>
</style>