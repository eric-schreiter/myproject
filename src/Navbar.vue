<template>
    <nav class="main-nav">
        <ul>
            <li><a href="">Home</a></li>
            <li><a href="">About</a></li>
            <li><a href="">Contact</a></li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
    data(){
        return{

        }
    }
}
</script>

<style>
.main-nav ul{
    display:grid;
    grid-template-columns: 1fr 1fr 1fr;
    align-items: center;
    padding:.5rem;
    list-style: none;
    width:50%;
    margin:0 auto;
    text-align: center;
    font-size: 1.25rem;
}
</style>

