<template>
    <div class="blogs">
        <h2>{{ blogTitle }}</h2>
        <input type="text" v-model="searchTerm">
        <button @click="changeTitle">Change Title</button>
        <div v-for="post in filteredPosts" :key="post.id">
            <h3>{{ post.title }}</h3>
            <p> {{ post.body  | snippet}}</p>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    name:'Blogs',
    data(){
        return{
            blogTitle:'Blogs',
            posts: [],
            searchTerm: ''
        }
    },
    methods: {
        changeTitle(){
            this.blogTitle = 'Amazing Blog Site'
        }
    },
    // beforeCreate(){
    //     alert("beforeCreate hook")
    // },
    computed: {
        filteredPosts() {
            return this.posts.filter(posts => {
                return posts.title.match(this.searchTerm)
            })
        }
    },
    created(){
       // alert("created hook")
       // npm install axios ==>
       axios.get('https://jsonplaceholder.typicode.com/posts')
       .then(response => {
           console.log(response)
           this.posts = response.data
       }).catch(err => {
           console.log(err)
       })
    }
    // beforeUpdate(){
    //     alert("beforeUpdate hook")
    // }
}
</script>