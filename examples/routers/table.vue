<template>
    <div>
        <div style="height:300px;width: 500px;display: flex;flex-direction: column;display: -moz-flex; -moz-flex-direction:column">
            <div>sdfdsfdsf</div>
            <Table style="flex: 1;-moz-flex:1;height: 100%;" border :columns="columns2" :data="data4"
                   @on-select="select"
                   @on-row-click="a"
                   @on-select-row-click="b"
                   @on-unselect="c"
                   @on-select-all="a"
                   ref="table"></Table>
            <!--<scrollbar ref="scroll" style="flex: 1;width: 100%">-->
            <!--<div style="background: darkseagreen;width: 800px;height: 400px"></div>-->
            <!--</scrollbar>-->
            <div @click="refresh" style="background: red">刷新</div>
        </div>

        <div style="height: 500px">


        </div>

    </div>


</template>
<script>
	export default {
		data () {
			return {
				columns2: [
					{
						type: 'selection',
						width: 60,
						align: 'center'
					},
					{
						title: '姓名',
						key: 'name',
						width: 100,
//						fixed: 'left',
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
						width: 100
					},
					{
						title: '省份',
						key: 'province',
						width: 100
					},
					{
						title: '市区',
						key: 'city',
						width: 100
					},
					{
						title: '地址',
						key: 'address',
						width: 200
					},
					{
						title: '邮编',
						key: 'zip',
						width: 100,
						render: (h, params) => {
							return h('Poptip', {
								props: {
									trigger: 'click'
								},
								scopedSlots: {
									content: props => h('div', [h('p', 'POS机品牌公司：联迪'), h('p', 'POS机型号：LANDI APOS A8'), h('p', 'POS机类型：智能机')])
								}
							}, '查看');
						}
					},
					{
						title: '操作',
						key: 'action',
//						fixed: 'right',
						width: 120,
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
				data4: [
					{
						name: '王小明',
						age: 18,
						address: '北京市朝阳区芍药居',
						province: '北京市',
						city: '朝阳区',
						zip: 100000
					},
					{
						name: '张小刚',
						age: 25,
						address: '北京市海淀区西二旗',
						province: '北京市',
						city: '海淀区',
						zip: 100000
					},
					{
						name: '李小红',
						age: 30,
						address: '上海市浦东新区世纪大道',
						province: '上海市',
						city: '浦东新区',
						zip: 100000
					},
					{
						name: '周小伟',
						age: 26,
						address: '深圳市南山区深南大道',
						province: '广东',
						city: '南山区',
						zip: 100000
					},
					{
						name: '王小明',
						age: 18,
						address: '北京市朝阳区芍药居',
						province: '北京市',
						city: '朝阳区',
						zip: 100000
					},
					{
						name: '张小刚',
						age: 25,
						address: '北京市海淀区西二旗',
						province: '北京市',
						city: '海淀区',
						zip: 100000
					},
					{
						name: '李小红',
						age: 30,
						address: '上海市浦东新区世纪大道',
						province: '上海市',
						city: '浦东新区',
						zip: 100000
					},
					{
						name: '周小伟',
						age: 26,
						address: '深圳市南山区深南大道',
						province: '广东',
						city: '南山区',
						zip: 100000
					}
				]
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
				console.log(val)
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
			refresh(){
				this.$refs.table.$refs.tbody.$refs.scrollbars.calculateSize();
//				this.$refs.scroll.calculateSize();
			}
		},
		mounted(){
//			console.log('我是table视图')
//            console.log(this.$refs.table.getdata())
//            console.log(this.$refs.table.getButtom())
			this.$nextTick(() => {
//            	this.$refs.scroll.calculateSize();
//	            this.$refs.table.$refs.tbody.$refs.scrollbars.calculateSize();
			});

		}
	};
</script>
<style>
</style>
