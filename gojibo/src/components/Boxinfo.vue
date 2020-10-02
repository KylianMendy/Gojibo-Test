<template>
  <div class="boxinfo">
    <h1 class="boxinfo__title">Vos infos</h1>
    <div class="boxinfo__box">
      <div>
        <p>Name: {{firstname}}</p>
        <p>Lastname: {{lastname}}</p>
      </div>
      <div>
        <p>Gender: {{gender}}</p>
        <p>Email: {{email}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'Boxinfo',
  props:{
    firstname:String,
    lastname:String,
    gender:String,
    email:String,
  }
}
</script>

<style lang="scss" scoped>

.boxinfo{
  width: 40vw;
  background-color: #13629B;
  border-radius: 0.5rem;
  text-align: left;
  padding: 2%;
  color: #F6F5F5;
  &__title{
    font-size: 3rem;
    margin-left: 15%;
    font-weight: bold;
  }
  &__box{
  display: flex;
  justify-content: space-around;
  font-size:1rem;
  padding: 5%;

    p{
      margin-top: 10%;
    }
  }
}

</style>