<template>
 <p v-if="age > 25">{{msg}}. My name is {{name}}. I am {{age}} years old.</p>
 <p v-else>You must be 25 years or older to view this message</p>
</template>

<script>
export default {
  name: "Greeting",
  props: ["age"],
  data() {
    return {
      msg: "Hello World",
      name: "Elaine"
    }
  }
}
</script>

<style scoped lang="scss">
$color: red;

p {
    color: $color;
}
</style>