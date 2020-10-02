<template>
  <div class="box">
    <div>
      <p>Name: {{firstname}}</p>
      <p>Lastname: {{lastname}}</p>
    </div>
    <div>
      <p>Gender: {{gender}}</p>
      <p>Email: {{email}}</p>
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
.box{
  width: 40vw;
  background-color: #13629B;
  display: flex;
  justify-content: space-around;
  text-align: left;
  color: #F6F5F5;
  border-radius: 0.5rem;
  font-size:1rem;
  padding: 5%;

  p{
    margin-top: 10%;
  }
}
</style>