<template>
  <div id="employee-add">
    <form @submit.prevent="handleSubmit">
      <label>Employee name :</label>
      <input v-model="employee.name" type="text" />
      <label> Employee Email :</label>
      <input v-model="employee.email" type="text" />
      <button id="addButton">Add</button>
    </form>
  </div>
</template>
<script>
export default {
  name: "EmployeeAdd",
  data() {
    return {
      employee: {
        name: "",
        email: ""
      }
    };
  },
  methods: {
    handleSubmit() {
      this.$emit("add:employee", this.employee);
      console.log("added");
    }
  }
};
</script>
<style scoped>
#addButton {
  color: rgb(190, 13, 13);
}
</style>