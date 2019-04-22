<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar/>
    <!-- <AllFriends :friends="friends" @delete="deleteFriend"/>
    <OnlineFriends :friends="friends"/> -->
    <Blogs />
  </div>
</template>

<script>
import Navbar from './Navbar'
// import AllFriends from './AllFriends.vue'
// import OnlineFriends from './OnlineFriends'
import Blogs from './Blogs'

export default {
  name: 'app',
  components: {
    Navbar: Navbar,
    // AllFriends: AllFriends,
    // OnlineFriends: OnlineFriends,
    Blogs: Blogs
  },
  data () {
    return {
      title: "My first Vue app, wooohooo!!!",
      // friends: [
      //       {name: 'Mario', online:true},
      //       {name: 'Luigi', online:false},
      //       {name: 'Toad', online:true},
      //       {name: 'Bowser', online:false}
      //   ]
    }
  },
  methods:{
    // deleteFriend(payload){
    //   console.log(payload)
    //   this.friends = this.friends.filter(
    //     friend => friend.name !== payload.name
    //   )
    // }
  }
}
</script>

<style>
h1 {
  color:hsl(0,0%,20%);
  text-align: center;
  font-weight: nomral;
}
</style>
