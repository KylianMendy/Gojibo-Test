<template>
  <div class="stats">
    <div class="stats__partone">
      <h1 class="stats__title">Stats</h1>
      <div class="stats__graphic">
        <div>
          <h2>Values</h2>
          <line-chart :data="chartdata"></line-chart>
        </div>
      </div>
    </div>
    <div class="stats__parttwo">
      <Meanvalue class="meanvalue"/>
      <div class="listvalue">
        <div class="listvalue__titles">
          <p class="">Dates</p>
          <p class="">Values</p>
        </div>
      <Histogram class="histogram" v-for="(data,index) in datas"
      :data="data"
      :date="data.date"
      :value="data.value"
      :key=index>
      </Histogram>
      </div>
    </div>
  </div>
</template>

<script>

import Meanvalue from './Meanvalue.vue'
import Histogram from './Histogram.vue'
export default {
  name:'Stats',
  components:{
    Meanvalue,
    Histogram,
  }, 
   data(){
     return{
       chartdata: {
         "2020/09/20":8,
         "2020/09/21":9,
         "2020/09/22":14,
         "2020/09/23":8,
         "2020/09/24":12,
         "2020/09/26":0,
         "2020/09/27":9,
         "2020/09/28":10,
         "2020/09/29":15
       },
      chartOptions: {
      responsive: true,
      maintainAspectRatio: false
     },
      datas: [
        {
          date: "2020/09/20",
          value: 8
        },
        {
          date: "2020/09/21",
          value: 9
        },
        {
          date: "2020/09/22",
          value: 14
        },
        {
          date: "2020/09/23",
          value: 8
        },
        {
          date: "2020/09/24",
          value: 12
        },
        {
          date: "2020/09/25",
          value: 4
        },
        {
          date: "2020/09/25",
          value: 10
        },
        {
          date: "2020/09/25",
          value: 12
        },
        {
          date: "2020/09/26",
          value: 0
        },
        {
          date: "2020/09/27",
          value: 9
        },
        {
          date: "2020/09/28",
          value: 10
        },
        {
          date: "2020/09/29",
          value: 15
        },  
      ],
    }
  }
}

</script>

<style lang="scss" scoped>
.stats{
  display: flex;
  justify-content: space-around;
  width: 100vw;
  text-align: left;
  margin-top: 5%;

  &__partone{
    width: 50vw;
    margin-top: 3%;
  }

  &__graphic{
    border-radius: 0.5rem;
    width: 600px;
    height: 200px;
  }

  &__parttwo{
    width: 30vw;
    
    .meanvalue{
      position: relative;
      bottom: 4em;
      right: 4em;
      z-index: 100;
    }
    .listvalue{

      &__titles{
        display: flex;
        font-weight: bold;
        width: 25vw;
        justify-content: space-around;
      }
    }
  }

  &__title{
    font-size: 96px;
    font-weight: bolder;
    color: #13629B;
    margin: 0;
  }
}

.histogram:nth-child(odd) {
    background: #CCC
  }
</style>