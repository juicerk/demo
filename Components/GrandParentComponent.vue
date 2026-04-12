<template>
    <div>
        <p>this grandParent</p>
        <ParentComponent />
    </div>
</template>

<script setup>
import { provide } from 'vue';
import ParentComponent from './ParentComponent.vue';

provide('shardValue', 'hello world!');
</script>