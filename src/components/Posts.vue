<script setup>
import TheButton from './TheButton.vue';
</script>

<template>
    <div class="post_container">
        <div class="posts">
            <h2>{{ title }}</h2>
            <p>{{ text }}</p>
        </div>
        <div v-on:click="openLink()" class="image_wrapper">
            <img :src='"/assets/images/"+img' alt="postImage">
            <div class="overlay">
                <TheButton text="Visit the Repository" type="filled"/>
            </div>
        </div>


    </div>
</template>

<script>
export default {
    props: ['title', 'text','img','link'],
    methods:{
        openLink(){
            window.open(this.link,'_blank')
        }
    }
  


}


</script>

<style scoped>
.post_container {
    display: grid;
    grid-template-columns: 3fr 2fr;
    margin-top: 5rem;
    align-items: center;
    justify-items: center;
    
}

h2 {
    padding-bottom: .5;
    color: green;
  
    

}

img{
    max-width:100%;
    max-height:100%;
}

.image_wrapper{
    position: relative;
    
}

.image_wrapper:hover .overlay {
    bottom: 0;
    height: 100%;
  }

.overlay {
    position: absolute;
    left: 0;
    bottom: 100%;
    height: 0;
    width: 100%;
    overflow: hidden;
    backdrop-filter: blur(8px) brightness(80%);
    transition: all .3s ease-in-out;
    display: flex;
    align-items: center;
    justify-content: center;
  }










@media only screen and (max-width: 768px) {
    .post_container {
        display: flex;
        flex-direction: column;
        text-align: center;

    }
    img{
        padding: 10px;
    }






}
</style>
