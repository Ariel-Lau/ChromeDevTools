# Chrome DevTools（`Cmd+Opt+I`）

## 1 介绍

Chrome DevTools是内嵌在Chrome浏览器里的一组用于网页制作和调试的工具。
工欲善其事必先利其器，熟练的使用DevTools能够大大提高我们的工作效率。

## 2 Elements

### 2.1 HTML面板（元素）

#### 2.1.1 元素选择

* 页面鼠标移动到元素 > 右键 > 检查 > 打开开发者工具后自动将鼠标定位的元素选中，背景高亮成蓝色。
* 点击检查元素icon ![](assets/inspect.png)（快捷键：`command + shift + c`），鼠标在页面中选中元素背景被高亮成蓝色。
* 打开开发者工具，点击dom树的某个元素节点，选中节点的背景被高亮成蓝色。
* 在console面板中执行`document.querySelector()`，如`document.querySelector('p')`
* 选择元素DOM层级的直观方式

![](assets/domlayer.jpg)

#### 2.1.2 编辑/替换内容
（1）`cmd + Enter`
（2）点击编辑部分之外的地方保存编辑内容

#### 2.1.3 交换元素位置
* drag拖拽
场景：当你想要看看页面某部分在 DOM 树的不同位置将如何显示的时候，只需拖动并且放置它(到指定的位置)

