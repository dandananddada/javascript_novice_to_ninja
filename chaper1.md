#Hello JavaScript

现在是时候开始学习JavaScript了，在本章我们将介绍JavaScript语言并搭建相应的开发环境，我们也会开始写第一个JavaScript程序。

本章将涵盖：

* 编程
* JavaScript历史
* 必要的JavaScript开发工具
* 第一个JavaScript程序——Hello World!
* 控制台下的JavaScript
* 浏览器下的JavaScript
* 其他复杂的JavaScript程序

## 编程

编程是让计算机实现你想要做的，计算机程序由一系列的指令组成，这些指令指明了计算机需要完成哪些任务。然后不幸的是计算机语言与我们不同，计算机只能识别0和1。第一台计算机通过打孔卡来编程，打孔卡用孔表示1，无孔表示0。机器语言和汇编语言是低级编程语言，它们是最接近计算机硬件的。它们代码抽象难于书写，因为严重依赖于计算机架构。

相对的高级编程语言允许使用诸如逻辑声明、函数这样抽象的概念，这使得程序更易于人们阅读和书写。用诸如C、C++、Java这样的程序语言来编写代码，然后编译成机器语言执行。这些程序运行效率高，使用于需要高效运行的游戏及专用的业务软件。

在运行时通过解释器转译为机器码的高级语言称作脚本语言，他们相对的比编译语言运行要慢。随着解释器概念越来模糊，脚本语言与编译语言的界限也越来越模糊。

## JavaScript

JavaScript是这本书将要介绍的语言，通常它被作为一门web语言。因为几乎所有浏览器都能运行JavaScript，导致它成为目前最流行的语言之一。它入手难度低，你只需要一个文本编辑器和一个浏览器就可以编写JavaScript了。虽然JavaScript易于学习，不过因为独有的特点和一些有趣的怪癖导致它难于掌握。一旦你掌握了它，你会发现它是一门灵活高效的语言，可以写出强大的程序。

JavaScript是一门高级语言，它在运行时被编译。这意味着它需要一个引擎来在运行时解释程序并执行它。像Firefox、Chrmoe、Internet Explore这些浏览器都有提供JavaScript引擎，当然JavaScript也可以脱离浏览器运行。许多现代的JavScript引擎都采用及时（JIT）解释过程来加速编译过程，使程序更快运行。

JavaScript也是一门动态语言，这意味着JavScript可以在运行时改变程序代码。


### JavaScript历史

万维网最初是一些列通过超链接链接到一起的页面，不久后人们想要更多的交互，所以网景（一个早期的浏览器提供商）让Brendan Eich 为他们开发一门新的基于Navigator浏览器的语言。因为网景与微软在占有浏览器市场方面存在激烈的竞争，所以这项工作是需要尽快完成的。Eich计划用十天来创建一门原型语言，为了完成这个计划他从其他语言借鉴了很多特性，比如AWK、Java、Perl、Scheme、HyperTalk和Self。这门新的语言最初被叫做LiveScript，因为当时Sun的Java语言很受欢迎，为了推广，很快得LiveScript更名为JavaScript。这个名字经常会招致些不必要的误会，以为JavaScript是一个精简版的Java。尽管JavaScript采用了很多Java的语法，但实际上这两门语言是没有关系的。

1995年网景浏览器第二版正式引入了JavaScript，次年微软在JavaScript的基础上通过逆向工程创建了微软自己的JavaScript版本，为避免Sun公司已经授权Java商标给网景公司而导致的侵权问题，命名这个版本的JavaScript为JScript。JScript搭载于IE3浏览器有着和JavaScript相同的表现，甚至有同样的bug和怪癖，除此之外也兼备了IE浏览器一些独有的特性。同一时期微软还在IE浏览器上搭载了另一门脚本语言——VBScript，但它并没有火起来。

