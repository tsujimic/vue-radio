<script setup lang="ts">
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)

</script>

<template>
    <div>
        <p>Current component: A</p>
        <h3 class="mt-1 text-2xl text-indigo-500">{{ msg }}</h3>

        <div class="py-5">
            <div>
                <span>count: {{ count }}</span>
            </div>
            <div class="space-x-1">
                <button type="button" class="bg-blue-400 hover:bg-blue-300 text-white rounded w-10 h-10" @click="count++">+</button>
                <button type="button" class="bg-orange-400 hover:bg-orange-300 text-white rounded w-10 h-10" @click="count--">-</button>
            </div>
        </div>

    </div>

</template>
    
<style scoped>
    
</style>
    