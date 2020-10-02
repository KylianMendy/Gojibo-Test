<template>
  <div class="welcome">
    <div class="welcome__partone">
      <div class="message">
        <h1 class="message__one">Welcome</h1>
        <h1 class="message__two">Enola</h1>
      </div>
      <Boxinfo class="boxinfo"
      v-for="(firstname,index) in firstnames"
      :key=index
      :firstname="firstnames[index]"
      :lastname="lastnames[index]"
      :gender="genders[index]"
      :email="emails[index]"/>
    </div>
    <div class="welcome__parttwo">
      <div class="profile">
        <svg width="35" height="35" viewBox="0 0 35 35" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M16.4746 5.19531H18.5254C18.7077 5.19531 18.7988 5.28646 18.7988 5.46875V29.5312C18.7988 29.7135 18.7077 29.8047 18.5254 29.8047H16.4746C16.2923 29.8047 16.2012 29.7135 16.2012 29.5312V5.46875C16.2012 5.28646 16.2923 5.19531 16.4746 5.19531Z" fill="black"/>
        <path d="M6.01562 16.2012H28.9844C29.1667 16.2012 29.2578 16.2923 29.2578 16.4746V18.5254C29.2578 18.7077 29.1667 18.7988 28.9844 18.7988H6.01562C5.83333 18.7988 5.74219 18.7077 5.74219 18.5254V16.4746C5.74219 16.2923 5.83333 16.2012 6.01562 16.2012Z" fill="black"/>
        
        </svg>
        <img class="profile__pic" :src="pic" alt="profile_pic"/>
      </div>
      <Search/>
    </div>
  </div>
</template>

<script>

import Search from './Search'

import Boxinfo from '../components/Boxinfo.vue'

export default {
  name: 'Welcome',
  components:{
    Boxinfo,
    Search,
  },
  data(){
    return{
      firstnames:["Enola"] ,
      lastnames: ["Holmes"],
      genders: ["F"],
      emails: ["unknowned"],
      pic:["https://cdn.discordapp.com/attachments/639945082967031849/761548680679260191/profile_pic.png"]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>


.welcome{
  margin-top: 5%;
  width: 100vw;
  display: flex;
  justify-content: space-around;
  &__partone{
    width:50vw
  }
  &__parttwow{
    width: 50vw;
  }
  h1{
    margin: 0;
  }
  .profile{
      text-align: right;
      margin-bottom: 20%;
      align-items: center;
      &__pic{
        width: 3em;
      }
    }
}
.message{
  display: flex;
  font-weight: bold;
  font-size: 4rem;
  width: 30vw;
  justify-content: space-between;
  margin-bottom: 5%;
  &__two{
  color: #13629B;
  }
} 
</style>