JavaScript（和JScript）马上流行起来。它入手难度低易于学习，这意味着动态页面及更优交互的网页爆发式的增长。不幸的是，它的低门槛也是一把双刃剑，即使人们没有完全理解代码的含义也能写出可以正常运作的代码。代码被简单的拷贝粘贴经常错误的使用，导致很多糟糕的代码出现在世界各地的网站上。JavaScript经常被用来创建恼人的弹窗广告及嗅探器（用来获取浏览器都访问了哪些页面的程序），导致它也开始有了负面的名声。

网景和Sun公司决定在欧洲计算机制造商协会的帮助下开始标准化JavaScript。同样为了避免触犯Sun公司的Java商标，这个标准化语言叫做ECMAScript。这反而更加混乱。最终ECMAScribt用来代指这项规范，而JavaScript则用来代表语言本身。

ECMAScribt标准很难被统一解释，所以依于不同JavaScript引擎JavaScript有着不同的实现。这有是为什么浏览器在执行同一个JavaScript程序会有不同的表现。

### 浏览器之争

在网景4和IE4发布时，JavaScript已经相当流行。微软开始大肆宣传动态HTML，简写作DHTML，通过使用JavaScript可以使HTML更具互动性。出于抓住人气的目的，网景和微软开始试着添加新的特性，因此引入了不同的语法。这场通过追加新特性的“军备竞争”就是广为人知的浏览器之战。不幸的一方是开发人员不得不去写两个版本的代码来在各自的浏览器上实现同样的结果。专业的开发人员经常误解JavaScript为一门不适合严肃哦编程的玩具语言，这是不公正的批判，语言本身是没有问题的，问题在于如何它是如何实现和使用的。

最终微软赢得了这场“战争”，IE成为了主流浏览器，在Web标准项目（WaSP）的努力下，浏览器对于标准的支持也有所改善。开发人员和浏览器提供商开始共同协作向万维网联盟（W3C）和ECMA指定的标准靠拢。

2002年开源浏览器Firefox面世，2003年苹果公司推出Safari浏览器，它们都很好的支持标准规范，这意味着开发人员可以通过JavaScript开发出能在各个浏览器表现一致的，更好的Web应用。

### Web 2.0

2005年像Google Maps、Flickr和Gmail这样的网站开始出现，成功的证明了JavaScript能够创造出同桌面应用一样表现的富互联网应用。几乎同一时期，Jesse James Garrett创造了Ajax——异步JavaScript和XML，这项技术允许从后端获取数据后，只在web页面相关的部分进行更新，不再需要全页面刷新，不会影响用户访问页面其他部分。这项技术为用户创造了一个无缝体验，并广泛应用于Web 2.0 的项目中。导致很多专业的开发人员开始更加关注JavaScript，它开始被看做是一门强大、灵活的编程语言，能够创造出高质量的代码。

### 标注

随着JavaScript被用于更复杂的应用，浏览器开始拥抱标准，JavaScript的境况发生了改变。新一场浏览器战争爆发了，这次关注点在于哪个浏览器是更符合标准的。

“There has also been competition to increase the speed of the JavaScript engine that is built into the different browsers. This started in 2008 when engineers at Google developed the V8 engine to run inside the Chrome browser. It was significantly faster than previous JavaScript engines and signalled another arms race as other browser vendors responded by increasing the speed of their engines. JavaScript now runs significantly faster in modern browsers and the pace of improvement shows no sign of slowing down.”

### HTML5

HTML5是最新的HTML规范，实际上它更是一系列最新的web技术的总称，涵盖了HTML、CSS3模块以及一些JavaScript和Web页面交互的API，这些内容将在第十章详细说明。

HTML5作为一个新兴的主流的Web开发标准，已经被证明非常流行，在它的一些更有趣的特性方面，JavaScript是一个关键性的功能。

### Node.js

2009年Ryan Dahl 开发了Node.js，它允许在服务端使用JavaScript。它依赖于谷歌V8引擎，基于事件驱动环境实现了无阻塞的输入输出。这使得JavaScript可以实现更高效、更强大的实时Web应用。这也导致了许多应用和JavaScript库可以脱离浏览器使用。Node JS如今异常流行，并且仍旧在增长。这增加了JavaScript的兴趣点和使用性，它也开始在更多环境下出现。

