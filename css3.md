# CSS3

## 1. 新特性

- CSS3选择器
  - 基本选项器
  - 属性选择器
  - 伪类选择器
- CSS3边框与圆角
  - 圆角 border-radius
  - 盒阴影 box-shadow
  - 边框背景图 border-image
- CSS3背景与渐变
  - rgba
  - 背景色渐变

  ```javascript
  //元素背景色从左到右由红色渐变成黄色（默认从上到下）
  #grad {
      background-image: liner-gradient(to right, red, yellow);
  }
  ```

- CSS3倒影
  - -webkit-box-reflect：方向(below/above/left/right) 距离;
- CSS3过渡
  transition：设置元素的过渡效果
  - transition-property：过渡属性名；
  - transition-duration：规定完成过渡效果需要花费的时间；
  - transition-timing-function：指定切换效果的速度；
  - transition-delay：指定何时将开始切换效果；
  - cubic-bezier(x1,y1,x2,y2)：贝塞尔曲线，是控制变化的速度曲线。
- CSS3变换
  - transform：应用于元素的2D或3D转换。这个属性允许将元素进行旋转、缩放、移动、倾斜等；
  - transform-origin：允许更换元素的位置。2D转换元素可以改变元素的X，Y轴。3D还可以更改元素的Z轴；
  - transform-style：指定嵌套元素是怎样在三维中呈现的；
  
  ```javascript
  //顺时针旋转7°
  div {
    transform: rotate(7deg);
  }
  ```

- CSS3动画
  - animation-name：@keyframe动画名称；
  - animation-duration：动画指定需要多少时间完成；
  - animation-timing-function：设置动画将如何完成一个周期；
  - animation-delay：设置动画启动前的延迟；
  - animation-iteration-count:定义动画的播放次数；
  - animation-direction：指定是否应该反向播放动画。
  
  ``` javascript
  //div元素从左到右移动200px，过程3s
  div {
    width: 100px;
    height: 100px;
    background-color: red;
    animation: move 3s;
  }
  @keyframes move {
    from {
        margin-left: 0px;
    }
    to {
        margin-left: 200px;
    }
  }
  ```
