<script>
    export default { 
        data() {
            return {
                // Add code here
                id: "demo1",
                bluebtn: true,
                blueBox: true
            }
        },
        methods: { 
   			// Add code here
            changeColor(){
                this.blueBox = !this.blueBox;
                this.bluebtn = !this.bluebtn
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class="m-2" @click="changeColor" :class="{'blueBox': blueBox, 'redBox': !blueBox}">
            div ID : {{id}} 
        </div>
        
        <button type="button" @click="changeColor" :class="{'btn btn-primary': bluebtn, 'btn btn-danger': !bluebtn}">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>