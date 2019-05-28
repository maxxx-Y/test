# 人脸识别签到小程序
## 进度
- **2019/5/25**  
  实现了学生上传或者拍摄图片到云存储，并结合腾讯云人脸识别完成了人脸信息检测与分析，展示了上传照片的魅力值
- **2019/5/26**  
  - 实现了管理员创建人员库的操作
  - 实现了验证创建的人员库名称和id是否存在的功能
- **2019/5/27**  
  修复学生登录功能
- **2019/5/28**  
  实现学生登陆后上传相片至人员库
## 遇到并解决的问题
- **2019/5/25**  
  在控制台删除云函数后，在本地修改后再次上传若失败可以在云函数根目录右键并选择同步云函数列表
- **2019/5/28**  
  - 本地云函数修改并保存后记得要上传至云
  - 获取创建人员接口的参数时报很多奇怪的错，发现是修改了const
  - 调用`wx.chooseImage()`后，`object.success`回调函数的参数`res`中的`attribute tempFilePaths`不是image或url
  - 用云文件ID换取真实链接的API是在服务端调用的，而非小程序端

## 准备
### 起步
1. [微信公众平台](https://mp.weixin.qq.com/)
2. [下载IDE](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)
3. [node.js](https://nodejs.org/en/)
4. [npm](https://www.w3schools.com/whatis/whatis_npm.asp)
5. [Vant Weapp小程序组件](https://youzan.github.io/vant-weapp/#/intro)
### 阅读
1. [微信小程序官方文档](https://developers.weixin.qq.com/miniprogram/dev/index.html?t=19051721)
2. [云开发官方文档](https://developers.weixin.qq.com/miniprogram/dev/wxcloud/basis/getting-started.html)
3. [学习node.js -en](https://www.w3schools.com/nodejs/)
4. [学习node.js -zh](https://nqdeng.github.io/7-days-nodejs/)
## 资料
### 人脸识别
1. [腾讯云人脸识别文档](https://cloud.tencent.com/document/product/867/17636)
2. [腾讯云人脸识别之<b>人脸验证</b>文档](https://cloud.tencent.com/document/product/867/32806)
3. [小程序使用腾讯云人脸检测](https://github.com/Techeek/WX_TencentAI_Face)
4. [小程序人脸识别](https://cloud.tencent.com/developer/article/1362842)
### 云开发
1. [云开发实现登录注册](https://juejin.im/post/5bbf08dfe51d450e92526f3e)
### Javascript async/await
1. [segmentfault - 理解同步异步和事件循环](https://segmentfault.com/a/1190000004322358)
2. [掘金 - 异步编程意识](https://juejin.im/post/5a8fc6345188257a804aa956)
3. [segmentfault - 理解async/await](https://segmentfault.com/a/1190000007535316)

