<script setup>
import Posts from "./Posts.vue";
import {posts   } from "../assets/posts"
</script>

<template>
    <div class="projects">
        <h2>My Projects</h2>
        <div v-for="post in posts">
            <Posts :title="post.title" :text="post.text" :img="post.img" :link="post.link"/>
        </div>
    </div>
</template>


<script>

</script>

<style scoped>

@media only screen and (max-width: 768px) {
    .projects{
        text-align: center;
    }
}


</style>