Node.js的流行引领了JavaScript同构开发的潮流，同一套JavaScript代码即可以在客户端运行，又可以在服务端运行，如果客户端无法运行这段代码，它可以在服务端运行并下载，如果无法在服务端运行，则可以在客户端运行。

### JavaScript 的未来

对于JavaScript来说这是一个激动人心的时刻，它不仅是制作单纯的web交互，也可以用来实现越来越多的应用。单页面应用是增长最为快速的领域。这些应用在浏览器上运行，并严重依赖JavaScript。HTMl5游戏也变得越来越流行，尤其图像处理方面，浏览器持续在改进。

JavaScript和HTML5技术可以被用来开发浏览器插件、Windows 8桌面部件、Firefox OS和Chrome OS应用。许多web无关的应用也用JavaScript作为它们的脚本语言，它可以用来添加PDF文档的互动性，创建HTML模板（Mustache），与数据库交互（MongoDB）甚至控制机器人（Cylon.js）

目前看来JavaScript似乎有个不错的未来，随着Web平台的发展和成熟，脱离浏览器使用的增长，JavaScript将在未来开发占据一个重要的地位。


## 基础开发环境

起初先接触很少的JavaScript开发，所需的开发工具只有一个编辑器和一个web浏览器，比如FIrefox、Opera、Internet Explore、Safari或者Chrome。

### JavaScript 版本

这本书中我们将使用EMCA5，建议你使用现代的浏览器（无论使用哪个浏览器，请升级到最新版本）。显然你不能依赖用户去升级他们的浏览器到最新，所以我们也会指出那些无法在旧版本工作的代码。

### 文本编辑器

如果你在使用windows，Notepad就足够用了，如果你觉得他有点太基础了，你可以试试Notepad++，E Text Editor或者Sublime Text。

如果你在使用Mac，你可以使用内置的文本编辑器、Text Wrangler、TextMate或者Atom text editor，你也可以使用Sublime Text。

如果你在使用Linux，用内置的文本编辑器就好（比如Gedit、Genie、Kate、Vim或者Emacs），你也可以使用E Text Editor或者Sublime Text。

你也可以考虑用集成开发环境（IDE）比如Eclipse、Coda、NetBeans或者在线的 Cloud9

其他可选的有趣的可供选择的比如Brakets，这是一个免费的跨平台的，甚至可以写JavaScript编辑器

### 浏览器控制台

几乎所有浏览器都可以运行JavaScript，大多数现代浏览器都支持JavaScript控制台，可以用来执行JavaaScript代码片段。接下来介绍如何在一些主流浏览器启动JavaScript控制台：

##### Chrome

View > Developer > JavaScript Console, 或者Mac下用快捷键：Command + Option + J，Windows或Linux下用快捷键 Command + Option + J (Mac)  Control + Shift + J。

##### Safari

快捷键：Command + Option + I。

##### Internet Explorer

F12打开开发者工具，点击Console标签页。

##### FireFox

快捷键打开Web控制台，Mac下按：COMMAND + SHIFT + K ，Windows下按：CTRL + SHIFT + K 

##### 其他方案

你可以安装Firebug插件，按F12打开Firebug然后点击控制台标签页。

其他选项可以访问站点：JS Console，它允许你直接在浏览器输入JavaScript命令并观察运行结果，我用这个控制台来执行这本书中大部分的代码片段。

## 你的第一个JavaScript程序

关于JavaScript已经聊的差不多了，现在是时候来写你的第一个程序了。

通常去学一门编程语言都是从“Hello world！”程序开始。这是一个简单的程序可以输出“Hello world！”说明你已经踏入编程的世界了。我们准备履行这个传统，用JavaScript写一段“Hello world”程序。

在你的浏览器访问JS Console然后输入如下代码：

```
console.log("Hello World!");
```

不出意外你能看到控制台输出“Hello World！”，如下图。


程序只有一行代码，让控制台输出日志“Hello World！”。

恭喜，你现在已经写了第一个JavaScript程序，虽然代码看起来不多，但是请记住每一个忍者的旅途都是从一小步开始的。
