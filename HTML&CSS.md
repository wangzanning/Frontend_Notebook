- [给行内元素设置padding和margin是否有效](https://blog.csdn.net/qq_37621289/article/details/82859024)***[ ! important ]***

  对行内元素，左右设置优先，上下设置无效，包括padding-top/bottom, margin-top/bottom, 从显示效果上增加了，但其实设置无效，不影响周围的元素，盒子模型并未被撑开。（对img有效）

- [深度解析使用CSS单位px、em、rem、vh、vw、vmin、vmax实现页面布局](https://blog.csdn.net/weixin_33757609/article/details/94699419?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.control&dist_request_id=d20105fc-7810-4855-9627-597cddc2df8f&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.control)***[ ! important ]***

  vw, wh： 相对于视窗长宽的百分比

  vmin和vmax：vw和vh中较小和较大的那个

  建议综合 固定宽度、字体大小可用rem、px；其他可结合vw %

- [CSS层叠上下文、层叠等级、层叠顺序、z-index](https://juejin.cn/post/6844903667175260174)

  <img src="/Users/zanning/Library/Application Support/typora-user-images/image-20210630174509201.png" alt="image-20210630174509201" style="zoom:50%;" />

  

  首先先看要比较的两个元素是否处于同一个层叠上下文中：    1.1如果是，谁的层叠等级大，谁在上面（怎么判断层叠等级大小呢？——看“层叠顺序”图）。    1.2如果两个元素不在统一层叠上下文中，请先比较他们所处的层叠上下文的层叠等级。 2、当两个元素层叠等级相同、层叠顺序相同时，在DOM结构中后面的元素层叠等级在前面元素之上。

- [浅谈script标签中的async和defer](https://www.cnblogs.com/jiasm/p/7683930.html)

  defer会异步地按照顺序执行，async并不会按着`script`在页面中的顺序来执行，而是谁先加载完谁执行。

- [由 flex: 1引发的思考](https://blog.csdn.net/u013451157/article/details/79011679?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.control&dist_request_id=80a65e55-8c94-4f25-a50d-e06d36dd2cab&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.control)

  flex 是 `flex-grow`、`flex-shrink`、`flex-basis`的缩写。

  ```css
  .item {flex: 1;}
  .item {
      flex-grow: 1;
      flex-shrink: 1;
      flex-basis: 0%;
  }
  ```

- [响应式布局](http://caibaojian.com/356.html)***[ ! important ]***

  1. 设置 Meta 标签

  2. 通过媒介查询来设置样式 Media Queries

     ```css
     @media screen and (max-width: 980px) {
       #head { … }
       #content { … }
       #footer { … }
     }
     ```

- [行内元素和块状元素的区别](http://blog.sina.com.cn/s/blog_c112a2980102xsvd.html)

  当把行内元素设置为float:left/right后，该行内元素的display属性会被赋予block值，且拥有浮动特性。行内元素去除了中间莫名的空白。

- 

- 

- 

