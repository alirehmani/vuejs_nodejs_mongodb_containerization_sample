<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <employee-form msg="I Love Devops"></employee-form>
</template>
<script>


import EmployeeForm from './components/EmployeeForm.vue'

export default {
  name: 'App',
  components: {
    EmployeeForm
  }
}
</script>