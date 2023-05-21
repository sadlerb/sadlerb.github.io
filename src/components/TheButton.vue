<template>
    <div :class="type">
        <button>
            {{ text }}
        </button>
    </div>
</template>


<script>
export default {
    props: ['text', 'type']
}
</script>

<style scoped>
button {
    width: 250px;
    padding: 15px;
    height: auto;
    font-size: 18px;
    font-weight: 600;
    margin: 0.5rem;
}

.default button {
    border: solid green;
    border-radius: 15px;
    color: green;
    background-color: transparent;
}

.default:hover button{
    border: solid transparent;
    background-color: green;
    color: white;
    border-radius: 15px;
}

.filled button{
    border: solid green;
    border-radius: 15px;
    color: white;
    background-color: green;
} 
.filled:hover button{
    border: solid #11431a;
    border-radius: 15px;
    color: white;
    background-color: #11431a;
}

@media(max-width : 768px) {
    button {
        width: 180px;
        font-size: 13px;

    }
}
</style>