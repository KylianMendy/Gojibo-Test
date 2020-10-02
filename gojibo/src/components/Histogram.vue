<template>
  <div class="histogram">
    <p class="historgam__date">{{date}}</p>
    <p class="historam__value">{{value}}</p>
  </div>
</template>

<script>
export default {
  name:'Histogram',
  props:{
    data:Object,
    date:String,
    value:Number,
  }
}
</script>

<style lang="scss" scoped>
.histogram{
  width: 25vw;
  display: flex;
  justify-content: space-around;
  align-items: center;
  p{
    margin-top: 3%;
  }
}
</style>