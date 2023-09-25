<template>
    <div>
        Here comes the content of the HomePage.
        Buttons:
        <ul style="list-style: none;">
            <li>
                <BaseButton>
                    Active default button
                </BaseButton>
            </li>
            <li>
                <BaseButton disabled>
                    Disabled default button
                </BaseButton>
            </li>
            <li>
                <BaseButton color="primary">
                    Active primary button
                </BaseButton>
            </li>
            <li>
                <BaseButton color="primary" disabled>
                    Disabled primary button
                </BaseButton>
            </li>
            <li>
                <BaseButton color="warn">
                    Active warn button
                </BaseButton>
            </li>
            <li>
                <BaseButton color="warn" disabled>
                    Disabled warn button
                </BaseButton>
            </li>
            <li>
                <BaseButton color="danger">
                    Active danger button
                </BaseButton>
            </li>
            <li>
                <BaseButton color="danger" disabled>
                    Disabled danger button
                </BaseButton>
            </li>
        </ul>

        <br><br>

        <BaseAsyncButton @click="myPromise">Text</BaseAsyncButton>
    </div>
</template>

<script setup>
import { ref } from 'vue'

import BaseButton from '../components/BaseButton.vue'
import BaseAsyncButton from '../components/BaseAsyncButton.vue'

var count = ref(0);

function myPromise() {
    count.value += 1;
    return new Promise((resolveInner) => {
        setTimeout(resolveInner, (count.value * 1000) + 1000);
    })
}
</script>

<style scoped>
div {
    margin: 2rem;
    text-align: center;
}
</style>
