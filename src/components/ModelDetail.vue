<template>
    <el-container>
      <el-header>Header</el-header>
      <el-main>
          <div class="model-info">
            <span class="model-left">
              <img class="img" src="http://modeler.rtongcloud.com/base/api/file/target/pic/b5acc0ad44064a28928aa9c9b4775dd3"/>
              <el-button type="primary" class="model-button">立即使用</el-button>
              <el-button type="primary" class="model-button model-button-return">返回</el-button>
            </span>
            <div class="model-detal-info" >
              <div class="model-name"> GNN模型 </div>
              <div class="model-score"> 暂无评分 </div>
              <div class="model-other-info"> 更新时间: 2018-12-24 14:47 </div>
              <div class="model-other-info"> 模型描述: 这是一个对任意形态，任意结构面的切割 结构面要求是平面 如果是 </div>
              <div class="model-other-info"> 业务模型分类:河道洪水演算 </div>
              <div class="model-other-info"> 专业模型分类:无 </div>
            </div>
            <span class="model-version-info">
                <span>V1.0.0</span>
                <el-divider direction="vertical"></el-divider>
                <span>使用过136次</span>
            </span>

          </div>
          <el-tabs v-model="activeName" @tab-click="handleClick">
            <el-tab-pane label="模型概述" name="first">模型概述</el-tab-pane>
            <el-tab-pane label="参数说明" name="second">参数说明</el-tab-pane>
            <el-tab-pane label="bug反馈" name="third">bug反馈</el-tab-pane>
          </el-tabs>
      </el-main>
    </el-container>
</template>


<script>
export default {
    name: 'ModelDetail',
    data() {
      return {
        activeName: 'second'
      };
    },
    methods: {
      handleClick(tab, event) {
        console.log(tab, event);
      }
    }
  };
</script>

<style>
@import url("//unpkg.com/element-ui@2.12.0/lib/theme-chalk/index.css");
  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  .p {
    padding-top: 10px;
    padding-bottom: 10px;
  }

  .model-other-info {
    font-size: 12px;
    line-height: 30px;
  }

  .model-version-info {
    height: auto;
    display: flex;
  
    position: absolute;
    top: 20px;
    right: 20px;
  }

  .model-score {
    font-size: 19px;
    color: #FA9300;
    letter-spacing: 6px;
  }

  .model-name {
    font-weight: bold;
    font-size: 18px;
  }

  .model-detal-info {
    width: auto;
    text-align: left;
    line-height: 35px;
  }

  .model-info {
    width: auto;
    display: flex;
    padding-bottom: 20px;
    flex-direction: row;
  }

  .model-left {
    width: 200px;
    
  }

  .el-main {
    background-color: #ffffff;
    color: #333;
    text-align: center;
    margin-top: 30px;
    margin: auto;
    width: 1170px;
    position: relative;
  }

  .model-button {
    width: auto;
    margin-top: 20px;
    text-align: center;
    font-size: 12px;
    padding-top: 8px;
    padding-left: 15px;
    padding-right: 15px;
    padding-bottom: 8px;
  }

  .model-button-return {
    background: #bbb;
    border-color: #bbb
  }

  .img {
    width: 140px;
    height: 140px;
    border: 1px solid #eee;
    border-radius: 5px;
  }


</style>