![](https://user-gold-cdn.xitu.io/2018/12/9/16793797bde74b62?imageslim)

* 使用control按钮
场景：如果只是想在 DOM 结构中往上一点或者往下一点的移动当前被选中的元素，可以使用`[⌘] + [⬆] / [⌘] + [⬇] `。

#### 2.1.4 删除元素
（1）选中元素，按delete
（2）`cmd + z`

#### 2.1.5 选中元素 > 右键
* cut、copy、paste、hide、force state....
<br>(补图......)

#### 2.1.6 技巧
* 显示和隐藏元素
场景：可以按下'h'来隐藏在元素面板中被你选中的元素，再次按下'h'使它出现。某些时候这是很有用的，例如你想截图，但是又不想里面包含一些敏感信息。

![](https://user-gold-cdn.xitu.io/2018/12/9/1679379780c11ef3?imageslim)

* 基础编辑器
(1) 使用`cmd + z` 撤销我们的任何改动。
(2) 使用`cmd + shift + z` 重新编辑我们的任何修改。

![](https://user-gold-cdn.xitu.io/2018/12/9/1679379788863b4e?imageslim)

* 展开所有子节点：右击节点后选择`expand recursively`

![](https://user-gold-cdn.xitu.io/2018/12/20/167c99eb333a3f6c?imageslim)

* 快速控制节点的展开与折叠
左键（left）：折叠子元素
右键（right）：展开子元素
`[⬆]/[⬇]`：上下选择节点

###  2.2 DOM样式(CSS)、结构

#### 2.2.1 styles

##### 2.2.1.1 修改、添加、搜索class属性、新增style样式
* 选中类 > 点击空白 > 输入样式（提示：Enter）
* color颜色选择器（鼠标点击颜色方块会出现颜色选择器）
改变颜色格式：在颜色预览中用Shift + Click ，可以在rgba,hsl和hexadecimal（十六进制）这三种格式中切换。

![](assets/colorpicker.gif)

![](https://user-gold-cdn.xitu.io/2018/12/12/167a1d2cc62a8d0f?imageslim)

* （1）显示和隐藏css属性;
（2）引用外部文件样式，点击文件打开source，定位到对应样式；
（3）鼠标hover到三个点icon，可以添加`text-shadow`、`box-shadow`、`color`、`background-color`，点击+icon可以添加新的style样式。

![](assets/cssproperty.png)

![](https://user-gold-cdn.xitu.io/2018/12/14/167ac1748b954754?imageslim)

* 搜索类名（点击`.cls`）
* 添加新的style样式，点击`.cls`旁边的`+`图标

![](assets/addcls.jpg)

##### 2.2.1.2 设置标签不同状态的样式
* 点击`:hov`可以选择不同的状态

![](assets/hov.png)

* 在线调伪类样式
选中a标签 > 右键 > `force element state` > 选择想要调试的伪类，在标签前会出现一个黄色的小圆点，就可以直接调伪类样式了。

![](assets/atagfake.jpg)

##### 2.2.1.3 快速同步定位页面视图到选中元素(`Scroll Into View`)
* 场景：页面视图显示靠底部，选中的dom节点元素在靠上位置。
操作：选中元素 > 右键 > `scroll into view`使视图快速回到dom选中元素位置

![](assets/scrollintoview.png)

##### 2.2.1.4 快速查找节点
* `cmd + f`

![](assets/searchnode.png)

##### 2.2.1.5 编辑DOM节点
* 修改内容：双击选中元素的内容即可修改

![](assets/editdomnode.png)

* 添加属性
(1) 双击节点元素名称，右边出现空白即可添加属性
(2)选中元素 > 右键 >  `add attributes`
* 修改元素
(1) 双击节点元素名称，元素名称会被高亮 > 输入新的元素名称

##### 2.2.1.6 技巧
* `Shadow editor`阴影编辑器

![](https://user-gold-cdn.xitu.io/2018/12/14/167ac17a4194c870?imageslim)

* `Timing function editor`定时函数编辑器（`Cubic bezier`贝塞尔 编辑器）：
贝塞尔曲线是一串用来定义CSS的动画速度在整个动画过程中如何变化的魔法数值。
设置为`transition-timing-function`或者 `animation-timing-function`CSS属性。
**注意**：如果`timing`函数的值没有设置在`trasition`, `animation`简写的形式中，这个符号不会显示出来)边上的曲线符号

![](https://user-gold-cdn.xitu.io/2018/12/14/167ac1748b45fe3f?imageslim)

#### 2.2.2 如何在`console`面板快速打出相应节点？
##### 2.2.2.1 $
* `$0~$4`：最近选择过的5个DOM节点。`$0`返回最近一次选择的DOM节点(或当前节点)，以此类推，`$1`返回上上次选的DOM节点。最多可保存5个，如果不满5个，则返回undefined。
* 将元素存储为全局变量
场景：需要多次返回某一个节点

![](assets/storeasgloablvariable.png)

![](assets/consoleglobal.png)

#### 2.2.3 DOM Breakpoints <br>
场景：当js修改了DOM节点（如修改节点的属性）时可以给DOM节点打断点来调试。

![](assets/dombreakpoints.png)

#### 2.2.4 computed窗格

##### 2.2.4.1 查看元素盒模型
* 查看width、height、padding、border、margin...度量单位可以是px、百分比、vm等。

##### 2.2.4.2 关于computed中的样式
* 显示顺序是按字母顺序显示
* 显示的是真正作用在元素上的样式：style中的样式可能是全部的样式，包括一些不起作用的样式。可实时查看更新样式是否生效。
* 查看继承的css属性
* 勾选computed中的`show all`复选框，展示元素所有的属性样式。

![](assets/computedshowall.png)

* 通过filter可以过滤/查找某些属性/值（styles、computed...都有这个选项）

#### 2.2.5 检查动画`Animations`
* 作用：
（1）检查动画
（2）修改动画
* 打开方式：
（1）`command menu`，搜索animations打开；
（2）或者在styles窗格按animations按钮打开。

#### 2.2.6 `EventListeners`
![](https://user-gold-cdn.xitu.io/2018/5/11/1634dfc23d6b8c65?imageslim)

#### 2.2.7 `Properties`
查看元素具有的方法与属性，比查API手册要方便。

![](assets/elementsproperties.gif)

## 3 Console

### 3.1 打开

#### 3.1.1 直接打开Devtools，切换到console面板

#### 3.1.2 在其它面板中打开console抽屉
* `command menu` > 搜索console > 选择`Drawer Show Console`
* 打开console面板时，console抽屉式导航栏将自动折叠。

![](assets/openconsole.jpeg)

### 3.2 日志级别 ([demo](https://devtools.glitch.me/console/log.html))

#### 3.2.1 日志来源
* 代码捕捉的日志
* 浏览器或框架捕捉的日志（如404、500、undefined、null等异常错误）

#### 3.2.2 类型
`console.log()`、`console.info()`、`console.warn()`、`console.error()`、console.debug()

#### 3.2.3 消息输出
* 如果一条消息连续重复，控制台不会再新行上输出每一个消息实例，而是将堆叠消息合并，在左侧外边距显示一个数字，表示该消息已重复的次数。

![](assets/consolelognum.png)

* 如果想为每一个日志使用一个独特的行条目，可以在settings中的console项启用`Show timestamps`。或者在`command menu`中打开`timestamps`。

![](assets/showtimestamps.jpeg)

![](assets/timestampedconsole.png)

#### 3.2.4 console过滤
* filter选择过滤不同类型的console信息。
日志严重级别：Verbose、Info、Warning、Error

![](assets/loglever.jpeg)

* 正则过滤 `live expressions`

![](assets/liveexpress.jpeg)

![](https://user-gold-cdn.xitu.io/2018/12/29/167f82b33009449f?imageslim)

#### 3.2.5 sidebar(侧边栏)
![](assets/siderbar.jpeg)

### 3.3 console API
* `console.table()`格式化输出

![](assets/consoletable.png)

* `console.group()`; `console.groupEnd()`：将信息进行分组管理，在信息量较大时使用比较有优势。

![](assets/consolegroup.jpeg)

* `console.dir()`：将一个对象以JSON表达式的格式打印。

![](assets/consoledir.jpeg)

场景：`console.log()`会将这个交互式的元素渲染成像是从Elements中剪切出来的一样。
如果想要查看这个节点所关联到的真实的JavaScript对象，查看节点的属性等等，这样的情况下，如果需要更加直接表现形式来展示数据，就可以使用`console.dir`。

![](https://user-gold-cdn.xitu.io/2018/12/7/1678936410bb79fa?imageslim)

* `console.dirxml()`：将节点的后代节点以xml格式打印出

![](assets/consoledirxml.png)

* `console.trace()`： 可以打出js的函数调用栈
* `console.time()`、`console.timeEnd()` ：计算一段代码间消耗的时间（监测代码执行时间）
`console.time()`开启一个计时器；
`console.timeEnd()`结束计时并将结果在console中打印出来。

如果想一次记录多件事，可以往这些函数中传入不同的标签值。(例如：`console.time('loading')`, `console.timeEnd('loading')`)

![](https://user-gold-cdn.xitu.io/2018/12/13/167a484d3824545d?imageslim)

* `console.profile()` 、`console.profileEnd()` ：查看CPU的消耗
* `console.count()` ：相同的日志当前被打印的次数，比如一个函数被执行的次数。
`console.countRest()`：重置count
* `console.assert(expression, object)` ：
assert（断言）：用于保证程序的正确性，只有当express的值为false，则在控制台上打印错误信息。
* `console.debug()`、`console.info()`、`console.warn()`、`console.error()`......
* `debug()`、`keys()`、`dir()`......

### 3.4 console历史记录

#### 3.4.1 清空console历史记录
* 清空按钮
* 控制台输入`clear()`
* `ctrl + l`
* 在控制台中点击右键，然后按`Clear console`
* JavaScript代码内调用`console.clear()`
**注意**：如果勾选了`preserve log`，则`console.clear()`会被禁用，使用无效。

#### 3.4.2 保留历史记录
* 启用`preserve log`可以在页面刷新或更改之间保留控制台历史记录。
消息将一直存储，直到清空控制台或关闭标签。

![](assets/preservelog.jpeg)

#### 3.4.3保存console历史记录
* 控制台中点击右键，然后选择`Save as`，将控制台的输出保存到日志文件中。

![](assets/consolesaveas.png)

### 3.5 $
* `$0~$4`：打出选中的元素，上一次选中的元素，上上次选中的元素...以此类推
* `$_`：返回最近使用的表达式的结果（对上次执行结果的引用）；如果`$_`表达式是一个数组，则可以用`$_.length`获取数组的长度
* `$()`: `document.querySelector()`返回第一个与之匹配的css选择器，如`$('div')`返回本页的第一个div元素。
* `$$()`：`document.querySelectorAll()`返回一个数组，与之匹配的css选择器的元素。如`$$('div')`返回所有的div元素组成的数组
* `$i`：引入一些npm库

![](https://user-gold-cdn.xitu.io/2018/12/7/16785da0dea963fb?imageslim)

### 3.6 console设置
* setting设置console模块
* console面板点击设置icon

![](assets/consoleset.jpeg)

### 3.7 技巧
* console代码换行：Chrome控制台回车默认是执行，要想输入换行，应按`Shift + Enter`
* copy()：复制一个具体对象的字符串表达式到剪切板，如`copy($0)`
* `getEventListeners(domElement)`返回在DOM元素上注册的所有的事件

![](https://img.mukewang.com/5b7cd1040001a01305740369.gif)

![](assets/geteventlistener.jpeg)

* `Store as global`：如果你在console中打印了一堆数据(例如App中计算出来的一个数组)，然后你想对这些数据进行额外操作，例如，使用我们刚刚说的copy ，那就可以轻松将它转换成一个全局变量：只需右击，并且选择`Store as global variable`(保存为全局变量) 这个选项。第一次使用的话，它会创建一个名为`temp1`的变量，然后是`temp2`等等。这样你就可以操作各样的数据，而不用担心他们会被复写。

![](https://user-gold-cdn.xitu.io/2018/12/7/167874429e8b8f73?imageslim)

* 保存堆栈

![](https://user-gold-cdn.xitu.io/2018/12/7/16787442c1b6d1f7?imageslim)

* `console.log()`基于调用堆栈自动缩进

![](assets/consolelogstack.jpeg)

## 4 sources

### 4.1 调试

#### 4.1.1 sources面板
（1）文件导航窗格：列出了页面请求的每个文件；
（2）代码编辑窗格：在文件导航窗格选择文件后，代码编辑窗格会显示选中文件的内容；
（3）js调试窗格：检查页面js的各种工具。

![](assets/sourcespanel.png)

#### 4.1.2 js调试窗格
* 调试按钮从左到右：
1.暂停/继续脚本执行：如果一个函数里有大量代码，但是大部分代码与定位的问题无关，点击该按钮（或者光标放到下一个要执行的断点行然后右键选择`continue to here`可以直接到该行的`debugger`）可用于跳过冗长的代码片段，执行到下一个断点处（与你定位问题相关的代码处）。
2.单步调试（不遇到函数，执行下一步；遇到函数，不进入函数，直接执行下一步），快捷键f10；
3.进入函数调试，快捷键f11（不遇到函数，执行下一步；遇到函数，进入函数执行上下文）；
4.跳出当前函数；
5.禁止所有的断点，停止任何调试；
6.程序运行遇到异常时是否中断调试

![](assets/debugger.png)

![](assets/sourcespannel2.png)

* `watch`: 调试过程中监听某些变量值的变化
* `call stack`: 函数调用栈；
拷贝调用栈：右键 —> `copy stack trace`
**技巧**：`Blackbox a script`屏蔽无关代码
（1）场景：假如使用了第三方库、文件，如果你确定你所调试的问题与第三方文件无关，可以开启脚本黑盒的调试方式，开启黑盒调试后调用栈不会出现第三方文件的方法，调试也不会进入到第三方文件的函数中，可以绕过冗长的第三方或更深层次的嵌套，提高调试效率。
（2）操作：
a. 在已打开的文件中右键 —> `Blackbox a script`
b. 在`Call Stack`中，右键 -> `Blackbox Script`
c. `Settings` -> `Blockboxing` -> `add pattern`，下拉菜单中，选择Blackbox黑箱，Disabled阻止执行
**`Blackbox a script`&&`call stack`**：调用栈在排查问题是很有用的，函数的执行是有执行上下文的，函数由最外层到最内层依次压入栈中，在执行的时候，依次从栈中弹出，这样我们就可以从最内层沿着链找到最外层，排查错误时也是这个道理。
有时遇到不知名的错误，可能是调用第三方的，也可能是底层的，总之不是我们写的代码。遇到这种情况就可以尝试用调用栈的方法，沿着链去找源头，不过调用栈中可能混杂了不是我们自己写的函数，这时候`Blackbox script`就派上用场了。
ps: Network表格中的类似调用栈的Initiator也可以结合`Blackbox a script`帮助我们更快速的定位问题。
![](https://user-gold-cdn.xitu.io/2019/3/9/1696299b43d863b3?imageslim)
* `scope`: 作用域链（代码中有闭包时scope窗格关注会多些，比如调试闭包中的this指向）。
* `breakpoints`: 设置的断点全部显示在这里，可以快速定位到文件中断点的位置。
* `XHR/fetch breakpoints`: 发请求的断点，比如可以在发ajax请求中打的断点。
* `DOM Breakpoints`: js改变dom节点属性、dom节点子节点树、移除dom节点操作时打的断点全部显示在这个窗格。
* `global listeners`: 全局监听器
  在浏览器中window是全局对象，所以在`Global Listeners`面板中显示绑定在window对象上的事件监听。
* `event listener breakpoints`： 事件监听断点，比如鼠标的click事件，键盘keydown事件等。勾选事件前面的单选框即可监听该事件。
### 4.2 断点（`break points`）
在代码执行过程中暂停代码，同时检查所有相关的变量的值。

#### 4.2.1 添加断点的方式
* 可以在代码里加`debugger`调试；
* 在代码编辑窗格直接打断点

#### 4.2.2 DOM相关的断点(`DOM Breakpoints`)
* 子节点树改变、节点属性改变、节点移除

![](assets/domchangebreakpoint.png)

#### 4.2.3 条件断点(`Conditional breakpoints`)
* 场景：有时设置的断点被执行太多次了：想想看，有一个对200个元素的循环，但你只对第110次循环的结果感兴趣，或者只对一些满足其他的特殊条件的结果感兴趣。这样的情况下，就可以设置一个条件断点。
* 操作：
（1）右击行号并且选择`Add conditional breakpoint`(添加条件断点)的选项
（2）或者右击一个已经设置的断点并且选择`Edit breakpoint`(编辑断点)
（3）然后输入一个执行结果为true或者false的表达式（它的值并不需要明确的为true或者false尽管那个弹出框的描述是这样说的）。
在这个表达式中，你可以获取到任何这段代码可以获取到的东西，即这一行的作用域。
现在条件满足的话，断点就会暂停代码的执行。

![](https://user-gold-cdn.xitu.io/2018/12/17/167b94b8f36112b7?imageslim)

参考链接：<https://juejin.im/post/5c16d943518825566d2365f3>

### 4.3 代码格式化
* `pretty print` {} 

![](assets/prettypoint.svg)

### 4.4 快速打开文件
将项目文件直接拖到Source面板，DevTools会将对文件的修改同步到系统文件中。

![](https://user-gold-cdn.xitu.io/2018/12/29/167f5b37db4e23ac?imageslim)

### 4.5 `workspaces`
工作区支持即时同步样式

![](https://user-gold-cdn.xitu.io/2018/12/29/167f5b37d2312b72?imageslim)

### 4.6 技巧
1. `command+p`: 直接定位到某一行。如图，直接定位到第33行第14列。

![](assets/positionline.gif)

2. 快速查找文件&搜索特定字符串

![](assets/quicksearch.jpeg)

3. 多行插入编辑内容：在Sources编辑框中，按住Cmd，在要编辑的地方点击鼠标，可以设置多个插入符。按下Ctrl + U撤销编辑，快速输入，快速删除。

![](assets/quickdelete.gif)

4. 多列内容选择 & 匹配相同选项：<br>（1）多列内容选择：按住Alt键，当鼠标箭头变为“+”号后，点击鼠标；<br>（2）匹配相同选项：选中需要匹配的元素，快捷键`Cmd + D`

![](assets/mutilinematch.gif)

5. `snippets`: 在任何页面创建、运行、保存代码段、小脚本。

![](assets/snippets.jpeg)

snippets执行脚本

![](assets/snippetjs.jpeg)

6. `Overrides`重写
   场景：在开发工具上调试css/js时，修改的属性值或代码在重新刷新页面时，所有的修改会被重置。如果想把修改的值保存下来，在页面刷新的时候不会被重置，可以使用overrides特性。
   Overrides默认是关闭的，需手动开启：
   （1）打开Sources面板
   （2）选择Overrides字标签
   （3）选择 `+Select folder for overrides`为Overrides设置一个保存重写属性的目录。

![](assets/sourcesoverrides.gif)

7. `Content scripts` 
   Chrome拓展注入在网页中的脚本。

   ![](assets/sourcecontentscripts.jpg)

8. `corverage`：获取关于冗余代码的摘要-细节信息
步骤1: 打开`command menu (command + shift + p)`

![](assets/corveragestep1.png)

步骤2：搜索`corverage`命令

![](assets/corveragestep2.png)

步骤3：打开coverage窗格，依次点击start和reload按钮

![](assets/corveragestep3.png)

步骤4：coverage窗格展示了在浏览器加载时每个加载的css和js文件中有多少使用和未使用的部分。（绿色是已使用的，红色是未使用的）

![](assets/corveragestep4.png)

步骤5：点击文件可以一行一行查看哪些部分被使用了哪些未被使用。

![](assets/corveragestep5.png)

![](https://user-gold-cdn.xitu.io/2018/12/29/167f829dae8fa7fb?imageslim)

8. `Drawer change`：检查修改的内容（将更改的内容与最初加载的样式进行比较，类似于Git），也可以撤销改动。

![](assets/drawerchange.jpg)

![](https://user-gold-cdn.xitu.io/2018/12/29/167f829dadf27e11?imageslim)

## 5 Network

### 5.1 工具栏

#### 5.1.1 `Preserve log`（跨页面加载保存请求）
如页面跳转，勾选`Preserve log`复选框后DevTool会保存所有请求。

![](assets/netPreserveLog.jpeg)

#### 5.1.2 `Disable cache`（更改加载行为）
勾选`Disable cache`复选框可以停用浏览器缓存来模拟首次访问者，即可模拟新用户访问。
在其它面板中停用浏览器缓存：`command menu`打开`Network conditions`抽屉，勾选/取消`Disable cache`复选框。

![](assets/netdisablecache.jpeg)

#### 5.1.2 搜索/过滤网络日志：字符串搜索、正在匹配、doamin:*.com域名搜索

![](assets/netfilter.jpeg)

* 按类型过滤请求：XHR、JS、CSS、Img、Media、Font、Doc、WS (WebSocket)、Manifest......
* 按属性过滤请求：如domain、method、set-cookie-value、size
* 按时间过滤请求：在Overview窗格中点击并向左或向右拖动，可以仅显示在指定时间范围内处于活动状态的请求。

![](assets/netfiltertime.jpeg)

* **技巧**：同时启用多个类型的过滤器：按住Command，然后点击相应的过滤器

![](assets/netmanytypefilter.jpeg)

#### 5.1.3 隐藏数据网址
数据网址是嵌入到其它文档中的小文件，在Request表格中看到的以`data:`开头的所有请求都是数据网址，如图片的base64格式。

![](assets/nethidedataurl.jpeg)

#### 5.1.4 查看未压缩资源的大小(`Use Large Request Rows`)
点击这个icon还可以启动使用大行请求，就是在请求表格展示的每一行高度增加了。

![](assets/netuselargerrow.jpeg)

#### 5.1.5 Overview时间概览

![](assets/netoverview1.jpeg)

![](assets/netoverview2.jpeg)

### 5.2 网络请求表格

![](assets/networktable.png)

* Name：资源的文件名或标识符
* Status：http请求响应状态码
* Type：资源类型
* Initiator：启动源，发起请求的对象、进程 。Parser、Redirect、Script、Other
* Size：响应头和响应内容组合的大小
* Time：请求开始到从响应中接收到最终字节的总时间。
* Waterfall：瀑布流：各请求相关活动的直观分析图。
  waitting(TTFB)：请求在接收到服务器返回的第一个字节的等待时间
  content download：请求下载花费的时间
  stalled: 请求会因为高优先级请求到达、和目标服务器已经建立了6个TCP连接等原因而阻塞

![](assets/netwaterfall.jpeg)

时间细分阶段各字段表示的意义参考链接：<https://developers.google.com/web/tools/chrome-devtools/network-performance/reference#query-string>

* 对请求进行排序：点击Requests表格中任何列的标题，可以按该列对请求排序。
* 添加或移除列：右键点击Requests表格的表头，然后选择一个选项以便隐藏或显示此选项。 当前显示的选项旁有复选标记。

![](https://user-gold-cdn.xitu.io/2018/12/29/167f828279b0b397?imageslim)

* 添加自定义列：右键点击Requests表格的表头，选择`Response Headers` —> `Manage Header Columns`

### 5.3 查看请求的详情
在Request表格的Name列下，点击请求的地址

![](assets/netheaders.svg)

### 5.4 查看请求的发起者和依赖项
Shift + 鼠标指针悬停在Requests表格中的请求上。绿色请求表示发起者，红色表示依赖项。

### 5.5 Requests的其它操作
导出请求数据、复制到剪切板...

![](assets/netotherop.jpeg)

### 5.6 查看请求的堆栈轨迹
鼠标指针悬停在`Initiator`列上，显示调用堆栈信息。

![](assets/netinitiatorstack.png)

### 5.7 阻塞请求
（1）`command menu` —> `request blocking` —> +add需要阻塞的请求
（2）选中一个请求，右击，选中`Blockrequest domain`或`Blockrequest URL`，可分别阻塞该请求所在domain下的所有请求和该请求。
**红色文字的请求表示已经被阻塞**

![](assets/netblockedstyles.png)

## 6 Performance(Timeline) (待补充......)

## 7 Memory (待补充......)

## 8 Application (待补充......)

### 8.1 Storage (待补充......)
* Cookie
* Local Storage
* IndexDB
* Session Storage
  
## 9 Security
查看页面整体的安全性，Security面板可以调试安全隐患，并确保已在网站上正确实施HTTPS。

### 9.1 `Security Overview` (安全概述)
从`Security Overview`可以知道页面是否安全。
安全的页面会显示信息：This page is secure (valid HTTPS)

![](assets/securityoverview.jpg)

不安全的网页会显示信息： This page is not secure
如果请求的页面通过HTTP提供，那么main origin被标记为不安全

![](https://img.php.cn/upload/article/000/000/028/5c3953e0f18e4198.png)

点击`View certificate`按钮可以查看`main origin`的服务器证书

![](assets/securityviewcertificate.jpg)

使用左侧面板可以检查单个安全或不安全的源，单击安全源以查看该源的连接和证书详细信息。

![](assets/securityorigin.gif)

## 10 Audits (待补充......)

## 11 `Device Mode`模拟移动设备
截屏

![](assets/devicemodescreencut.jpeg)

添加ua，可模拟手机ua

![](assets/devicemodeua.jpeg)

**[获取手百、浏览器等的UA](http://service.spiritsoft.cn/ua.html)**：http://service.spiritsoft.cn/ua.html

## 12 开发者工具的全局配置

### 12.1 更多More
![](assets/setdevtools.jpeg)

#### 12.1.1 `Hide console drawer(或按esc)`
* 打开或关闭console抽屉，在各个面板中都可以打开或关闭console抽屉；
* 点击左侧三个点的icon可以打开其他的抽屉，如网络状况、性能监控等；
* 拖拽面板可以改变各面板的显示顺序

![](assets/sethhideconsoledraw.jpeg)

#### 12.1.2 setting —> workspace
可将DevTools中作出的更改保存到文件系统里，`Add folder`按钮点击可以选择保存文档的目录，所以DevTools也可以作为代码编辑器。

![](assets/setworkspace.jpeg)

#### 12.1.3 快捷键Shortcuts

![](assets/setshortcuts.jpeg)

* 按h键隐藏/显示
* `cmd + shift + d`切换devtool的位置（横、竖）

![](https://user-gold-cdn.xitu.io/2018/12/18/167c07cf50125757?imageslim)

#### 12.1.4 定位sensors

![](assets/setsensors.jpeg)

### 12.2 `Command Menu（cmd + shift + p）`

* Network conditions: User agent可配置各浏览器各版本的代理，也可以新增代理

![](assets/cmdmenunetconditionua.jpeg)

模拟网络状态、模拟特定的用户代理

![](https://user-gold-cdn.xitu.io/2018/12/20/167caa8723019208?imageslim)

* `> —> ?`查看其它有效键入符的执行命令

![](assets/cmdmenuothertype.jpeg)

如果输入 ! 在它的输入框中，就可以根据名字来选择你的代码块。

![](https://user-gold-cdn.xitu.io/2018/12/29/167f5b6999c09e59?imageslim)

* 截屏
(1) 截取页面部分元素：`Capture node screenshot`（截取的是在Elements中选中的元素）
(2) 截取完整页面：`Capture full size screenshot`（截取的是整个屏幕的元素，无需在Elements中选中元素）
(3) 截取当前视图内的页面：`Capture screenshot`（截取的是浏览器当前视图中展示的元素，无需在Elements中选中元素）

* theme切换devtools的主题

* snippets
* sensors
* search
* 3g

## 13 一些技巧
* DevTools已经支持直接使用await

场景：async/await 使得异步操作变得更加容易和可读，唯一的问题在于await需要在async函数中使用。如果我们要在DevTools的控制台使用，需要一些特殊的处理，使用`Immediately Invoked Async Function Expression (IIAFE)`一点都不方便。

![](assets/asyncawait.jpeg)

参考链接：<https://juejin.im/post/5c0fdfc46fb9a049b13e0d82>

## 13 插件推荐
* FeHelper（WEB前端助手）

![](assets/pluginFeHelper.jpg)

* 全能二维码
* Dark Reader：护眼神器
* Nimbus 截幕 & 屏幕录像机

![](assets/pluginNimbus.jpg)

* 掘金
* Performance-Analyser(网页性能分析)：分析网页加载性能，包括http请求、执行期的时间、http请求文件的大小、占比

![](assets/pluginperformance.png)

## 14 博客、文章推荐
* [你不知道的Chrome调试工具技巧系列](https://juejin.im/post/5c09a80151882521c81168a2)