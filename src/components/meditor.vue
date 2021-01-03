<template>
<div>
  <mynav/>
  <markdown @on-save="save" ref="md" 
             @on-change="changeImg" 
             :theme="theme" 
             :initialValue="initialValue" 
             :placeholderValue="placeholderValue"
             :height='1000'/>
</div>
</template>
<script>
import mynav from './nav.vue'
import markdown from 'vue-meditors'
export default {
  name: 'meditor',
  components:{ 
    markdown,
    mynav
  },
  props: {
    msg: String
  },
  data(){
    return{
      placeholderValue: "請輸入問題描述",
      initialValue: "",
      theme: 'OneDark'
    }
  },
  motheds:{
    saveMd(){
      console.log(this.$refs.handleSave)
      this.$refs.md.handleSave();
    },
    save(content){
      console.log("原始内容："+content.value);
      console.log("转义后的内容："+content.html);
      console.log("主题theme："+content.theme);
    },
    changeImg(files,callback){
      console.log(files)
      //图片上传
      var url = "";
      callback(url);//通过callback回调将图片地址返回
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
