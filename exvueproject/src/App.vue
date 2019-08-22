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
      lid: 0,
      employees: [

      ]
    };
  },
  methods: {
    addEmployee(employee) {
      console.log(employee.name);
      console.log(employee.email);
      this.lid = this.lid + 1
      this.employees = [...this.employees, {...employee, id: this.lid}];
      
    }
  }
};
</script>

<style>
</style>
