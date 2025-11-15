<template>
    <div class="bg-gray-100 min-h-screen flex items-center justify-center">
        <div class="bg-white shadow-md rounded-lg p-6 w-full max-w-md">
            <h1 class="text-2xl font-bold text-center mb-4">To-Do App</h1>

            <!-- Input for adding a new task -->
            <div class="flex mb-4">
                <input type="teclxt" placeholder="Add a new task..."
                    class="flex-1 border rounded-l-lg px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-400" />
                <button class="bg-blue-500 text-white px-4 py-2 rounded-r-lg hover:bg-blue-600">
                    Add
                </button>
            </div>

            <!-- No tasks message -->
            <p class="text-gray-500 text-center">
                No tasks yet! Add your first task.
            </p>

            <!-- List of tasks -->
            <ul>
                <li v-for="(todo, index) in todos" :key="index" class="flex items-center justify-between border-b py-2">
                    <!-- Task text or editable input -->
                    <div class="flex items-center gap-2">
                        
                            {{ todo.text }}
                    
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";

</script>
<style>

</style>