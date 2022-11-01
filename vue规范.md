1、组件规范
> 1) 组件名为多个单词。（组件名应该始终是多个单词组成（大于等于 2），且命名规范为大驼峰方式。
这样做可以避免跟现有的以及未来的 HTML 元素相冲突，因为所有的 HTML 元素名称都是单个单词的。）
```javascript
    // 推荐
    export default {
      name: 'TodoItem'
      // ...
    };

    // 不推荐
    export default {
      name: 'Todo',
      // ...
    }
    export default {
      name: 'todo-item',
      // ...
    }
```

> 2) 组件文件名小写以中划线（-）连接
```
    // 推荐
    components/
    |- my-component.vue

    // 不推荐
    components/
    |- myComponent.vue
    |- MyComponent.vue
```

> 3) 基础组件文件名为 base 开头，使用完整单词而不是缩写。
```
    // 推荐
    components/
    |- base-button.vue
    |- base-table.vue
    |- base-icon.vue

    // 不推荐
    components/
    |- MyButton.vue
    |- VueTable.vue
    |- Icon.vue
```

> 4) 和父组件紧密耦合的子组件应该以父组件名作为前缀命名
```
    // 推荐
    components/
    |- todo-list.vue
    |- todo-list-item.vue
    |- todo-list-item-button.vue
    |- user-profile-options.vue （完整单词）

    // 不推荐
    components/
    |- TodoList.vue
    |- TodoItem.vue
    |- TodoButton.vue
    |- UProfOpts.vue （使用了缩写）
```

> 5) 在 Template 模版中使用组件，以kebab-case方式。
```javascript
    // 推荐
    <my-component />

    // 不推荐
    <MyComponent />
```

> 6) 组件的 data 必须是一个函数
```javascript
    // 推荐
    export default {
        data () {
            return {
                name: 'jack'
            }
        }
    }

    // 不推荐
    export default {
        data: {
            name: 'jack'
        }
    }
```

> 7) Prop 定义应该尽量详细
>    * 必须使用 camelCase 驼峰命名
>    * 必须指定类型
>    * 必须加上注释，表明其含义
>    * 必须加上 required 或者 default，两者二选其一
>    * 如果有业务需要，必须加上 validator 验证)

> 8) 为组件样式设置作用域 （<style scoped></style>）

> 9) 如果特性元素较多，应该主动换行。
```javascript
    // 示例
    <MyComponent foo="a" bar="b" baz="c"
        foo="a" bar="b" baz="c"
        foo="a" bar="b" baz="c"
    />
```

2、必须为 v-for 设置键值 key

3、v-show 与 v-if 选择
> 如果运行时，需要非常频繁地切换，使用 v-show ；如果在运行时，条件很少改变，使用 v-if。

4、目录规范（目录名按照上面的命名规范，其中 components 组件用大写驼峰，其余除 components 组件目录外的所有目录均使用 kebab-case 命名。）
```
src                                  源码目录
|-- api                              所有api接口
|-- assets                           静态资源，images, icons, styles等
|-- components                       公用组件
|-- config                           配置信息
|-- constants                        常量信息，项目所有Enum, 全局常量等
|-- directives                       自定义指令
|-- filters                          过滤器，全局工具
|-- datas                            模拟数据，临时存放
|-- lib                              外部引用的插件存放及修改文件
|-- mock                             模拟接口，临时存放
|-- plugins                          插件，全局使用
|-- router                           路由，统一管理
|-- store                            vuex, 统一管理
|-- themes                           自定义样式主题
|-- views                            视图目录
|   |-- role                                 role模块名
|   |-- |-- role-list.vue                    role列表页面
|   |-- |-- role-add.vue                     role新建页面
|   |-- |-- role-update.vue                  role更新页面
|   |-- |-- index.less                       role模块样式
|   |-- |-- components                       role模块通用组件文件夹
|   |-- employee                             employee模块
```