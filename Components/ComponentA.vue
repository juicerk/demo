<template>
    <p> ComponentA </p>
    <p> count:{{ count }}</p>
    <button @click="addCount">add</button>
    <input v-model="inputValue">
    <select v-model="selectValue">
        <option>1</option>
        <option>2</option>
        <option>3</option>
    </select>
</template>

<script setup name="ComponentA">
import {ref} from 'vue'

const count = ref(0);
const inputValue = ref('')
const selectValue = ref(1)

const addCount = function() {
    count.value ++;
}
</script>