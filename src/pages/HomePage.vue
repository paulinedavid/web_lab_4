<template>
    <div>
        Here comes the content of the HomePage.
        <BaseButton> 
            Active button
        </BaseButton>
        <BaseButton disabled> 
            Disabled button
        </BaseButton>
    </div>
</template>

<script setup>
import BaseButton from '../components/BaseButton.vue'
</script>

<style scoped>
div {
    margin: 2rem;
    text-align: center;
}
</style>
