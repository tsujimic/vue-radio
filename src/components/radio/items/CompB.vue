<script setup lang="ts">
import { reactive, onMounted, watch } from 'vue'

defineProps({
    msg: String
})

const data = reactive({
    text: '',
    count: 0
});

onMounted(() => {
    const storedCompb = localStorage.getItem('compb');
    if (storedCompb) {
        Object.assign(data, JSON.parse(storedCompb));
    }
    // console.log('onMounted: ', data);

});

watch(data, (newVal) => {
    localStorage.setItem('compb', JSON.stringify(newVal));
    // console.log('localStorage.setItem: ', newVal);
}, { deep: true });

</script>

<template>
    <div>
        <p>Current component: B</p>
        <h3 class="mt-1 text-2xl text-indigo-500">{{ msg }}</h3>

        <div class="py-5 w-1/3">
            <div>
                <span>Message is: {{ data.text }}</span>
            </div>
            <div>
                <input 
                    class="border focus:border-2"
                    v-model="data.text"
                    placeholder="type input ... "
                />
            </div>
            <div>
                <span>count: {{ data.count }}</span>
            </div>
            <div class="space-x-1">
                <button type="button" class="bg-blue-400 hover:bg-blue-300 text-white rounded w-10 h-10" @click="data.count++">+</button>
                <button type="button" class="bg-orange-400 hover:bg-orange-300 text-white rounded w-10 h-10" @click="data.count--">-</button>
            </div>

        </div>
    </div>
</template>
    
<style scoped>
    
</style>
    