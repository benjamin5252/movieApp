<template>
  <div class="filetrans-modal">
    <div class="filetrans-header"><div class="filetrans-header-inner">Header</div></div>
    <div class="filetrans-content">
      <div class="home-indicator">
        Home
      </div>
      <div class="file-dialog">
        <div class="file-body">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Incidunt, fugiat distinctio maxime fugit molestias aperiam soluta. Sit illo, perferendis eaque officia quasi obcaecati quaerat est atque provident qui maiores, modi rem eius iste ea molestias numquam placeat facilis. Quod molestiae fuga fugiat itaque aut facere sunt voluptatum eaque? Vero facere explicabo, debitis velit dolorum consequatur repellat. Ut quia numquam sint aliquid, debitis magnam accusantium quis repellat, delectus facilis dolorem ad quas! Nihil est dolor fuga iusto. Tenetur ipsum aut nostrum esse at odio nulla ut hic, mollitia recusandae veritatis repellat. Veritatis voluptatum consequuntur dicta quibusdam numquam accusamus excepturi sapiente in. Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum itaque quaerat ipsam tempore in nam ipsa suscipit quia. Earum assumenda optio temporibus aut itaque similique accusantium esse delectus totam officia.</div>
      </div>
    </div>
    <div class="filetrans-btns">
      <div class="btn btn-createfolder"><div class="btn-inner">Create folder</div></div>
      <div class="btn btn-cancel"><div class="btn-inner">Cancel</div></div>
      <div class="btn btn-movehere"><div class="btn-inner">Move here</div></div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import '@/assets/style_acs.css';
import {
  defineComponent,
  reactive, //賦值 type[obj,arr]
  ref, //賦值 type[int,bool,str,obj,arr] 使用 value 呼叫
  onMounted, //渲染後載入
  onBeforeMount, //渲染前載入
  onUpdated, //渲染完成後載入
  useAsync, //同步
  computed, //計算
  watch,
} from '@nuxtjs/composition-api';

export default defineComponent({
  head() {
    return {
      title: 'Amaryllo Cloud',
      link : [
        {
          hid : 'icon',
          rel : 'icon',
          type: 'image/x-icon',
          href: '/image_2021_03_03T01_13_08_067Z.png',
        },
      ],
    };
  },

});
</script>

<style lang="scss" scoped>
.filetrans-modal{
  color: #000;
  background-color: #fff;
  width: 500px;
  position: fixed;
  z-index: 100;
  left: 50%;
  top: 20%;
  transform: translate(-50%, -50%);
  .filetrans-header{
    font-size: 16px;
    height: 30px;
    color: #fff;
    background-color: #f08300;
    .filetrans-header-inner{
      padding-left: 12px;
      line-height: 30px;
    }
  }
  .filetrans-content{
    
    .home-indicator{
      padding-left: 20px;
      padding-top: 10px;
      padding-bottom: 10px;
    }
  }
  .file-dialog{
      width: 460px;
      padding-top: 10px;
      padding-bottom: 30px;
      margin: 0 auto;
      overflow-y: initial !important;
      overflow-y: scroll; 
      max-height: 20%;  
      .file-body{
      height: 200px;
      overflow-y: auto;
    }
  }
  .filetrans-btns{
    display: flex;
    width: 460px;
    margin: 0 auto;
    .btn{
      padding-left:10px;
      padding-right:10px;
      width: auto;
      line-height: 30px;
      margin: 0 10px;
      height: 30px;
      background-color: #E8E8E8;
      &.btn-createfolder{
        background-color: #F08300;
      }
      
    }
    
  }
  
}
</style>
