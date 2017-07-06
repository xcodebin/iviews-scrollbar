<template>
    <div>
        <Poptip trigger="hover" confirm title="提示标题" content="提示内容">
            <Button>hover 激活</Button>
        </Poptip>
        <Poptip title="提示标题" content="提示内容">
            <Button>click 激活</Button>
        </Poptip>
        <Poptip trigger="focus" >
            <Button>focus 激活</Button>
            <i-input slot="content" placeholder="输入框的 focus"></i-input>
        </Poptip>
        <Poptip trigger="focus" title="提示标题" content="提示内容">
            <i-input placeholder="输入框的 focus"></i-input>
        </Poptip>
    </div>
</template>
<script>
    export default {

    }
</script>
