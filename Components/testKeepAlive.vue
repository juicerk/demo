<template>
    <p>Keep-Alive 演示</p>
    <p>curComponent:{{ curComponent }}</p>
    <button @click="changeB">changeB</button>
    <button @click="changeA">changeA</button>

    <KeepAlive>
        <component :is="currentComponent"/>
    </KeepAlive>
    <p>---------without keepAlive--------</p>
    <component :is="currentComponent"/>
</template>

<script setup>
import { ref } from 'vue';
import ComponentA from './ComponentA.vue';
import ComponentB from './ComponentB.vue';

const curComponent = ref('ComponentA')
const currentComponent = ref(ComponentA)

const changeA = function() {
    curComponent.value = 'ComponentA'
    currentComponent.value = ComponentA
}

const changeB = function() {
    curComponent.value = 'ComponentB'
    currentComponent.value = ComponentB
}
</script>