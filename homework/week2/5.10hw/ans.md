1. jd.css中line14 - 20, 已经注释了一句话， 如果再用ctrl + /注释掉整段就会出错了，怎样可以解决？
	
	```
	答，css的注释：/**/	；所以先将已经注释的内容释放，然后注释整段；保证被注释的内容被/**/包括
	```
	
2. jd.css中line66, div0属性中top: 30px一定要设置， 不然它的位置就不对了， 
	因为是相对于li0(父亲)的位置，但是line 192, div3中top不用设置位置也没有问题， 为什么？

	```
	答：line66设置top的原因，你将.oversea的a标签设置为了float属性，脱离了文档流
	```
	
3. jd.css中line455用到了::before, 不太明白它的用法；而且position:absolute应该是相对于父亲(li0的位置)，
	这里为什么设置成top:-1px, left: 0px，感觉是相对于自身(div0)
	
	```
   答:
	before属于伪类选择器；这个学习内容将在下节课具体讲解，这里就简介一下：向选定的元素前插入内容；
	
	这里.div0::before将伪类选择器设置为position，则它相对的元素为div0
	```


4. 海外最下面的两个区域，中间多出来一行，跟原网站不太一样，不知道为什么会多出来

	```
	答：首先你将.oversea的a标签设置为float，所以它的height属性没效果；先将float去掉，并设置a为block
	```


5. 未完成的部分：（1） 一些图标，不知道怎么使用这些icon,比如定位，向下的小箭头，还有国旗
   
    (2) navbar中点击手机京东，里面的一个白色的三角不知道是怎么做出来
   
   ```
   （1）答，网站中的图标，一般用矢量图，或者用精灵图的方式展现。像作业中的向下的小箭头用的是矢量图；
   而国旗用的是精灵图，然后定位。
   
   这些都是矢量图iconfont；都是公司内部设计的，比如右箭头：
	@font-face {
	  font-family: "iconfont"; /* Project id  */
	  src: url('iconfont.ttf?t=1670287359638') format('truetype');
   }
	
	.iconfont {
	  font-family: "iconfont" !important;
	  font-size: 16px;
	  font-style: normal;
	  -webkit-font-smoothing: antialiased;
	  -moz-osx-font-smoothing: grayscale;
   }
	
	.icon-youjiantou:before {
	  content: "\e686";
   }
	
	
	使用的时候：
	<i class="iconfont icon-youjiantou"></i>
   就会显示右箭头的图标
   ```

	（2）答：很高兴您发现了这个问题，而我们下节课也将具体展开讲解。
	具体用到border元素的设置。
