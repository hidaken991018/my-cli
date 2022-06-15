 
<template>
  <div class="mytest"><p v-if="isVisible">{{ message }}</p></div>

</template>

<script>
export default {
  data: function() {
    return {
      message: 'hello'
    }
  },
  computed: {
    isVisible: function() {
      if (this.message) {
        return true;
      } else {
        return false;
      }
    }
  }
}
</script>

<style scoped>。
div {
  text-align: center;
 
}
</style>