<template>
    <div>
      <div class="frame">
        <button @click="selectVideo">选择视频</button>
        <label>{{ selectedVideo }}</label>
      </div>
      <div class="frame">
        <label>参考物与起跳板距离:</label>
        <input type="text" v-model="referenceDistance" @input="validateInput" />
        <label>m</label>
        <button @click="startTracking" :disabled="!canStartTracking">开始测算助跑速度</button>
      </div>
      <div class="frame">
        <label>处理进度：</label>
        <progress :value="progress" max="100"></progress>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedVideo: '',
        referenceDistance: '',
        progress: 0,
      };
    },
    computed: {
      canStartTracking() {
        return this.selectedVideo !== '' && this.referenceDistance !== '';
      },
    },
    methods: {
      selectVideo() {
        // 使用Vue插件或自定义的文件选择对话框组件来选择视频文件
        // 设置this.selectedVideo的值
      },
      validateInput() {
        // 在此处验证输入，并更新this.referenceDistance的值
      },
      startTracking() {
        // 执行长跳追踪操作
        // 更新this.progress的值以显示处理进度
      },
    },
  };
  </script>
  
  <style scoped>
  .frame {
    padding: 20px;
  }
  </style>
  