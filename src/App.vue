<template>
  <div class="app">
    <vueUploadFolderHy
      id="dropzone"
      ref="myDropzone"
      :parentId="parentId"
      :action="folderUrl"
      :options="dropzoneOptions"
      :useCustomSlot="true">
      <i class="el-icon-upload"></i>
      <div class="el-upload__text">将图片或者文件夹拖拽到此处上传，或者点击批量上传图片</div>
    </vueUploadFolderHy>
  </div>
</template>

<script>
import vueUploadFolderHy from 'vue-upload-folder-hy';

export default {
  name: 'app',

  components: {
    vueUploadFolderHy
  },

  data() {
    return {
      dropzoneOptions: {
        autoProcessQueue: false,
        url: 'xx', // 上传图片地址
      },
      parentId: 'xxx', // 如果你拖动文件夹里面还有图片 那要传一个id 
      folderUrl: 'xx' // 创建文件夹的地址
    };
  }
};
</script>


