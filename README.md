# mobileRepository
移动端开发知识库，常见的BUG整理和经验分享：

## 常见BUG

#### 移动端点击300ms延迟

**FastClick**

[FastClick](https://github.com/ftlabs/fastclick) 是 FT Labs 专门为解决移动端浏览器 300 毫秒点击延迟问题所开发的一个轻量级的库。FastClick的实现原理是在检测到touchend事件的时候，会通过DOM自定义事件立即出发模拟一个click事件，并把浏览器在300ms之后的click事件阻止掉。


## 页面优化

1. 页面文字字号/修饰（加粗不加粗）设定规范
2. 页面块/元素之前padding,margin预先设定规范
4. 常用颜色设置：主色，文字色，边框色等规范
5. **图片/头像**大小设定规范
6. 用户操作反馈设定规范
7. 页面UI元素: Button/Input/List等设定规范，使用BEM来封装组件。
8. 页面之间跳转**加载动画**设定规范
9. 表单基本验证提示。



## 前端性能优化

1. 前端小图片/ICON之类的做成雪碧图，2倍图使用`zoom`缩放
2. 页面图片懒加载
3. 必要的时候把**不常更换的图片**改成webp格式，减少HTTP请求
4. css库，js库压缩合并，经常修改的不合并
5. css文件放`</head>`前，JS放`</body>`前，在PHP项目开发中，为了方便经常把js写在页面里，常用js,比如jquery,都放在head里，这样会阻塞页面DOM的渲染，**建议**最好在公共的文件里定义一个底部solt，再写页面js的都放在这个slot里，就可以做到js文件放在`</body>`前了。
6. 

