<template>
    <div class="todo-title">
        <h1>{{title}}</h1>
        <h1>{{dataLength.length}}</h1>
    </div>
</template>

<script>
    export default {
        props: ["title", "dataLength"]
        
    }
</script>

<style>
    .todo-title {
        display: flex;
        justify-content: space-between;
        margin: 15px 20px 0px 20px;
        color: #3F51B5
    }

    .todo-title h1 {
        font-size: 20px;
        margin: 0px;
    }

    .todo-title h1:last-child {
        color: white;
        background-color: #3F51B5;
        padding-left: 9px;
        padding-right: 9px;
        padding-top: 4px;
        border-radius: 50px;
        font-size: 13px;
    }
</style>