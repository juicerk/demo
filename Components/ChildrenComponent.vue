<template>
    <div>
        <button @click="sendData()">Send message</button>
    </div>
    <div class="test-v-model">
        <input v-model="messageModel"/>
        <input v-model="messageModel2"/>
    </div>

    <div>
        <p>grandParent shardData: {{ shardData }}</p>
    </div>
</template>

<script setup>
import { defineModel, inject } from 'vue';

defineProps({
    placeholder:{
        type: String,
        default: '123'
    }
})
const emit = defineEmits(['sendEvent'])
function sendData() {
    emit('sendEvent','abc','bcd','efgggg');
}
const messageModel = defineModel('message');
const messageModel2 = defineModel('message2');

const shardData = inject('shardValue')
</script>