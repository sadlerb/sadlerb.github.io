<script setup>
import TheButton from './TheButton.vue';
import TheSocials from './TheSocials.vue';
</script>

<template>
    <div class="header_container">
        <div class="hero">
            <div class="typed">
                <h1>Brendon Sadler</h1>
            </div>
            <div class="typed-delayed">
                <h2>Full-Stack Developer</h2>
            </div>
            <div class="button_container">
                <div class="slide">
                    <a href="mailto:sadlerb22@gmail.com">
                        <TheButton text="Contact Me" type="default" />
                    </a>
                </div>
                <div class="slide">
                    <a href="/assets/Resume_2023.pdf" download="Brendon_Sadler.pdf">
                        <TheButton text="Download My Resume" type="default"/>
                    </a>
                </div>
            </div>
            <TheSocials />
        </div>
    </div>
</template>

<style scoped>
.hero {
    display: flex;
    flex-direction: column;
    padding-bottom: 3rem;

}

h2 {
    font-size: 30px;
    display: table-caption;
    margin: 0;

}

h1 {
    font-size: 50px;
    color: var(--color-heading);
    display: table-caption;

}

.typed h1 {
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid;
    width: 0;
    animation: typing 1.5s steps(30, end) forwards, blinking 1s infinite;
    animation-delay: 0ms;
}

.typed-delayed h2 {
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid;
    width: 0;
    animation: typing 1.5s steps(30, end) forwards, blinking 1s infinite;
    animation-delay: 2500ms;
}

.slide {
    animation-fill-mode: none, forwards;
    animation: sideInFromRight 2s ease-in-out forwards;
    animation-delay: 4000ms;
    opacity: 0;
    
}

@keyframes sideInFromRight {
    from {
        margin-left: 200%;
        opacity: 0;
    }

    to {
        margin-left: 0%;
        opacity: 1;
    }
}

@keyframes typing {
    from {
        width: 0
    }

    to {
        width: 100%
    }
}

@keyframes blinking {
    0% {
        border-right-color: transparent
    }

    50% {
        border-right-color: white
    }

    100% {
        border-right-color: transparent
    }
}

.button_container {

    display: flex;
    flex-direction: row;

}





@media(max-width : 426px) {
    .hero {
        align-items: center;
        justify-content: center;
        text-align: center;

    }

    h2 {
        font-size: 15px;
    }

    h1 {
        font-size: 18px;
    }

    .button_container {
        display: flex;
        flex-direction: column;
    }


}
</style>


