<template>
    <button :role="props.role" :style="props.style" :disabled="props.disabled">
        <slot></slot>
    </button>
</template>

<script setup>
const props = defineProps(['role', 'style', 'disabled']);
</script>


<style scoped>
button {
    background-color: green;
    color: white;
    border: solid 1px white;
    border-radius: 5px;
    box-shadow: rgba(0, 0, 0, .3) 0 0 5px;
    padding: 5px;
    transition: all ease-out 100ms;
}

button:hover {
    box-shadow: rgba(0, 0, 0, .5) 0 3px 10px;
}

button:active {
    box-shadow: none;
}

button:disabled {
    background-color: rgb(151, 201, 151);
    color: white;
    box-shadow: none;
    border-color: rgb(230, 230, 230);
}
</style>
