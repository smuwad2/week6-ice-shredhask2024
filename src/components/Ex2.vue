<script>
    export default { 
        data() {
            return {
                width: '200',
                height: '200',
                myImg: '/assets/me.png'
            }
        },
    }
</script>

<template>

    <img v-bind:src="myImg" v-bind:width="width" v-bind:heights="height"/>
   
</template>
