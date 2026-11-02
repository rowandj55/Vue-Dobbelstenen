<template>
    <div>
        <button @click="emitRolls">Throw the dice!</button>
    </div>
</template>

<script setup>
import {ref} from 'vue';
const props = defineProps({
    count: Object,
});

const newRoll = ref('');

const emit = defineEmits(['addRoll']);

const emitRolls = () => {
    newRoll.value = Math.floor(Math.random() * 6) + 1;
    emit('addRoll', newRoll.value);
};
</script>
