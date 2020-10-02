<template>
  <div class="meanvalue">
    <span class="meanvalue__number">12</span>
    <div class="meanvalue__text">
      <h2>Mean value</h2>
      <p>of the mounth</p>
    </div>
  </div>
</template>

<script>
export default {
  name:'Meanvalue'
}
</script>

<style lang="scss" scoped>

.meanvalue{
  display: flex;
  width: 20vw;
  margin-left: 40%;
  box-shadow: 2px 2px 32px 2px rgba(175,175,175,1);
  border-radius: 0.5rem;
  padding: 3%;
  &__number{
  font-size: 72px;
  color: #13629B;
  font-weight: bolder;
  margin-right: 5%;
  margin-left: 3%;
  }
  &__text{
    margin-left: 2%;
    text-align: left;
    h2{
      margin-top: 15%;
      margin-bottom: 0;
    }
    p{
      margin: 0;
      color: #CACACA;
    }
  }
}

</style>