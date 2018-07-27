根据今天所学内容，我给出了
# 验证问题的自己的解答
- **盒模型的概念**  
block元素和inline-block元素具有盒模型的概念，而inline元素没有。盒模型就是将一个元素看做一个盒子，准确地说，是盒子本身：仅含border、padding、content。
盒子与盒子之间需要空间，这个空间不属于该元素，但属于盒模型，这个空间就是margin。合理控制border、padding、content、margin各个部分的大小，可使页面
易读美观。  

- **inline、block和inline-block的概念**    
inline、block、inline-block是display属性的属性值，由此区分出inline元素、block元素、inline-block元素。  
block元素具有盒模型，默认情况下独占一行或多行（由盒子大小决定），上下有换行。默认的block元素有：div、p、h1...h6、ol、ul、dl、table、address、blockquote、form。  
inline元素在block元素内存在，它们按照从左到右从上到下的顺序依次在block元素中排列。inline元素与元素之间默认没有间隙。inline元素虽然不具备盒模型，但是
允许为inline元素添加padding、border、margin，这里的padding、border、margin和盒模型中的意义相同，但是仍存在区别，区别主要在于添加了padding、border、margin
的inline元素对其他元素的影响，和block元素，以及inline-block元素是不同的。常见的inline元素有：img、code、em、strong、span、label。
inline-block元素既具有inline元素的特点，又具有block元素的特点。它首先“是”inline元素，它将存在于block元素的内部，同样地从上到下从左到右地排列。但是它又
像block元素那样，具有盒模型，可以有content、padding、border、margin这套完整的东西，因此可以将其他元素（包括inline-block元素和inline元素推开）。 
常见的inline-block元素有textarea,button,input、select。    

- **内外边距，宽度，高度，box-sizing等属性**    
内外边距的设置是尺寸方面的设置，利用padding属性和margin属性就可以实现。  
width和height同样是对盒模型尺寸方面的设置。当box-sizing属性为默认值content-box时，width和height属性对内容区的宽高进行设置；当box-sizing属性的属性值为
border-size时，width和height属性对整个盒子（包含border、padding、content）的宽高进行设置。  
box-sizing设为border-size时非常有利于布局（教训。。），想要调整元素内部的样式时不会对盒外以及整体布局产生影响。    

- **浮动，清除浮动**    
浮动是一种布局方式，特点尤其是能够让默认竖向排列的块级元素横向排列，通过:1、设置一元素为浮动元素，如：float: left; 2、该浮动元素在父元素范围内摆放； 3、
该浮动元素从文档流中删除； 4、其余非浮动的块级元素看不到浮动元素、该DOM中该浮动元素之后的浮动块级元素看到该元素、内联元素看到该元素； 5、看不到的元素将
自顾自地在父元素范围内排列，所以可能被浮动元素覆盖；看到的元素将避开、环绕着浮动元素排列。  
由于块级元素可能会被浮动元素覆盖，所以有时需要清除这种影响，方法是：给该块级元素添加clear属性。    

- **如何使用浮动进行布局**  
以下纯粹是我的个人经验，觉得还ok。  
1、确认浮动元素以及它的父元素是哪个（些），计划怎样让浮动元素在父元素范围内布局。  
2、按照设计好的布局，给浮动元素添加float属性，box-sizing属性和width属性。**注意**width属性一定要加上，而且以百分比为单位，而且
横向摆放的几栏都要以百分比为单位设置width属性，而且所有横向的栏加起来不要超过100%。否则会造成随着浏览器窗口的改变，浮动元素
需要的空间不足，因而换行移动的混乱情况。**并且**box-sizing属性最好加上，因为浮动元素布局很容易乱，box-sizing能够起很大帮助。  
3、浮动元素的高度不能像flexbox一样自动拓展，这个有时很不方便，目前也没有很好的解决办法。。    


**All rights reserved.**
