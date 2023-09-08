# HTML5

## 1. DOCTYPE的作用？严格模式与混杂模式如何区分？它们有何意义？

- 作用：`<!DOCTYPE>`声明位于文档的最前面，处于`<html>`标签之前。告知浏览器以何种模式来渲染文档。
- 区分：
  - 严格模式的排版和JS运作模式是以该浏览器支持的最高标准运行的；
  - 在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作。
- 意义：DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现

## 2. 新特性

- 语义化标签：header、article、footer、nav、section、aside、hgroup、source、command、datalist、details、dialog
- 本地化存储：localStorage、sessionStorage
- 离线应用、离线缓存：manifest
- 拖拽以及释放的api：Drag and drop
- 媒体播放：video、audio
- 增强表单控件：calendaer、data、time、email、url、search
- 地理位置：Geolocation
- 多任务：webworker
- 全双工通信协议：websocket
- 历史管理：history
- 跨域资源共享（CORS）:Access-Control-Allow-Origin
- 页面可见性改变事件：visibilitychange
- 跨窗口通信：PostMessage
- From Data 对象
- 绘画：canvas

## 3. 移除元素

- 纯表现的元素：basefont、big、font、center、s、strike、tt、u
- 对可用性产生负面影响的因素：frame、frameset、noframes

## 4. 对HTML语义化的理解

- HTML语义化让页面的内容结构化，结构更清晰，便于对浏览器、搜索引擎解析；
- 即使在没有css样式的情况下，也能以一种文档格式显示，并且是容易阅读的；
- 有利于SEO；
- 便于阅读理解。

## 5. 页面导入样式时，使用link和@import的区别

- link属于XHTML标签，而@import是css提供的；
- link与页面同时加载，@import引用的css文件需等到页面加载完成之后在加载；
- link方式的样式的权重高于@import。

## 6.a标签target属性的取值及作用

- _self：默认属性值。当前窗口打开；
- _blank：打开新窗口；
- _parent：在父窗口打开；
- _top：在顶层框架中打开。

## 7. 一个网页从开始请求到最终显示的完整过程

&emsp;一个网页从开始请求到最终显示的完整过程一般可分为7个步骤：

- 在浏览器输入url；
- DNS解析；
- TCP三次握手；
- 发起HTTP请求；
- 返回请求资源；
- 渲染页面；
- TCP四次挥手。

## 8. async和defer的作用与区别

- 脚本没有defer或async，浏览器会立即加载并执行指定的脚本，也就是说不等待后续载入的文档元素，读到就加载并执行；
- defe属性表示延迟执行引入的JavaScript，即这段JavaScript加载时，HTML并未停止解析，这个过程是并行的。当整个document解析完毕后再执行脚本文件，在DOMContentLoaded时间触发之前完成。多个脚本按顺序执行；
- async属性表示异步执行引入的JavaScript,与defer的区别在于，如果已经加载好，就会开始执行，也就是说它的执行仍然会阻塞文档的解析，只是它的加载过程不会阻塞。多个脚本的执行顺序无法保证。
