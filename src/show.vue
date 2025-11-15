<template>
    <div class="box">
        <button @click="showMessage('success')" class="Sucsess">Show Success</button>
        <button @click="showMessage('error')" class="Error">Show Error</button>
        <button @click="showMessage('info')" class="Info">Show Info</button>
    </div>

    <div class="ShowBox">  
        <div v-if="visibleMessage === 'success'" class="Sucsess-message">
            <h1>Action completed Successfully!</h1>
            <button @click="dismissMessage">Dismiss</button>
        </div>
        <div v-if="visibleMessage === 'error'" class="Error-message">
            <h1>Something went wrong! Please try again.</h1>
            <button @click="dismissMessage">Dismiss</button>
        </div>
        <div v-if="visibleMessage === 'info'" class="Info-message">
            <h1>Here is some important information for you.</h1>
            <button @click="dismissMessage">Dismiss</button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            visibleMessage: null, 
        };
    },
    methods: {
        showMessage(type) {
            this.visibleMessage = type; 
        },
        dismissMessage() {
            this.visibleMessage = null; 
        },
    },
};
</script>

<!-- <style>

   .box {
    display: flex;
    justify-content: center;
    padding: 5px;
    }
    .box > button {
        padding: 15px;
        cursor: pointer;
        border-radius: 5px;
        margin: 20px;
        width: 160px;
        font-weight: 700;
    }
    h1{
        font-size: 26px;
    }
    .Sucsess {
        background-color: rgb(68, 194, 68) ;
        border: none;
        padding: 10px;
        border-radius: 5px;
    }
    .Error {
        background-color: rgb(224, 73, 73);
        border: none;
        border-radius: 5px;    }
    .Info {
        background-color: rgb(53, 53, 235);
        border: none;
        border-radius: 5px;    }
    .ShowBox {
        display: flex;
        margin: 20px;
        width: auto;
        height: 100%;
        z-index: 100;
        justify-content: center;
        align-items: center;
    }
    .ShowBox > div {
        width: 300px;
        /* height: 200px; */
        border-radius: 10px;
        padding: 30px;
        text-align: center;
        /* color: white; */
        margin: 10px;
    }
    .ShowBox > button {
        border: 1px;
        border-radius: 5px;
        padding: 5px;
        margin-bottom: 20px;
        background-color: rgb(181, 180, 180);
        color: rgb(66, 65, 65);
    }
    .Sucsess-message > button {
        border: 1px;
        border-radius: 5px;
        font-size: 20px;
        padding: 5px;
        margin-bottom: 20px;
        background-color: rgb(181, 180, 180);
        color: rgb(66, 65, 65);    }
    .Error-message > button {
        border: 1px;
        border-radius: 5px;
        font-size: 20px;
        padding: 5px;
        margin-bottom: 20px;
        background-color: rgb(181, 180, 180);
        color: rgb(66, 65, 65);
    }
    .Info-message > button {
        border: 1px;
        border-radius: 5px;
        font-size: 20px;
        padding: 5px;
        margin-bottom: 20px;
        background-color: rgb(181, 180, 180);
        color: rgb(66, 65, 65);
    }
    .Sucsess-message {
        background-color: rgb(100, 229, 120) ;
        color: rgb(19, 181, 57);
    }
    .Error-message {
        background-color: rgb(237, 119, 119);
        color: rgb(195, 42, 42);
    }
    .Info-message {
        background-color: rgb(81, 128, 237);
        color: blue;
    }

</style> -->
