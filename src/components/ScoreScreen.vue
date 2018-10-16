<template>
  <div>
    <Cows :cow_count="crazycompoundobject"/>
  </div>
</template>
<script>
  import Cows from './Cows.vue'
  import cow_data from '@/data/cow_data.json'
  import {EventBus} from '@/store/event-bus.js'
  export default {
    created: function(){
      EventBus.$on('clicky', this.clicky)
    },
    destroyed: function(){
      EventBus.$off('clicky', this.clicky)
    },
    components: {
      Cows
    },
    methods: {
      clicky: function(evt, value){
        this.cows = evt.target.value
      }
    },
    data: function(){
      return {
        cows: 0
        crazycowscompoundobject: cow_data,
        pigs: 0
        crazycowscompoundobject: [{label: 'a', value: -1}]
        sheep: 0
        crazycowscompoundobject: [{label: 'a', value: -1}]
      }
    }
  }
</script>
<style>

</style>