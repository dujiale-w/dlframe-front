<template>
  <!-- <nav>
    
    <el-button>Default</el-button>
    <el-button type="primary">按钮</el-button>
  </nav> -->
  <div>
    <el-container>
      <el-header style="background-color:yellowgreen">
        <p>选择数据集：</p>
        <el-select v-model="value1" placeholder="请选择" style="position: absolute ;left:120px ;top:20px;">
          <el-option v-for="item in options1" :key="item.value" :label="item.label" :value="item.value"
            :disabled="item.disabled" />
        </el-select>
        <p style="position:absolute ;left:370px ;top:10px;">选择算法：</p>
        <el-select v-model="value2" placeholder="请选择" style="position: absolute ;left:450px ;top:20px;">
          <el-option v-for="item in options2" :key="item.value" :label="item.label" :value="item.value"
            :disabled="item.disabled" />
        </el-select>
      </el-header>
    </el-container>
  </div>
  <el-row :gutter="20">
    <el-col :span="12">
      <div class="grid-content ep-bg-purple" />
      <p></p>
      <p></p>
      <div class="header">
        
 <el-button type="success" round style="position:absolute ; right:55% ;top:11%  " >执行算法</el-button>
      </div>   
       <!--  <headers title="新建记录"></headers> -->
        <el-input v-model="textarea" :rows="8" type="textarea" placeholder="Please input" />
      
    </el-col>
    <el-col :span="12">
      <div class="grid-content ep-bg-purple-light" />
      <p></p>
      <p></p>
      <div class="header">
        <el-button type="info" round style="position:absolute ; left:55% ;top:11%  " >结果显示</el-button>
      </div>
      
      <el-input v-model="textarea" disabled :rows="8" type="textarea" />
    </el-col>
  </el-row>

</template>

<!-- <script lang="ts"> 
export {
  name:'v-header',
  data(){
    return{}
  },
}
</script> -->

<script lang="ts" setup >
import { ref } from 'vue'
import {
  Check,
  Delete,
  Edit,
  Message,
  Search,
  Star,
} from '@element-plus/icons-vue'

name: 'v-header'


const textarea = ref('')


const value1 = ref('')
const value2 = ref('')
const options1 = [
  {
    value: '鸢尾花数据集',
    label: '分类数据集',
  },
  {
    value: 'Option2',
    label: 'Option2',
    disabled: true,
  },
  {
    value: 'Option3',
    label: 'Option3',
  },
  {
    value: 'Option4',
    label: 'Option4',
  },
  {
    value: 'Option5',
    label: 'Option5',
  },
]

const options2 = [
  {
    value: '线性回归算法',
    label: '分类数据集',
  },
  {
    value: 'Option2',
    label: 'Option2',
    disabled: true,
  },
  {
    value: 'Option3',
    label: 'Option3',
  },
  {
    value: 'Option4',
    label: 'Option4',
  },
  {
    value: 'Option5',
    label: 'Option5',
  },
]

/* export default{
  name: "HelloWorld"
} */
</script>

<style scoped>
/*文本域*/
.text-area {
  width: 100%;
  border-top: 1px solid gainsboro;
  border-bottom: 1px solid gainsboro;

}

.text-area textarea {
  width: 100%;
  margin: 0.75rem 0;
  border: none;
  outline: none;
  padding-left: 1.125rem;
  height: 6.5rem;
}

.text-area textarea::-webkit-input-placeholder {
  color: #9E9E9E;

}

.header {
  height: 50px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  /* align-items: center; */
  font-size: 30px;
  background: #d8dbd5;

}
</style>