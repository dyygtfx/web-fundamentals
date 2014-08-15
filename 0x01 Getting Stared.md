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
