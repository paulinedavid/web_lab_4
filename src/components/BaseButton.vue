<template>
<button :role="props.role" :style="props.style" :disabled="props.disabled" :class="color">
        <slot></slot>
    </button>
</template>

<script setup>
const props = defineProps(['role', 'style', 'disabled', 'color']);
var colors = ['primary', 'warn', 'danger'];

var color;

const init = async () => {
    if (colors.includes(props.color)) {
        color = props.color;
    } else {
        color = colors[0];
    }
};

init();
</script>

<script>
</script>


<style scoped>
button {
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
    box-shadow: none;
    border-color: rgb(230, 230, 230);
}

button.primary {
    background-color: green;
    color: white;
}

button:disabled.primary {
    background-color: rgb(151, 201, 151);
    color: white;
}

button.warn {
    background-color: rgb(242, 233, 64);
    color: black;
}

button:disabled.warn {
    background-color: rgb(255, 252, 199);
    color: rgb(148, 148, 148);
}

button.danger {
    background-color: rgb(225, 36, 36);
    color: white;
}

button:disabled.danger {
    background-color: rgb(255, 177, 177);
    color: white;
}
</style>
