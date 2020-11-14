**### offsetParent**

```javascript
ie7以上（不是火狐）    
    不论父级有没有定位，只要本身定位为fixed
           ==》 offsetParent:null
    本身定位不为fixed
         父级没有定位：
                ==》 offsetParent:body
         父级有定位：
                ==》offsetParent：定位父级 

  火狐
     不论父级有没有定位，只要本身定位为fixed
             ==》 offsetParent:body
      本身定位不为fixed
         父级没有定位：
               ==》 offsetParent:body
         父级有定位：
               ==》 offsetParent:定位父级


               
      即下面的结论：  
      
 IE7以上：
 
   不论父级有没有定位，只要本身定位为fixed
           ==》 offsetParent:null（ie7以上（不是火狐）  ）
            ==》 offsetParent:body（火狐）
  本身定位不为fixed（IE7以上的浏览器包括火狐）
         父级没有定位：
               ==》 offsetParent:body
         父级有定位：
               ==》 offsetParent:定位父级
                            
 如果body和html之间的margin被清掉了。IE7以下与IE7以上的结论相同
 
 
```

​        IE7以下，如果当前元素的某个父级触发了haslayout,那么offsetParent就会指向到这个触发了layout特性的父节点上（最常见的触发haslayout的属性就是  overflow: hidden;）


### 注意点
    
    1.分清parentNode和offsetParent的区别
        
        parentNode：直接父级

        offsetParent：类似于CSS的包含块

    2.offsetParent的作用：
       offsetLeft和offsetTop是参照于offsetParent的内边距边界的

    3.dom里所有的元素都是有offsetLeft和offsetTop的


