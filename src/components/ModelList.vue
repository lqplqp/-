<template>

    <el-container >
        <el-header>Header</el-header>
        <el-container class="main-area" >
            <el-main>
                <el-row :gutter="20" >
                    <p v-for="model in models">
                        <el-col :span="5">
                            <span class="grid-content bg-white">
                                <img class="content-image" src="http://modeler.rtongcloud.com/base/api/file/target/pic/b5acc0ad44064a28928aa9c9b4775dd3"/>
                                <div class="content-title">{{ model.modelName }}</div>
                                <div class="content-use-count">使用了 {{ model.useCount }} 次</div>
                                <p class="content-model-des">模型简介: {{ model.modelDes }}</p>
                            </span>
                        </el-col>
                    </p>
                </el-row>
            </el-main>
            <span>
                <el-aside>
                  <p v-for="modelType in modelTypes">
                      <el-link type="primary">{{ modelType.typeName }}类模型 
                            <span class="badge">{{ modelType.typeNums }}
                            </span>
                      </el-link>
                  </p>
            </el-aside>
            </span>

        </el-container>
        <el-footer>
          <el-pagination
            background
            layout="prev, pager, next"
            :total="1000">
          </el-pagination>
        </el-footer>
    </el-container>
    
    
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
        models: [
            {
                modelName: 'GNN',
                useCount: '123',
                modelDes: 'GNN模型是一个图神经网络模型GNN模型是一个图神经网络模型GNN模型是一个图神经网络模型GNN模型是一个图神经网络模型GNN模型是一个图神经网络模型',
            },
            {
                modelName: 'CNN',
                useCount: '1',
                modelDes: 'CNN是一个依赖于卷积神经网络的模型',
            },
            {
                modelName: 'RNN',
                useCount: '6',
                modelDes: 'RNN是一个以来于递归神经网络的模型',
            },
            {
                modelName: 'RNN',
                useCount: '6',
                modelDes: 'RNN是一个以来于递归神经网络的模型',
            },
            {
                modelName: 'RNN',
                useCount: '6',
                modelDes: 'RNN是一个以来于递归神经网络的模型',
            }
        ],
        modelTypes: [
            {
                typeName: "A",
                typeNums: '10'
            },
            {
                typeName: "B",
                typeNums: '2'
            },
            {
                typeName: "C",
                typeNums: '7'
            },
            {
                typeName: "A",
                typeNums: '10'
            },
            {
                typeName: "B",
                typeNums: '2'
            },
            {
                typeName: "C",
                typeNums: '7'
            },
        ]
    }
  }
}
</script>

<style>
@import url("//unpkg.com/element-ui@2.12.0/lib/theme-chalk/index.css");

  .el-row {
    margin-bottom: 20px;
    background: #eee;
    padding-left: 20px;
    padding-right: 20px;
  }

  .badge {
    background-color: #5CB85C;
    color: #fff;
    font-family: 'Open Sans';
    font-size: 11px;
    text-align: center;
    font-weight: 600;
    padding-left: 7px;
    margin-right: 10px;
    padding-right: 7px;
    text-shadow: none;
    border-radius: 10px;
    float: right;
  }



  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }


  .el-aside {
    background-color: #fff;
    color: #333;
    margin-top: 60px;
    text-align: center;
    width: 80px;
    line-height: 20px;
    height: auto;
    margin-right: 120px;
    border: 10px;
  }

  .main-area {
      background: #eee;
      padding-bottom: 20px;
  }

  .el-link {
      display: block;
      text-align: left;
      padding-top: 12px;
      padding-left: 20px;
      padding-bottom: 12px;
      color: #000;
      border-bottom: 1px solid #ddd;
  }

  .el-main {
    background-color: #eee;
    color: #333;
    text-align: center;
    margin-top: 20px;
  }

  .el-col {
    border-radius: 8px;
    margin-bottom: 15px;
    margin-right: 30px;
    background-color: #fff
  }

  .divider-css {
      color: #00ff00
  }

  .content-use-count {
      color: #fa9700;
      font-size: 14px;
      text-align: right;
      margin-top: 5px;
      margin-right: 14px
  }

  .content-title {
      margin:0 auto;
      margin-top: 5px;
      line-height: 35px;
      text-align: center
  }

  .content-image {
      padding-top: 20px;
      width: 260px;
      height: 260px;
      margin: 0 auto
  }

  .content-model-des {
    font-size: 12px;
    color: #707070;
    height: 35px;
    line-height: 35px;
    margin-left: 10px;
    margin-right: 10px;
    width: 95%;
    text-align: center;
    overflow: hidden;
    border-bottom: 1px solid #dadada;
  }

  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-white {
    background: #fff;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    height: 420px;
    width: 260px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>
