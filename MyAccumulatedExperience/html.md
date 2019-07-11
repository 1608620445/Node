# 前台记录
_前台不是强项，但毕竟是要全栈的，至少得说的过去的吧，我要做山头最靓的仔_
![王之审视](html_files/1.jpg)
## Vue
### 问题汇总
1. Vue页面设置高度100%
``` vue
<!-- App.vue中style增加该样式 -->
html,body,#app{
    height: 100%;
}
```
2. Vue assets图片不能正常加载
vue在打包时只会将static下面的图片保留，assets目录下的图片会转换成base64，直接打包到js文件中，所以你用字符串是读取不到图片的，

``` vue
    <!-- dom使用-->
    <el-container :style="node">
    
    <!-- data中增加-->
    node: {
        backgroundImage: "url(" + require("../assets/login.jpg") + ")",
        backgroundRepeat: "no-repeat"
    }
```
## JavaScript
