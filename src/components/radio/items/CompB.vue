<script setup lang="ts">
import { ref } from 'vue'

const msg = ref('')

</script>

<template>
    <div>
        <p>Current component: B</p>
        <div class="py-5 w-1/3">
            <div>
                <span>Message is: {{ msg }}</span>
            </div>
            <div>
                <input 
                    class="border focus:border-2"
                    v-model="msg"
                    placeholder="type input ... "
                />
            </div>
    </div>
    </div>
</template>
    
<style scoped>
    
</style>
    