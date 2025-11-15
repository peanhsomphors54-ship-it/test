<template>
<div class="all">
    <div class="success">
        <div class="n1">
            <button @click="showSuccess" class="a">Show Success</button>
            <button @click="showError" class="b">Show Error</button>
            <button @click="showInfo" class="c">Show Info</button>
        </div>
        <div class="n2">
            <div v-if="Notification" class="m">
                <h1>Action Complited successfully!</h1>
                <button class="d" @click="dismiss" >Dismiss</button>
            </div>
        </div>
    </div>
    <!-- <div class="error">
    <div class="n1">
        <button @click="showSuccess" class="a">Show Success</button>
        <button @click="showError" class="b">Show Error</button>
        <button @click="showInfo" class="c">Show Info</button>
    </div>
    <div class="n3">
        <div v-if="message" class="m">
            <h1 class="Err">Something went wrong. Please try again.</h1>
            <button class="d" @click="dismiss" >Dismiss</button>
        </div>
    </div>
</div> -->
<!-- <div class="info">
    <div class="n1">
        <button @click="showSuccess" class="a">Show Success</button>
        <button @click="showError" class="b">Show Error</button>
        <button @click="showInfo" class="c">Show Info</button>
    </div>
    <div class="n4">
        <div v-if="message" class="m">
            <h1 class="In">Here is some important information for you.</h1>
            <button class="d" @click="dismiss" >Dismiss</button>
        </div>
    </div>
</div> -->
</div>
</template>

<script setup>
import { ref } from 'vue';
const message = ref('')

// const showSuccess = () => {
//     message.value = 'Success'
//     setInterval(()=>{
//         message.value = ''
//     }, 3000)
// }

// const showError = () => {
//     message.value = 'Success'
//     setInterval(()=>{
//         message.value = ''
//     }, 3000)
// }

// const showInfo = () => {
//     message.value = 'Success'
//     setInterval(()=>{
//         message.value = ''
//     }, 3000)
// }

// const dismiss = () => {
//     message.value = ''
// }

</script>

<!-- <style>
.all{
    display: flex;
    justify-content: center;
    padding: 5px;
}

    .n1{
        display: flex;
        justify-content: center;
        font-size: 30px;
        padding: 5px;
        margin: 30px;
    }

    .a{
        background-color: rgb(68, 194, 68) ;
        border: none;
        padding: 10px;
        border-radius: 5px;
    }
    .b{
        background-color: rgb(224, 73, 73);
        border: none;
        border-radius: 5px;
    }
    .c{
        background-color: rgb(75, 75, 243);
        border: none;
        border-radius: 5px;
    }
    .n2{
        border: 1px solid	;
        text-align: center;
        background-color: rgb(184, 249, 227);
        border-color: rgb(35, 181, 35);
        border-radius: 10px;
        margin: 30px;
    }
    .n3{
        border: 1px solid	;
        text-align: center;
        background-color: rgb(249, 184, 184);
        border-color: rgb(181, 35, 35);
        border-radius: 10px;
        margin: 30px;
    }
    .Err{
        color: rgb(207, 24, 24);
    }
    .n4{
        border: 1px solid	;
        text-align: center;
        background-color: rgb(118, 129, 246);
        border-color: rgb(57, 35, 181);
        border-radius: 10px;
        margin: 30px;
    }
    .In{
        color: rgb(53, 67, 224);
    }
    /* h1{
        color: rgb(66, 216, 166);
        margin: 25px;
    } */
    .d{
        border: 1px;
        border-radius: 5px;
        font-size: 21px;
        padding: 5px;
        margin-bottom: 20px;
        background-color: rgb(181, 180, 180);
        color: rgb(66, 65, 65);
    }
</style> -->