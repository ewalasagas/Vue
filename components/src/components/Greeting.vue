<template>
 <p>{{msg}}. My name is {{name}}</p>
</template>

<script>
export default {
  name: "Greeting",
  data() {
    return {
      msg: "Hello World",
      name: "Elaine"
    }
  }
}
</script>

<style>
p {
    color: red;
}
</style>