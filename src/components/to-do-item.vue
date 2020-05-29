<template>
  <div class="item">
    <h4>{{ msg }}</h4>
  </div>
</template>

<script>
  export default {
    name: 'to-do-item',
    props: {
      msg: String
    }
  }
</script>

<style scoped>
  div {
    width: fit-content;
    height: fit-content;
    padding: 0px 5px 0px 5px;
  }
</style>
