background-clip:padding-box  防止背景入侵边框

box-shadow:som,som,som; 可以创建任意数量的投影

outline 和border类似  有一个outline-offset 可以指定他和元素之间的距离

background-position  可以指定背景任意方向上的任意偏移距离  如：background-position: left 10px right 20px  top 10px ;

background-position偏移量是跟随默认的 background-origin：padding-box; 偏移的  如果要让其跟随内容偏移 应该background-origin：content-box;

calc() 计算属性 

background：linear-gradient() 背景渐变 可以是定任意数量的条纹属性（可以在linear-gradient属性中添加【to right】属性改变文理方向如：横向条纹，纵向条纹）(在linear-gradient属性中添加【xdeg】使其旋转变成斜向纹理)  指定背景大小 background-size：宽 高；

还有更多更复杂的纯css3背景 详见 http://bennettfeely.com/gradients/

border-radius属性 可以指定任意方向角的圆角参数可以是、固定值、百分数、也可以是分数、 该属性常用来做圆形 圆角 椭圆

平行四边形 用transform：skewX（xdeg） 来实现  需要注意的是 该属性变形的是整体。如只需要外部包裹层变形 需要在内部有一个反变形

可以使用伪元素模拟形变 需要注意的是要将伪元素的层级设置为-1 来避免将元素遮盖

图剪裁属性clip-path：polygon（指定剪裁区域 可以是百分数，也可以是精确的数字） 用于处理图像 可以给一张图片设置切角样式

网页中切角很常见实现方式使用linear-gardent属性指定切角方向  

transform属性可以实现很多的形变效果，放大缩小scale（），旋转routate（），扭曲skew（），2D变换perspective（）可以实现梯形

利用伪元素和形变transform属性可以实现饼图  例子：饼图

元素投影box-shadow    可以指定五个参数 1、左右偏移 2、上下偏移 3、模糊半径 4、扩张半径 5、投影颜色   可以设置多个投影

投影并不适用于所有的情况 如果投影元素有半透明背景、切胶效果、通过chip-path生成的形状 都不太实用这时可以用filter滤镜来实现

