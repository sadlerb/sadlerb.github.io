<script setup>
import GithubIcon from '../assets/icons/GithubIcon.vue';
import LinkedinIcon from '../assets/icons/LinkedinIcon.vue';
</script>
<template>
    <div class="icon_container">

            <a href="https://github.com/sadlerb" target="_blank">
                <GithubIcon />
            </a>

            <a href="https://www.linkedin.com/in/brendon-sadler-8259181b0/" target="_blank">
                <LinkedinIcon />
            </a>

    </div>
</template>

<style scoped>
svg:hover  {
    color: green
}

svg {
    max-width: 50px;
    max-height: 50px;
    color: white;
    margin: 1rem
}



@keyframes elastic-slide {
    from {
        margin-left: -400%;
        opacity: 0;
    }

    to {
        margin-left: 0%;
        opacity: 1;
    }
}

.icon_container {
    display: flex;
    flex-direction: row;
    justify-content: left;
    opacity: 0;
    animation: elastic-slide 2.2s cubic-bezier(0.68, -0.55, 0.265, 1.55) forwards;
    animation-delay: 4000ms;
}

@media only screen and (max-width: 768px) {
    .icon_container {
        justify-content: center;
    }

    svg {
        max-width: 35px;
        max-height: 35px;
    }








}
</style>