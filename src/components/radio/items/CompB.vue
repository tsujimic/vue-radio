<script setup lang="ts">
import { ref } from 'vue'

defineProps({
  msg: String
})

const value = ref('')

</script>

<template>
    <div>
        <p>Current component: B</p>
        <h3 class="mt-1 text-2xl text-indigo-500">{{ msg }}</h3>

        <div class="py-5 w-1/3">
            <div>
                <span>Message is: {{ value }}</span>
            </div>
            <div>
                <input 
                    class="border focus:border-2"
                    v-model="value"
                    placeholder="type input ... "
                />
            </div>
        </div>
    </div>
</template>
    
<style scoped>
    
</style>
    