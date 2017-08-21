<style>
    /*body{*/
        /*height: 2000px;*/
    /*}*/
</style>
<template>
    <Scrollbar style="height: 300px" ref="scrollbar">
        <div style="height: 600px;width:300px;background-color: #1c2438">

        </div>
        <BackTop :show="true" @on-click="aa">

        </BackTop>
    </Scrollbar>

</template>
<script>
    export default {
        data(){
            return {

            }
        },
        methods:{
        	aa(){
        		this.$refs.scrollbar.scrollToY(0)
            }
        },
        mounted(){
            
        }
    }
</script>
