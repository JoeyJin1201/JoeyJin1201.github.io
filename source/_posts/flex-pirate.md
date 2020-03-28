---
title: Flex 其實沒有想像中複雜(初級20題)
abbrlink: 3200182051
date: 2020-03-27 14:33:38
categories:
  - css
tags:
  - Flex
  - CSS
  - Practice
---

首先要感謝的是六角學院的用心栽培以及大量的付出及回饋

光是一個`Flex`居然還做了合計幾十關的[遊戲](https://hexschool.github.io/flexbox-pirate/index.html#/)免費提供學員們練習

以下是我自己練習並紀錄過程，真心想學好`Flex`的話，還是建議自己跑過一次流程哦！


<!-- more -->

<br/>

![轉載自 卡斯伯's Blog](https://i.imgur.com/VZWAEA4.png)

>偉大的`Flex`系統主要分為`交錯軸(垂直)`和`主線軸(水平)`
>由這兩大軸線系統就能夠組合出既完美又精準且方便的排版模式
>好`Flex` 不學嗎？

* 小小概念

    屬性`display`中之值`block`<font color="#FF0000">會</font>讓元素換行。
    屬性`display`中之值`inline`<font color="#FF0000">不會</font>讓元素換行。
    `flex`中的`交錯軸(垂直)`預設排列方是為<font color="#FF0000">由左至右</font>。
    `flex`中的`主線軸(水平)`預設排列方式為<font color="#FF0000">由上至下</font>。

    * 第一題
    
    把`display`的值換成`flex`就會預設由左至右排列。

    {% codeblock lang:css %}
    .aims {
      display:flex;
    }
    {% endcodeblock %}

    <br/>

* 第一類題

    這邊會需要用到一個的屬性`justify-content`來決定元素根據`交錯軸(垂直)`所呈現的位置。

    * 第二題

    而`flex-end`這個值會讓元素貼齊`交錯軸(垂直)`預設最右上方之終點位置。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      justify-content: flex-end;
    }
    {% endcodeblock %}

    * 第三題

    而`center`這個值就是讓元素根據`交錯軸(垂直)`預設定位在上方正中心位置。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      justify-content: center;
    }
    {% endcodeblock %}

    * 第四題

    而`space-around`這個值會讓元素根據`交錯軸(垂直)`等距分散排列，並且會預設對齊上方左右並各留下一些空白。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      justify-content: space-around;
    }
    {% endcodeblock %}

    * 第五題

    而`space-between`這個值會讓元素根據`交錯軸(垂直)`等距分散排列，並且會預設完全貼齊上方左右位置。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      justify-content: space-between;
    }
    {% endcodeblock %}

* 第二類題

    這邊會需要用到一個的屬性`align-items`來決定元素根據`主線軸(水平)`所呈現的位置。
    
    * 第六題
    
    而`flex-end`這個值會讓元素貼齊`主線軸(水平)`最左下方之終點位置。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      align-items: flex-end;
    }
    {% endcodeblock %}

    * 第七題

    而`center`這個值會讓元素根據`主線軸(水平)`預設來貼齊最左正中間之位置。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      align-items: center;
    }
    {% endcodeblock %}

* 混合類題

    * 第八題

    利用`justify-content: center`以及`align-items: center`即可讓元素在`交錯軸(垂直)`與`主線軸(水平)`上完美置中。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    {% endcodeblock %}

    * 第九題

    利用`justify-content: space-between`讓元素在`交錯軸(垂直)`左右貼齊，再以`align-items: flex-end`即可讓元素在`主線軸(水平)`貼齊下方。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
    }
    {% endcodeblock %}

    * 第十題

    利用`flex-wrap: wrap`讓元素在超出容器的情況下換行顯示。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-wrap: wrap;
    }
    {% endcodeblock %}

    * 第十一題

    利用`flex-wrap: wrap-reverse`的方式讓元素在超出容器的情況下進行反向換行顯示。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-wrap: wrap-reverse;
    }
    {% endcodeblock %}

    * 第十二題

    利用`flex-wrap: wrap`讓元素在超出容器的情況下換行顯示，再將`flrx-start`這個值放入`align-content`屬性中把元素移至`Flex`開始排列的位置接著顯示，而非由`主線軸(水平)`開始排列顯示。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-wrap: wrap;
      align-content: flex-start;
    }
    {% endcodeblock %}

    * 第十三題

    利用`flex-wrap: wrap`讓元素在超出容器的情況下換行顯示，下方的三個元素以`交錯軸(垂直)`的特性設定來`justify-content: center`，再利用`主線軸(水平)`的特性來設定`align-content: space-between`即可以完成。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      align-content: space-between;
    }
    {% endcodeblock %}

    * 第十四題

    利用`flex-direction: column`讓flex預設的排列方向由左至右變成由上至下顯示。
    <small><font color="#FF0000">提示:更改為直向排列後，主線軸(水平→垂直)與交錯軸(垂直→水平)位置會調換</font></small>
    由於主線軸及交錯軸位置調換的關係，故接下來要使用`align-items`而不是使用`justify-content`才能正常使用。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      align-items: center;
      flex-direction: column;
    }
    {% endcodeblock %}

    * 第十五題

    利用`flex-direction: column`讓flex預設的排列方向由左至右變成由上至下顯示，並且以`justify-content: center`來完成排列顯示。

    {% codeblock lang:css %}
    .aims {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    {% endcodeblock %}

    * 第十六題

    利用`flex-direction: column`讓flex預設的排列方向由左至右變成由上至下顯示，並且以`flex-wrap: wrap`讓元素在超出容器的情況下換行顯示，再以`justify-content: center`來完成排列顯示。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
    {% endcodeblock %}

    * 第十七題

    利用`flex-direction: column`讓flex預設的排列方向由左至右變成由上至下顯示，並且以`flex-wrap: wrap-reverse`讓元素在超出容器的情況下反向換行顯示，接著以`align-content: spacebetween`來完成排列顯示。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap-reverse;
      align-content: space-between;
    }
    {% endcodeblock %}

    * 第十八題

    利用`flex-direction: column`讓flex預設的排列方向由左至右變成由上至下顯示，並且以`justify-content: space-around`讓上下留白即可完成顯示。

    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap-reverse;
      align-content: space-between;
    }
    {% endcodeblock %}

    * 第十九題

    利用`flex-direction: column-reverse`讓flex預設的排列方向由左至右反向變成由下至上顯示，並且以`flex-wrap: wrap-reverse`讓元素在超出容器的情況下反向換行顯示，接著以`align-content:flex-start`來貼齊`主線軸(垂直)`的起始點，即可以完成顯示。
    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-direction: column-reverse;
      flex-wrap: wrap-reverse;
      align-content: flex-start;
      justify-content: center;
    }
    {% endcodeblock %}

    * 第二十題

    利用`flex-direction: row-reverse`讓flex預設的排列方向由左至右反向變成由右至左顯示，並且以`justify-content:center`讓元素置中`主線軸(水平)`，接著以`align-items:center`讓元素置中`交錯軸(垂直)`，即可以完成顯示。
    {% codeblock lang:css %}
    .aims {
      display: flex;
      flex-direction: row-reverse;
      justify-content: center;
      align-items: center;
    }
    {% endcodeblock %}

    <br>
    <br>

    ![Happy Ending!](https://i.imgur.com/u8AmwTp.png)
    
    <small><font color="#cccccc">順帶一提，這個遊戲計算時間是使用localStorage的技術，為了我的面子，請容許我將通關時間給改掉哈哈XD</font><small>