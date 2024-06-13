<script setup lang="ts">
import { shallowRef } from 'vue'
import CompA from './items/CompA.vue'
import CompB from './items/CompB.vue'

const current = shallowRef(CompA)

</script>

<template>
    <header class="bg-white shadow">
        <div class="mx-auto max-w-7xl py-2 px-3 sm:px-6 lg:px-8">
          <h1 class="text-2xl font-bold tracking-tight text-gray-900">Radio</h1>
        </div>
    </header>
    <main>
        <div class="mx-auto max-w-7xl py-6 sm:px-6 lg:px-8">
            <div class="space-x-2">
                <label><input type="radio" v-model="current" :value="CompA" /> A</label>
                <label><input type="radio" v-model="current" :value="CompB" /> B</label>
            </div>
            <KeepAlive>
                <component :is="current"></component>
            </KeepAlive>
        </div>
    </main>    
</template>
    
<style scoped>
    
</style>
    