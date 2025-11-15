<template>
    <div class="flex flex-col items-center justify-center min-h-screen bg-gray-100 p-6">
        <!-- Buttons to trigger notifications -->
        <div class="space-x-4 mb-6">
            <button @click="success"
                class="px-4 py-2 bg-green-500 text-white rounded-lg shadow-md hover:bg-green-600 transition-all duration-300">
                Show Success
            </button>
            <button @click="error"
                class="px-4 py-2 bg-red-500 text-white rounded-lg shadow-md hover:bg-red-600 transition-all duration-300">
                Show Error
            </button>
            <button @click="info"
                class="px-4 py-2 bg-blue-500 text-white rounded-lg shadow-md hover:bg-blue-600 transition-all duration-300">
                Show Info
            </button>
        </div>

        <!-- Notification with Tailwind transitions -->
        <div v-if="notification.visible" >
            <p class="text-lg font-semibold">Display message</p>
            <button @click="dismissNotification"
                class="mt-2 px-4 py-2 bg-gray-200 text-gray-800 rounded-md hover:bg-gray-300 transition-all duration-200">
                Dismiss
            </button>
        </div>
    </div>
</template>
<script setup>
    import { ref } from 'vue';
    const notification = ref({
        visible: false,
        true:'',
        message:'',
    })
    const showNotification =(type)=>{
        notification.visible.value = true
        if(type=='success'){
            notification.message.value ='Successfull'
        }        
        else if(type =='error'){
            notification.message.value ='Error'
        }
        else{
            notification.message.value ='Info'
        }
    }
    const dismissNotification =()=>{
        notification.visible.value = false
    }
</script>
<style>

</style>