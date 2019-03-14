## flex作用于父级的6个属性：

### 1.flex-direction: 用于指定flex主轴的方向，继而指定flex子项在flex容器中的位置

    row: 默认值，水平方向从左到有排列
    row-reverse：与row相反
    column：垂直方向上从上到下排列
    column-reverse： 与column相反

### 2.flex-wrap：用于指定flex子项是否换行
    nowrap： 默认值，表示不换行，flex子项可能会溢出
    wrap：换行，溢出的子项会换到下一行
    wrap-reverse： 反方向换行

### 3.flex-flow：复合属性，是flex-direction与flex-wrap的简写

### 4.justify-content：用于指定主轴（水平方向）上子项的对齐方式
    flex-start: 默认值，与行的起始位置对齐
    flex-end： 与行的结束位置对齐
    center： 与行的中间对齐
    space-between： 表示两端对齐，中间间距相等；
      注意： 当子项有溢出或者只有一个子项的时候，等同于flex-start
    space-around： 表示间距相等，中间间距是两端的两倍；
    注意： 当子项溢出或只有一个子项的时候，等同于center

### 5.align-items：用于指定侧轴（垂直方向）上的对齐方式
    stretch： 默认值，当flex子项未设置高度或者高度为auto的时候，stretch起作用，将flex子项的高度设置为行的高度，这里需要注意的是，当flex子项只有一行的时候，此时，行的高度为容器的高度，即flex子项的高度为容器的高度
    flex-start： 表示与侧轴开始的位置对齐
    flex-end： 表示与侧轴结束的位置对齐
    center： 表示与侧轴中间对齐
    baseline： 表示与基线对齐，当所有子项的的基线在同一线上，此时等同于flex-start

### 6.align-content： 该属性只用于多行的情况下，用于多行的对齐方式
    stretch： 默认值，当flex子项未设置高度或者高度为auto的时候，此时，flex子项的高度为行高度
    flex-start： 表示各行与侧轴开始的位置对齐，第一行紧靠侧轴开始边界，之后的每一行紧靠前面一行
    flex-end： 表示各行与侧轴结束的位置对齐，最后一行紧靠侧轴结束边界，之后的每一行都紧靠前面一行
    center： 各行与侧轴中间对齐
    space-between： 表示两端对齐，中间间距相等。注意：当子项有溢出或者只有一行的时候，效果等同于flex-start
    space-around： 各行间距相等，中间间距是两端的两倍。注意：当子项有溢出或者只有一行的时候，效果等同于center


## flex作用于子项的6个属性：
### order： 该属性用于指定子项的排了顺序，数值越小越靠前，可以为负数
    取值： 默认值为0

### flex-grow： 用来指定flex子项的扩展比例，不可以为负数，flex容易会根据子项设置的扩展比例来分配剩余空间
    取值： 数值，默认值为0， 表示即使存在剩余空间，flex子项也不做扩展

flex-shrink： 用于指定flex子项的收缩比例，flex容器会根据子项设置的收缩比例来收缩各个子项
  取值： 数值，不可以为负数，默认值为1, 表示所有子项在有溢出的时候，等比例收缩
  注意： 该属性只有在不换行的情况下使用

flex-base： 基本用不上的东西

align-self： 基本等同于父项align-items