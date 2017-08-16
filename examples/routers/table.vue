<template>
    <Scrollbar class="scrollbar">
        <div class="scroll-me">
            <!--<Button type="primary" @click="">qweqeqwe</Button>-->
            <Modal v-model="aaaa" width="700">
                <Table width="550" height="200" border :columns="columns2" :data="data4"
                       @on-select="select"
                       @on-row-click="a"
                       singleCheck
                       @on-select-row-click="b"
                       @on-unselect="c"
                       ref="table"></Table>
            </Modal>
        </div>
    </Scrollbar>

</template>
<script>
    export default {
        data () {
            return {
                aaaa:true,
                columns2: [
                    {
                        type: 'selection',
                        width: 60,
                        align: 'center'
                    },
                    {
                        title: '姓名',
                        key: 'name',
                        width: 300,
//                        fixed: 'left'
		                render: (h, params) => {
							return h('div', [
								h('Icon', {
									props: {
										type: 'person'
									}
								}),
								h('strong', params.row.age)
							]);
						}
                    },
                    {
                        title: '年龄',
                        key: 'age',
                    },
                    {
                        title: '省份',
                        key: 'province',
                    },
                    {
                        title: '市区',
                        key: 'city',
                    },
                    {
                        title: '地址',
                        key: 'address',
                    },
                    {
                        title: '邮编',
                        key: 'zip',
                    },
                    {
                        title: '操作',
                        key: 'action',
//                        fixed: 'right',
                        render: (h, params) => {
                            return h('div', [
                                h('Button', {
                                    props: {
                                        type: 'text',
                                        size: 'small'
                                    }
                                }, '查看'),
                                h('Button', {
                                    props: {
                                        type: 'text',
                                        size: 'small'
                                    }
                                }, '编辑')
                            ]);
                        }
                    }
                ],
                data4: []
            };
        },
        methods: {
            select(a, b, c, d){
//                console.log(this.$refs.table.getdata());
                console.log(a)
                console.log(b)
                console.log(c)
                console.log(d)
            },
            a(val){
//                console.log(val)
            },
            b(val){
                console.log(1)
                console.log(val)
            },
            c(a, b, c, d){
            //                console.log(this.$refs.table.getdata());
                console.log(a)
                console.log(b)
                console.log(c)
                console.log(d)
            },
        },
        mounted(){
        	console.log('我是table视图')
//            console.log(this.$refs.table.getdata())
//            console.log(this.$refs.table.getButtom())
            this.$refs.table.$refs.tbody.$refs.scrollbars.reset()
        }
    };
</script>
<style>
body{
    height:500px;
}
    .scrollbar {
        width: 100%;
        height: 300px;
    }

    .scroll-me {
        width: 500px;
        height: 600px;
        background-color: #00c261;
    }
</style>
