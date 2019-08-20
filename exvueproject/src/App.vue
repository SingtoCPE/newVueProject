<template>
  <div id="app">
    <h1>Employee Management</h1>
    <employee-adds @add:employee="addEmployee" />
    <employee-table v-bind:employees="employees" />
  </div>
</template>

<script>
import EmployeeTable from "./components/EmployeeTable.vue";
import EmployeeAdds from "./components/EmployeeAdds.vue";

export default {
  name: "app",
  components: {
    EmployeeTable,
    EmployeeAdds
  },
  data() {
    return {
      employees: [
        {
          
          name: "Richard Hendricks",
          email: "richard@piedpiper.com"
        }
      ]
    };
  },
  methods: {
    addEmployee(employee) {
      console.log(employee.name);
      console.log(employee.email);
      this.employees.push(employee)
    }
  }
};
</script>

<style>
</style>
