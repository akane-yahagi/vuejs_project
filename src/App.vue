<template>
  <div>
    <LikeHeader>
      <template v-slot:title>
        <h2>Hello!</h2>
      </template>
      <template v-slot:number>
        <p>number of Likes</p>
        <h2>{{ number }}</h2>    
      </template>
    </LikeHeader>
    <LikeNumber :total-number="number" @my-click="incrementNumber"></LikeNumber>
    <LikeNumber :total-number="number" @my-click="number = $event"></LikeNumber>  
  </div>
</template>

<script>
import LikeHeader from "./components/LikeHeader.vue"
export default {
  data() {
    return {
      number: 14
    }
  },
  components: {
    LikeHeader
  },
  methods: {
    incrementNumber(value) {
      this.number = value;
    }
  }
}  
</script>

<style scoped>
</style>
