<template>
  <div id="app">
    <div id="frame" style="-webkit-app-region: drag">
      <div class="frame-header">
        <div class="frame-title">RequestWechatTools</div>
        <ul class="frame-select"  style="-webkit-app-region: no-drag">
          <li><i class="el-icon-minus" @click="changeWindow('min-window')"></i></li>
          <li><i class="el-icon-full-screen" @click="changeWindow('max-window')"></i></li>
          <li><i class="el-icon-close" @click="changeWindow('close-window')"></i></li>
        </ul>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
  import { ipcRenderer } from 'electron'
  
  export default {
    name: 'RequestWechatTools',
    created: () => {
    },
    methods: {
      // 修改窗口操作
      changeWindow: (actionTag) => {
        console.log(ipcRenderer.send)
        console.log(ipcRenderer.send())
        console.log(ipcRenderer)
        console.log(actionTag)
        console.log(ipcRenderer.send(actionTag))
      }
    }
  }
</script>

<style>
  html,body,div,p,h1,h2,h3,h4,h5,h6,ul,li,ol {
    padding: 0;
    margin: 0;
  }
  ul,li,ol{
    list-style: none;
  }
  /* CSS */
  #frame {
    line-height: 1.875rem;
    padding:0 0.625rem;
    height: 1.875rem;
    overflow: hidden;
    border-bottom: 1px solid #C0C0C0;
    background: #2f9833;
    color:#ffffff;
  }
  .frame-title {
    display: inline-flex;
  }
  .frame-select {
    float: right;
  }
  .frame-select li {
    display: inline-block;
    margin: auto 0.5rem;
    cursor: pointer;
  }
</style>
