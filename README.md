## flex布局使用总结
-------------------
容器开启弹性布局
```css
.box{
  display: flex;
}
```
设为 Flex 布局以后，子元素的float、clear和vertical-align属性将失效。

- 作用于容器的常用属性
    * flex-direction：决定主轴的方向，默认为row。
    * flex-wrap：是否换行。
    * flex-flow：flex-direction属性和flex-wrap属性的简写形式，默认值为row nowrap。
    * justify-content：项目在主轴上的对齐方式，默认flex-start。
    * align-items：项目在交叉轴上如何对齐，默认值为stretch，即如果项目未设置高度或设为auto，将占满整个容器的高度。
    * align-content：多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用，默认值为stretch。

- 作用于项目的常用属性
    * order：属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。
    * flex-grow：属性定义项目的放大比例，默认为0。
    * flex-shrink：项目的缩小比例，默认为1。
    * flex-basis：在分配多余空间之前，项目占据的主轴空间，默认值为auto，即项目的本来大小。
    * flex：flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto，后两个属性可选。
    * align-self：私有对齐方式，可覆盖align-items属性，默认值为auto。

    具体效果可运行flex.html文件查看。

## grid布局使用总结
-------------------
基本组成：
 * "容器"（container）：使用网格布局的区域。
 * "项目"（item）：容器内定位的子元素。
 * "行"（row）：容器内水平区域。
 * "列"（column）：容器内垂直区域。
 * "单元格"（cell）：容器内行与列交叉的区域。
 * "网格线"（grid line）：容器内划分网格的线。

容器开启网格布局
 ```css
.box{
  display: grid;
}
```
设为 grid 布局以后，子元素的float、vertical-align、display: inline-block和display: table-cell属性将失效。

- 作用于容器的常用属性
    * grid-template-columns：定义每一列的列宽。
    * grid-template-rows：定义每一行的行高。
    * grid-row-gap：设置行与行的间隔（行间距）。
    * grid-column-gap：设置列与列的间隔（列间距）。
    * grid-gap：是grid-column-gap和grid-row-gap的合并简写形式。
    * grid-template-areas：定义区域。
    * grid-auto-flow：元素会按照顺序自动放置在每一个网格，默认值是row（先行后列）。
    * justify-items：设置单元格内容的水平位置（左中右）。
    * align-items：设置单元格内容的垂直位置（上中下）。
    * place-items：是align-items属性和justify-items属性的合并简写形式。