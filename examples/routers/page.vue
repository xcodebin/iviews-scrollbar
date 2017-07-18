<template>
    <div style="margin: 100px;">
        <Page :total="300" showTotal showSizer show-elevator size="small" placement="top" pageTooltip
              @on-page-size-change="onPageSizeChange"
              @on-change="onchange"
        ></Page>

    </div>
</template>
<script>
    export default {
        methods: {
            onPageSizeChange() {
                console.log('1111');
            },
            onchange(){
                console.log('2222')
            }
        }
    };
</script>
