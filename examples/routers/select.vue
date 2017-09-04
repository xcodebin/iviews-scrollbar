<template>
    <Row>
        <Col span="12" style="padding-right:10px">
        <Select v-model="model11" :disabled="false" filterable transfer>
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>
        </Col>
        <Col span="12">
        <Select v-model="model12" filterable :disabled="true" multiple>
            <Option v-for="item in cityList" :value="item.value" :key="item.value">{{ item.label }}</Option>
        </Select>
        </Col>
    </Row>
</template>
<script>
    export default {
        data () {
            return {
                cityList: [
                    {
                        value: 'beijing',
                        label: '北京市'
                    },
                    {
                        value: 'shanghai',
                        label: '上海市'
                    },
                    {
                        value: 'shenzhen',
                        label: '深圳市'
                    },
                    {
                        value: 'hangzhou',
                        label: '杭州市'
                    },
                    {
                        value: 'nanjing',
                        label: '南京市'
                    },
                    {
                        value: 'chongqing',
                        label: '重庆市'
                    },
                    {
                        value: '234',
                        label: '重庆市'
                    },
                    {
                        value: '234',
                        label: '重庆市'
                    },
                    {
                        value: '435',
                        label: '重庆市'
                    },
                    {
                        value: '456',
                        label: '重庆市'
                    },
                    {
                        value: '678',
                        label: '重庆市'
                    },
                    {
                        value: 'Z123',
                        label: '重庆市'
                    }
                ],
                model11: '',
                model12: []
            };
        }
    };
</script>
