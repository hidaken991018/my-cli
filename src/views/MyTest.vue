 
<template>
  <div class="mytest"><p v-if="isVisible">{{ message }}</p></div>
  <BodyCom :username="name" @add="add1"></BodyCom>
  <p>total : {{ totalcount }} </p>

</template>

<script>


import BodyCom from '../components/BodyCom.vue'

export default {

  

  components:{
    BodyCom
  },
  data: function() {
    return {
      message: 'hello',
      name: "かまいたち山内",
      count1: 0,
      count2: 0,
      totalcount: 0
    }
  },

  methods:{
    add1(count){
      this.count1 = count;
      this.totalcount = this.count1 + this.count2;
    },
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