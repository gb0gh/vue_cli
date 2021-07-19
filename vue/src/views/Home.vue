<template>
  <div>
    <h1>Don't try this at home</h1>
    <p>{{name}}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name : 'WWE Superstar John Cina'
    }
  }
}
</script>

<style scoped>
h1{
  font-size:20px;
  color : red;
}
</style>