<template>
  <div>
    <div v-for="item in list">
      <input type="radio" :id="item" name="cowcount" :value="item" @click="clicku">
      <label :for="item">{{item}}</label>
    </div>
<!--     <br>
    <input type="radio" id="two" name="cowcount" value="1" @click="clicku">
    <label for="two">One</label>
    <br>
    <input type="radio" id="three" name="cowcount" value="2" @click="clicku">
    <label for="two">Two to Three</label>
    <br>
    <input type="radio" id="four" name="cowcount" value="3" @click="clicku">
    <label for="two">Four to Five</label>
    <br>
    <input type="radio" id="five" name="cowcount" value="4" @click="clicku">
    <label for="two">Six or More</label>
    <br>
 -->    <span>Cows: {{ cow_count }}</span>
  </div>
</template>
<script>
  import {EventBus} from '../store/event-bus.js'

  export default {
    data: function(){
      return {
        list: [1,2,3,4,5,6]
      }
    },
    props: [
      'cow_count'
    ],
    methods: {
      clicku: function(value){
        EventBus.$emit('clicky', value)
      }
    }

  }

</script>
<style></style>