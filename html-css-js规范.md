1、驼峰式
> 1) 大驼峰 eg: UserInfo
> 2) 小驼峰 eg: userInfo

2、文件资源（项目、目录）
> 1) 文件名不得有空格
> 2) 文件名建议只使用小写字母，不使用大写字母
> 3) 名称较长时用中划线分隔
```
    c:/front-end/project-app
```

3、JS、CSS、SCSS、HTML、PNG 文件命名，全部采用小写方式， 以中划线分隔。

4、javascript
> 1) 命名
>    * 方法名、参数名、成员变量、局部变量都统一使用小驼峰（lowerCamelCase）风格
>    * 其中方法命名尽量是动词、动词+名词的形式。 eg: getData、updateData
>    * 常量命名全部大写，单词间用下划线（ _ ）隔开，力求语义表达完整清楚， 不要嫌名字长

> 2) 代码格式
>    * 使用 2 个空格进行缩进
>    * 不同逻辑、不同语义、不同业务的代码之间插入一个空行分隔开来以 提升可读性 

> 3) 字符串
>   * 统一使用单引号(' ')，不使用双引号(" ")。（ps: 在创建 HTML 字符串非常有好处）
```javascript
    // 推荐
    let str = 'foo';
    let testDiv = '<div id="test"></div>';

    // 不推荐
    let str = 'foo'; 
    let testDiv = "<div id='test'></div>";
```

> 4) 括号 if、else、for、width、do、switch、try、catch...关键字后必须有大括号

5、html
> 1) 推荐使用 HTML5 的文档类型申明
```html
    <!DOCTYPE html>
    <html>
        <head> 
            <meta http-equiv="X-UA-Compatible" content="IE=Edge" /> 
            <meta charset="UTF-8" /> 
            <title>Page title</title> 
        </head>
        <body> 
            <img src="images/company-logo.png" alt="Company">
        </body> 
    </html>
```

> 2) 缩进 缩进使用 2 个空格（一个 tab），嵌套的节点应该缩进。

> 3) 分块注释 在每一个块状元素，列表元素和表格元素后，加上一对 HTML 注释

> 4) 语义化标签HTML5 中新增很多语义化标签，所以优先使用语义化标签，避免一个页面都是div。

> 5) 引号 使用双引号(" ")，不用单引号(' ')

> 6) HTML 标签名、类名、属性统一用小写
```HTML
    // 推荐
    <div class="demo"></div>

    // 不推荐
    <div CLASS="DEMO"></div>
```
> 7) 元素属性 属性值可以写上的尽量都写上
```HTML
    // 推荐
    <input type="text" />
    <input type="radio" name="name" checked="checked" />

    // 不推荐
    <input type='text' />
    <input type="radio" name="name" checked />
```
> 8) 代码嵌套 每个块状元素独立一行，内联元素可选
```HTML
    // 推荐
    <div>
        <h1></h1>
        <p></p>
        <p><span></span><span></span></p>
    </div>

    // 不推荐
    <div>
        <h1></h1><p></p>
    </div>
```

6、css
> 1) 命名
>    * 样式类名使用小写字母，以中划线分割
>    * id采用驼峰方式
>    * scss、less中的变量、函数、混合、placeholder采用驼峰方式

> 2) 尽量使用缩写属性
```CSS
    // 推荐
    padding: 1rem 2rem 3rem 4rem;

    // 不推荐
    padding-top: 1rem;
    padding-right: 2rem;
    padding-bottom: 3rem;
    padding-left: 4rem;
```

> 3) 每个选择器及属性独占一行

> 4) 避免使用 ID 选择器及全局标签选择器防止污染全局样式

> 5) 公共样式放在统一的文件夹下， eg: style/common/common.css

> 6) 属性书写顺序
>    1. 布局定位属性：display/position/float/clear/visibility/overflow
>    2. 自身属性：width/height/margin/padding/border/background
>    3. 文本属性：color/font/text-decoration/text-align/vertical-align/white-space/break-word
>    4. 其它属性：content/cursor/border-radius/box-shadow/text-shadow
```CSS
.cs {
    display: block;
    position: relative;
    float: left;
    width: 100%;
    height: 100%;
    margin: auto;
    color: #fff;
    border-radius: 100%;
    cursor: pointer;
}
```

> 7) less代码组织
>    * @import
>    * 变量声明
>    * 样式声明
```Less
    @import "mixins/color.less";
    @default-text-size: 14px;
    .page {
        width: 100%;
        height: 100%;
    }
```