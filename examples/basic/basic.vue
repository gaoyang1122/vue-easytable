<template>
    <div>
        基本的表格功能展示<br/><br/>
        <Easytable :width="tables.width"
                   :minWidth="tables.minWidth"
                   :height="tables.height"
                   :minHeight="tables.minHeight"
                   :titleHeight="tables.titleHeight"
                   :rowHeight="tables.rowHeight"
                   :columns="tables.columns"
                   :tableData="tables.tableData"
        ></Easytable>
    </div>
</template>

<script>

    import Easytable from '../../src/vue-easytable.vue'
    import mockData from '../../mockServer/data.js'
    //import mockData from '../../mockServer/simpleData'


    export default{
        name: 'basic',
        components: {
            Easytable
        },
        data(){
            return {
                tables: {
                    width: 1600,
                    minWidth: 600,
                    height: 450,
                    minHeight: 300,
                    titleHeight: 35,
                    rowHeight:25,
                    tableData: mockData,
                    columns: [
                        {fileld: 'ENDDATE', title: '截至日期', width: 180, align: 'center', isFrozen: true},
                        {fileld: 'TOTALSH', title: '股东户数(总户数)(户)', width: 200, align: 'center', isFrozen: true},
                        {fileld: 'DEC_HJCGSLZGB', title: '平均每户持股数(总股本)(股)', width: 230, align: 'center'},
                        {fileld: 'TOTALASH', title: '股东户数(A股户数)(户)', width: 230, align: 'center'},
                        {fileld: 'DEC_HJCGSLTA', title: '平均每户持股数(流通A股)(股)', width: 240, align: 'center'},
                        {fileld: 'DEC_QSMGDCGBLHJS', title: '前十名大股东持股比例合计数(%)', width: 250, align: 'center'},
                        {fileld: 'DEC_QSMGDCGBLHJS_LTGGD', title: '前十名流通股东持股比例合计数(%)', width: 250, align: 'center'},
                        {fileld: 'NOTICEDATE', title: '公告日期', width: 200, align: 'center'},
                        {fileld: 'DIFFER', title: '较上期变动(总户数)(户)', width: 180, align: 'center'},
                        {fileld: 'RATE', title: '增长率(%)', width: 150, align: 'center'}
                    ]
                    /*  columns: [
                     {fileld: 'id', title: '编号', width: 150, align: 'left',isFrozen:true},
                     {fileld: 'name', title: '名称', width: 150, align: 'center',isFrozen:true},
                     {fileld: 'cost', title: '成本价', width: 150, align: 'center',isFrozen:true},
                     {fileld: 'status', title: '状态', width: 150, align: 'center',isFrozen:false},
                     {fileld: 'price', title: '价格', width: 150, align: 'center',isFrozen:false},
                     {fileld: 'attr1', title: '属性', width: 150, align: 'center',isFrozen:false},
                     {fileld: 'color', title: '颜色', width: 150, align: 'center',isFrozen:true}

                     ]*/
                }
            }
        }
    }
</script>