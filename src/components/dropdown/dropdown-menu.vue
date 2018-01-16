<template>
    <ul class="ivu-dropdown-menu" @click="prevent"><slot></slot></ul>
</template>
<script>
    export default {
    	methods: {
	    	prevent(e){
				event.stopPropagation();
			}
		}
    };
</script>
