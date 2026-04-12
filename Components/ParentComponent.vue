<template>
    <p>{{ message }}</p>
    <p>{{ message2 }}</p>
    <p>--------------------</p>

    <ChildrenComponent @sendEvent="needtosolve" v-model:message="message" v-model:message2="message2" placeholder="输入..."/>

    <p>--------------------</p>
</template>

<script setup>
import { ref } from 'vue';
import ChildrenComponent from './ChildrenComponent.vue';

const message = ref('')
const message2 = ref('')

function needtosolve(p1,p2,p3) {
    console.log(p1,p2,p3);
}
</script>