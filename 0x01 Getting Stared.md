###你的首个多屏网站
 
构建多屏体验并没有你听说的那么难。按照本教程中的课程，我们将为《CS256：移动Web开发 》课程做一个示范登录页，它可很好地运行于多种不同设备。


最终产品
![最终产品](https://developers.google.com/web/fundamentals/getting-started/your-first-multi-screen-site/images/finaloutput-2x.jpg)

在你完成上述课程之后，你将做出一个优秀的产品登录页，你可以应用于自己网站。网站将自适应于多种设备，从手机到电视。

**课程**

01.创建网站内容和结构 — 内容是所有网站的最重要部分。在这篇课程中，我们将向你展示如何快速规划并构建你的首个多屏网站。

02.让网站自适应 — 可以访问网站的设备数量非常多，从小屏幕的手机到大屏幕的电视。学习如何构建一个可以很好运行在这些设备的网站。

##创建网站内容和结构 


内容是任何网站最重要的部分。因此，让设计服务于内容，而不是设计决定内容。在这篇指南中，首先确定我们需要的内容，然后根据内容来创建结构，接着以简单的线性布局展示网页。线性布局在宽窄视口（ViewPort）方面具有良好效果。

本教程内容
 
* 创建网页结构 
* 向网页添加内容
* 总结 

###创建网页结构
 
####确定我们的需求
* 01  一块描述我们高级产品 — “CS256：移动Web开发”教程–的区域
* 02  一个表单，用于收集对我们产品感兴趣用户的信息
* 03  一段深入描述，以及视频
* 04  一些实际课程产品中的图片
* 05  一个数据表格，用来支持产品理念的信息

我们还分别从窄视口和宽视口列出了大致的信息架构和布局 

![布局图](https://developers.google.com/web/fundamentals/getting-started/your-first-multi-screen-site/images/wideviewport.png)

然后我们就很容易整出后续网页的基本框架 

```
   <!doctype html>
    <html>
      <head>
         <meta name="viewport" content="width=device-width, initial-scale=1.0">
         <title>CS256: Mobile Web development - structure</title>
      </head>
      <body>
        <div id="headline">
          <header>
            <h1></h1>
            <p></p>
          </header>
          <div id="blurb">
            <p></p>
            <ul>
              <li>
            </ul>
          </div>
          <form method="post" id="register">
          </form>
        </div>
        <div id="section1">
          <h2></h2>
          <p></p>
          <ul>
            <li>
          </ul>
          <video></video>
        </div>
        <div id="section2">
          <h2></h2>
          <p></p>
          <div id="images">
            <img>
          </div>
        </div>
        <div id="section3">
          <h2></h2>
          <p></p>
        </div>
        <footer>
          <p></p>
        </footer>
          </body>
    </html>
```
**给网页添加内容**

这个网站的基本部分已经完成。我们清楚这部分及其要展示的内容，并且知道这部分在整个信息架构中的各自位置。现在，我们开始扩建网站了。

**添加标题个表格**

标题和注册申请表单是该页面的关键部分，必须快速呈现给用户。

添加标题仅需要几行简单的代码。

```
  <div id="headline">
      <div class="container">
        <header>
          <h1>Mobile Web Development</h1>
          <p>Building Mobile Web Experiences</p>
        </header>
        <div id="blurb">
          <p>So you've heard mobile is kind of a big deal, and you're not
          sure how to transform your traditional desktop-focused web apps
          into fast, effective multi-device experiences.</p>
          <p>This course is designed to teach web developers what
          they need to know to create great cross-device web
          experiences.</p>
          <p>This course will focus on building mobile-first web apps,
          which will work across multiple platforms including:</p>
          <ul>
            <li>Android,</li>
            <li>iOS,</li>
            <li>and others.</li>
          </ul>
        </div>
        <form method="post" id="register">
        </form>
      </div>
    </div>
```
我们还需要填充表单。表单简易，用于搜集用户的名字、电话、回他们电话的恰当时间。

所有的表单应该具有标签和placeholders（预期值的提示信息），以便于用户聚焦相应的元素，了解往其中应该填写的内容，还有利于协助工具理解表单结构。名称属性不仅用于把表单值传输到服务器，还用于浏览器针对用户如何自动填写表单问题上给出重要提示。

我们还添加了语义类型，使得用户能够更快、更简单地在移动设备上输入内容。例如，当输入电话号码时，拨号键盘应恰好呈现在用户眼前。

```
<form method="post" id="register">
      <h2>Register for the launch</h2>
      <label for="name">Name</label>
      <input type="text" name="name" id="name"
        placeholder="Thomas A Anderson" required />
      <label for="email">Email address</label>
      <input type="email" name="email" id="email"
        placeholder="neo@example.com" required />
      <label for="tel">Telephone</label>
      <input type="tel" name="tel" id="tel"
        placeholder="(555) 555 5555" required />
      <input type="submit" value="Sign up">
</form>
```
了解更多关于如何创建酷炫的表单：

* 创建漂亮的表单
* 正确地输入标签和名称
* 选择最佳的input类型
* 提供实时验证

####创建视频信息和信息区域

内容的视频、信息区域稍微复杂一些，包括了一个我们产品功能的项目符号列表，还包含一个展示我们产品服务于用户的预留视频。


	<div id="section1">
	<div class="container">
	<h2>What will I learn?</h2>
	<p>After completing this class, you'll have built a 	web application with a first-class mobile experience.</p>
	<p>You'll understand what it takes to:</p>
	<ul>
	<li>build great web experiences on mobile devices</li>
	<li>use the tools you need to test performance</li>
	<li>apply your knowledge to your own projects in the future</li>
	</ul>
	<video controls poster="udacity.png">
	<source src="udacity.mp4" type="video/mp4"></source>
	<source src="udacity.webm" type="video/webm"></source>
	<p>Sorry your browser doesn't support video.
	<a href="udacity.mov">Download the video</a>.
	</p>
	</video>    
	</div>
	</div>
	
视频通常以互动性较强的方式来描述内容，经常用来阐述一个产品或概念。

遵循最佳实践原则，你可以轻松地在你的网站整合视频：

添加controls属性，方便人们播放视频
添加poster图片，提供内容预览
添加多个<source>元素，以支持多种视频格式
当窗口无法播放视频时，添加带视频链接的文本，供人们下载视频

```
<video controls poster="udacity.png">
  <source src="udacity.webm" type="video/webm"></source>
  <source src="udacity.mov" type="video/mov"></source>
  <p>Sorry your browser doesn't support video.
     <a href="udacity.mov">Download the video</a>.
  </p>
</video>
```
 了解更多关于网站使用视频的最佳方式

* 有效使用视频
* 改变开始播放位置
* 包含一张视频的海报

###创建图片区域

没有图片的网站会略显枯燥。有两种类型的图片：

* 内容图片—嵌入文档的图片，用于传达其他内容信息
* 样式图片—让网站看起来更漂亮的图片，包括背景图片、图案、渐变。我们将在下篇文章中讲述。
图片区域是内容图片的集合。这些图片出现在我们的产品中。

```
	<div id="section2">
      <div class="container">
        <h2>Who will teach me?</h2>
        <p>The worlds leading mobile web developers.</p>
        <div id="images">
          <img src="chriswilson.png" alt="Chris Wilson 			Course Instructor">
          <img src="peterlubbers.png" alt="Peter Lubbers 				Course Instructor">
          <img src="seanbennett.png" alt="Sean Bennet 			Course Developer">
        </div>
         
   </div>
	</div>
```

内容图片对于传达网页的涵义有着至关重要的作用。想想报纸文章中使用的图片吧。

```
	<div id="images">
      <img src="chriswilson.png" alt="Chris Wilson Course 		Instructor">
      <img src="peterlubbers.png" alt="Peter Lubbers 	Course Instructor">
      <img src="seanbennett.png" alt="Sean Bennet Course 		Developer">
    </div>
```
图片设置成与屏幕宽度一样宽。这个设置在移动设备上行之有效，但在桌面程序中表现平平。我们将在响应式设计部分讲述这个问题。

发现在内容中使用图片的最佳实践

* 有效使用图片
* 在标记中正确使用图片
* 优化图片压缩

####添加数据列表部分
最后一部分是简单的表格，用于列出产品的详细统计数据。

表格仅限用于列表式资料，如信息矩阵。

```
    <div id="section3">
      <h2>Mobile. Why should I care?</h2>
      <p>It is huge.  Everywhere.</p>
      <table>
        <caption>
          <p>Data from <a href="http://gs.statcounter.com/#desktop+mobile+tablet-comparison-ww-monthly-201303-201403">StatsCounter</a></p>
        </caption>
        <thead>
           <tr>
             <th>Country</th>
             <th>Desktop share</th>
             <th>Tablet share</th>
             <th>Mobile share</th>
           </tr>
        </thead>
        <colgroup>
           <col span="1">
           <col span="1">
           <col span="1">
           <col span="1">
        </colgroup>
        <tbody>
         <tr>
            <td data-th="Country"><a href="http://gs.statcounter.com/#desktop+mobile+tablet-comparison-IN-monthly-201303-201403">India</a></td>
            <td data-th="Desktop share">32%</td>
            <td data-th="Tablet share">1%</td>
            <td data-th="Mobile share">67%</td>
          </tr>
          <tr>
            <td data-th="Country"><a href="http://gs.statcounter.com/#desktop+mobile+tablet-comparison-GB-monthly-201303-201403">GB</a></td>
            <td data-th="Desktop share">69%</td>
            <td data-th="Tablet share">13%</td>
            <td data-th="Mobile share">18%</td>
          </tr>
          <tr>
            <td data-th="Country"><a href="http://gs.statcounter.com/#desktop+mobile+tablet-comparison-US-monthly-201303-201403">US</a></td>
            <td data-th="Desktop share">69%</td>
            <td data-th="Tablet share">9%</td>
            <td data-th="Mobile share">22%</td>
          </tr>
          <tr>
            <td data-th="Country"><a href="http://gs.statcounter.com/#desktop+mobile+tablet-comparison-CN-monthly-201303-201403">China</a></td>
            <td data-th="Desktop share">86%</td>
            <td data-th="Tablet share">4%</td>
            <td data-th="Mobile share">10%</td>
          </tr>
        </tbody>
      </table>
    </div>
 ```
 
#### 添加页脚

大部分网站需要一个页脚，用来展示诸如条款和条件、免责声明等内容，以及无须出现在页面的主导航或主内容区域的其他内容。

在我们的网站中，我们将链接到使用条款和条件、联系页面、以及我们的社交帐号。

	<div id="footer">
  		<div class="container">
   			 <p>We always need a footer.</p>
  		</div>
	</div>
	
####总结

我们已经创建好了网站的大纲，确定了全部的主要框架元素。我们确信所有相关内容已经准备妥当，以满足我们业务的需求。

![总结](https://developers.google.com/web/fundamentals/getting-started/your-first-multi-screen-site/images/content.png)
![总结](https://developers.google.com/web/fundamentals/getting-started/your-first-multi-screen-site/images/narrowsite.png)

你会发现，网页现在看起来相当完美了，这是已经设计完的效果。内容是任何网站最重要的方面。我们需要确保拥有良好的信息架构和坚实的信息密度。这篇指南提供了优秀的创建网站基础。我们将在下一篇指南中为内容设计样式。
