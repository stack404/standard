写在前面：本规范参考 [网友博客](https://www.cnblogs.com/suwanbin/p/13200530.html)
>本规范是根据个人习惯，和大众一些习惯融合而成的。例如下文提到字符串采用单引号、组件name遵守kebab-case`（小写横线）`格式、组件文件名使用CamelCase`（大驼峰）`格式等，其实都可以根据实际的情况进行调整。规范的目的是为了编写高质量的代码，提高团队之间的协同能力，降低维护成本。
>
>小写横线（kebab-case）：todo-item <br/>
>小驼峰（camelCase）： todoItem <br/>
>大驼峰（CamelCase）： TodoItem <br/>

# 前端开发规范
  
- [一、编程规范](#一编程规范)
  - [命名规范](#命名规范)
  - [HTML规范](#html规范)
  - [CSS规范](#css规范)
  - [Less or Sass规范](#less-or-sass规范)
  - [JavaScript规范](#javascript规范)
- [二、Vue项目规范](#二vue项目规范)
  - [Vue编码基础](#vue编码基础)
  - [目录规范](#目录规范)
- [三、其他](#其他)
  - [注释说明](#注释说明)
  
## 一、编程规范
### 命名规范

- __项目命名__

  全部采用kebab-case风格（小写横线）。

  :ok_person:推荐：`mall-management-system`<br/>
  :no_good:不推荐：`mall_management-system / mallManagementSystem`<br/>  

- __目录命名__

  全部采用kebab-case风格（小写横线），有复数结构时，要采用复数命名法， 缩写不用复数

  :ok_person:推荐： `scripts / styles / components / images / utils / layouts / demo-styles / demo-scripts / img / doc`<br/>
  :no_good:不推荐： `script / style / demo_scripts / demoStyles / imgs / docs`

    【__特殊__】VUE 的项目中的 components 中的组件目录，使用 kebab-case 风格（小写横线）

    :ok_person:推荐： `head-search / page-loading / authorized / notice-icon`<br/>
    :no_good:不推荐： `HeadSearch / PageLoading`

    【__特殊__】`VUE 的项目中的除 components 组件目录外的所有目录也使用 kebab-case 风格（小写横线）`

    :ok_person:推荐： `page-one / shopping-car / user-management`<br/>
    :no_good:不推荐： `ShoppingCar / UserManagement`<br/>

- __JS/CSS/SCSS/HTML/PNG 文件命名__

  全部采用 kebab-case 风格（小写横线）

  :ok_person:推荐： `render-dom.js / signup.css / index.html / company-logo.png`<br/>
  :no_good:不推荐： `renderDom.js / UserManagement.html<br/>`

- __命名严谨性__ 

  代码中的命名严禁使用拼音与英文混合的方式，更不允许直接使用中文的方式。 说明：正确的英文拼写和语法可以让阅读者易于理解，避免歧义。<br/>
  注意，即使纯拼音命名方式也要避免采用

  :ok_person:推荐：`henan / luoyang / rmb 等国际通用的名称，可视同英文。`<br>
  :no_good:不推荐：`DaZhePromotion [打折] / getPingfenByName() [评分] / int 某变量 = 3`

      __杜绝完全不规范的缩写，避免望文不知义：__<br/>
      :no_good:不推荐：`AbstractClass`“缩写”命名成 `AbsClass`；`condition`“缩写”命名成 `condi`，此类随意缩写严重降低了代码的可阅读性。
 <br/> 
### HTML规范

- __缩进__ 

  缩进使用 2 个空格（一个 tab）

- __注释格式__ 

  在每一个块状元素，列表元素和表格元素后，加上一对 HTML 注释。<br/>
  注释格式：
      ```html
      <!-- 列表模块 start -->
      <div>
        我是列表模块html内容
      </div>
      <!-- 列表模块 end -->
      ```

- __语义化标签__ 

  HTML5 中新增很多语义化标签，所以优先使用语义化标签，避免一个页面都是 div 或者 p 标签<br/>
  :ok_person:推荐：
      ```html
      <header></header>
      <footer></footer>
      ```
      :no_good:不推荐：
      ```html
      <div>
        <p></p>
      </div>
      ```

- __引号__ 

  尽量使用单引号''
 <br/> 
### CSS规范

- __命名__ 

  - class类名使用 kebab-case 风格（小写横线）
  - id 采用camelCase（小驼峰）式命名
  - scss 中的变量、函数、混合、placeholder 采用camelCase（小驼峰）式命名

  ID 和 class 的名称总是使用可以反应元素目的和用途的名称，或其他通用的名称，代替表象和晦涩难懂的名称

  :ok_person:推荐：
    ```css
    .fw-800 {
      font-weight: 800;
    }

    .red {
      color: red;
    }
    ```

  :no_good:不推荐：
    ```css
    .heavy {
      font-weight: 800;
    }

    .important {
      color: red;
    }
    ```

- __选择器__

  - css 选择器中避免使用标签名
  - 使用直接子选择器

  :ok_person:推荐：
    ```css
    .span-class {
      color: blue;
    }
    .content > .title {
      font-size: 2rem;
    }
    ```
  :no_good:不推荐：
    ```css
    span {
      color: blue;
    }

    .content .title {
      font-size: 2rem;
    }
    ```

- __尽量使用缩写属性__

  :ok_person:推荐：
    ```css
    border-top: 0;
    font: 100%/1.6 palatino, georgia, serif;
    padding: 0 1em 2em;
    ```
  :no_good:不推荐：
    ```css
    border-top-style: none;
    font-family: palatino, georgia, serif;
    font-size: 100%;
    line-height: 1.6;
    padding-bottom: 2em;
    padding-left: 1em;
    padding-right: 1em;
    padding-top: 0;
    ```

- __每个选择器及属性独占一行__ 

  :ok_person:推荐：
    ```css
    button{
      width:100px;
      height:50px;
      color:#fff;
      background:#00a0e9;
    }
    ```
  :no_good:不推荐：
    ```css
    button{
      width:100px;height:50px;color:#fff;background:#00a0e9;
    }
    ```
   
- __省略0后面的单位__

  :ok_person:推荐：
    ```css
   div{
      padding-bottom: 0;
      margin: 0;
    }
    ```
  :no_good:不推荐：
    ```css
    div{
      padding-bottom: 0px;
      margin: 0em;
    }
    ```
   
- __避免使用ID选择器及全局标签选择器防止污染全局样式__

  :ok_person:推荐：
    ```css
   .header{
      padding-bottom: 0px;
      margin: 0em;
    }
    ```
  :no_good:不推荐：
    ```css
    #header{
      padding-bottom: 0px;
      margin: 0em;
    }
    ```
<br/> 
### Less or Sass规范

- __代码组织__

  - 将公共less/sass文件放在`assets/styles/`
  - 按照以下顺序组织<br/>
    1.@import;<br/>
    2.变量声明;<br/>
    3.样式声明;<br/>

    ```scss
    @import "mixins/size.less";
    @default-text-color: #333;

    .page {
      width: 960px;
      marg
    }
    ```


- __避免嵌套层级过多__

  将嵌套深度限制在3级。过多的嵌套规则会影响可读性。

  :ok_person:推荐：
  ```scss
  .main-title{
     .name{
        color:#fff
     }
  }
  ```
  :no_good:不推荐：
  ```scss
  .main{
    .title{
      .name{
         color:#fff
      }
    }
  }
  ```
<br/> 
### JavaScript规范

- __命名__
  - 方法名、参数名、成员变量、局部变量都统一使用camelCase（小驼峰） 风格；变量不能以下划线开头，也不能以下划线或美元符号结束<br/>
    :ok_person:推荐：`localValue / getHttpMessage() / inputUserId`<br/>
    :no_good:不推荐：`_name / name_ / name$`<br/>
  
  - method方法命名必须是 _动词_ 或者 _动词+名词_ 形式<br/>
    :ok_person:推荐：`saveShopCarData / openShopCarInfoDialog`<br/>
    :no_good:不推荐：`save / open / nameUpdate`<br/>

  **_为了统一，增删查改、详情分别使用如下五个单词_** <br/>
  `add / update / delete / detail / get`<br/><br/>
  函数方法常用动词
  
  ``` 
  get 获取/set 设置,
  add 增加/remove 删除
  create 创建/destory 移除
  start 启动/stop 停止
  open 打开/close 关闭,
  read 读取/write 写入  
  load 载入/save 保存,
  create 创建/destroy 销毁
  begin 开始/end 结束,
  backup 备份/restore 恢复
  import 导入/export 导出,
  split 分割/merge 合并
  inject 注入/extract 提取,
  attach 附着/detach 脱离
  bind 绑定/separate 分离,
  view 查看/browse 浏览
  edit 编辑/modify 修改,
  select 选取/mark 标记
  copy 复制/paste 粘贴,
  undo 撤销/redo 重做
  insert 插入/delete 移除,
  add 加入/append 添加
  clean 清理/clear 清除,
  index 索引/sort 排序
  find 查找/search 搜索,
  increase 增加/decrease 减少
  play 播放/pause 暂停,
  launch 启动/run 运行
  compile 编译/execute 执行,
  debug 调试/trace 跟踪
  observe 观察/listen 监听,
  build 构建/publish 发布
  input 输入/output 输出,
  encode 编码/decode 解码
  encrypt 加密/decrypt 解密,
  compress 压缩/decompress 解压缩
  pack 打包/unpack 解包,
  parse 解析/emit 生成
  connect 连接/disconnect 断开,
  send 发送/receive 接收
  download 下载/upload 上传,
  refresh 刷新/synchronize 同步
  update 更新/revert 复原,
  lock 锁定/unlock 解锁
  check out 签出/check in 签入,
  submit 提交/commit 交付
  push 推/pull 拉,
  expand 展开/collapse 折叠
  begin 起始/end 结束,
  start 开始/finish 完成
  enter 进入/exit 退出,
  abort 放弃/quit 离开
  obsolete 废弃/depreciate 废旧,
  collect 收集/aggregate 聚集
  ```
  
- __代码格式__

  - 使用2个空格进行缩进 
  - 不同逻辑、不同语义、不同业务的代码之间插入一个空行分隔开来以提升可读性。

- __字符串__

  统一使用单引号（'），在创建有双引号引用的字符串非常友好：

  :ok_person:推荐：
  ```javascript
  let str = 'foo';
  let testDiv = '<div id="test"></div>';
  ```
  :no_good:不推荐：
  ```javascript
  let str = 'foo';
  let testDiv = "<div id='test'></div>";
  ```

- __对象声明__

  - 使用字面量创建对象<br/>
    :ok_person:推荐：`let user = {};`<br/>
    :no_good:不推荐：`let user = new Object();`<br/>
  - 使用字面量来代替对象构造器<br/>
    :ok_person:推荐：
    ```javascript
    let user = {
      age: 0,
      name: 1,
      city: 3
    };
    ```
    :no_good:不推荐：
    ```javascript
    let user = new Object();
    user.age = 0;
    user.name = 0;
    user.city = 0;
    ```

- __使用ES6__

  使用 ES6, ES7 的新语法，比如箭头函数、await/async ， 解构， let ， for…of 等等<br/>
  
- __括号__

  这些关键词，即使只有一行也要有大括号：if else for while do switch try catch finally with <br/>
  :ok_person:推荐：
  ```javascript
  if (condition) {
    doSomething();
  }
  ```
  :no_good:不推荐：
  ```javascript
  if (condition) doSomething();
  ```
<br/>   
## 二、Vue项目规范

### Vue编码基础

- __Vue编码基础__

  尽可能遵守Vue[官方规范](#https://cn.vuejs.org/v2/style-guide/)中的规范，以下列出的规范为重中之重：

  - __组件名为多个单词__
  
    组件名应始终是多个单词，命名规范遵守kebab-case（小写横线）格式。（这样能避免现在或未来的HTML元素冲突，HTML元素始终是单个单词）。<br/>
    :ok_person:推荐：
    ```javascript
    export default {
      name: 'TodoItem'
      // ...
    };
    ```
    :no_good:不推荐：
    ```javascript
    export default {
      name: 'Todo',
      // ...
    }
    export default {
      name: 'todo-item',
      // ...
    }
    ```

  - __组件文件名为kebab-case（小写横线）格式__
  
    即单词之间采用单横杠隔开。<br/>
    :ok_person:推荐：
    ```
    components/
    |- my-component.vue
    ```
    :no_good:不推荐：
    ```
    components/
    |- myComponent.vue
    |- MyComponent.vue
    ```
    
  - __基础组件文件名以base开头，使用完整单词__
  
    :ok_person:推荐：
    ```
    components/
    |- base-button.vue
    |- base-table.vue
    |- base-icon.vue
    ```
    :no_good:不推荐：
    ```
    components/
    |- MyButton.vue
    |- VueTable.vue
    |- Icon.vue
    ```
    
  - __和父组件紧密耦合的子组件，要以父组件名作为前缀__
  
    :ok_person:推荐：
    ```
    components/
    |- todo-list.vue
    |- todo-list-item.vue
    |- todo-list-item-button.vue
    |- user-profile-options.vue （完整单词）
    ```
    :no_good:不推荐：
    ```
    components/
    |- TodoList.vue
    |- TodoItem.vue
    |- TodoButton.vue
    |- UProfOpts.vue （使用了缩写）
    ```

  - __在template中使用组件，采用CamelCase（大驼峰）模式，仅有自己时使用自闭合__
 
    :ok_person:推荐：
    ```html
    <!-- 在单文件组件、字符串模板和 JSX 中 -->
    <MyComponent />
    <Row><table :column="data"/></Row>
    ```
    :no_good:不推荐：
    ```html
    <my-component /> <row><table :column="data"/></row>
    ```
  
  - __prop定义应尽量详细__
 
    - 必须使用 camelCase （小驼峰）命名
    - 必须指定类型
    - 必须加上注释，表明其含义
    - 必须加上 required 或者 default，两者二选其一
    - 如果有业务需要，必须加上 validator 验证

    :ok_person:推荐：
    ```javascript
    props: {
       // 组件状态，用于控制组件的颜色
       status: {
         type: String,
         required: true,
         validator: function (value) {
           return [
             'succ',
             'info',
             'error'
           ].indexOf(value) !== -1
         }
       },
       // 用户级别，用于显示皇冠个数
       userLevel：{
          type: String,
          required: true
       }
    }
    ```

  - __组件样式设置作用域__
 
    :ok_person:推荐：
    ```html
    <template>
      <button class="btn btn-close">X</button>
    </template>

    <!-- 使用 `scoped` 特性 -->
    <style scoped>
      .btn-close {
        background-color: red;
      }
    </style>
    ```

    :no_good:不推荐：
    ```html
    <template>
      <button class="btn btn-close">X</button>
    </template>
    <!-- 没有使用 `scoped` 特性 -->
    <style>
      .btn-close {
        background-color: red;
      }
    </style>
    ```
  
  - __template模版中仅保留简单的表达式__
  
    组件template中应只包含简单的表达式（如三目运算），复杂的表达式重构为`计算属性computed`或者`方法method`。<br/>
    :ok_person:推荐：
    ```javascript
    <template>
      <p>{{ normalizedFullName }}</p>
    </template>

    // 复杂表达式已经移入一个计算属性
    computed: {
      normalizedFullName: function () {
        return this.fullName.split(' ').map(function (word) {
          return word[0].toUpperCase() + word.slice(1)
        }).join(' ')
      }
    }
    ```

    :no_good:不推荐：
    ```html
    <template>
      <p>
           {{
              fullName.split(' ').map(function (word) {
                 return word[0].toUpperCase() + word.slice(1)
               }).join(' ')
            }}
      </p>
    </template>
    ```

  - __指令采用缩写形式__
  
    用（:）表示v-bind、用@表示v-on、用#表示v-slot <br/>
    :ok_person:推荐：
    ```html
    <input
      @input="onInput"
      @focus="onFocus"
    >
    ```
    :no_good:不推荐：
    ```html
    <input
      v-on:input="onInput"
      @focus="onFocus"
    >
    ```

  - __标签顺序template -> script -> style__

  - __v-for必须设置key值__

  - __v-show和v-if选择__
 
    频繁切换使用v-show，相反则用v-if<br/>
  
  - __script内部结构__
  
    :ok_person:推荐：
    ```javascript
    export default {
      components:{},
      props: {},
      data(){
        return {};
      },
      computed:{},
      watch: {},
      钩子函数（按其执行顺序）,
      methods: {},
    }
    ```
  
- __Vue Router规范__

  - __页面跳转，数据传递使用路由参数__
  
    页面跳转时，需要传递参数，推荐使用vue-router进行传参（采用vuex，页面刷新，传参会丢失，除非做两层处理）
  
    :ok_person:推荐：
    ```javascript
    let id = ' 123';
    this.$router.push({ name: 'userCenter', query: { id: id } });
    ```
  
  
  - __使用懒加载（延迟加载）__
  
    :ok_person:推荐：
    ```javascript
    {
      path: '/upload-attachment',
      name: 'UploadAttachment',
      meta: {
        title: '上传附件'
      },
      component: () => import('@/view/components/upload-attachment/index.vue')
    },
    ```
  
  
  - __router命名规范__
  
    path、childrenPath采用kebab-case（小写横线）风格（和文件目录、文件名保持一致）<br/>
    name采用CamelCase（大驼峰）风格（和组件name保持一致，keep-alive根据组件name进行缓存）<br/>
  
    :ok_person:推荐：
    ```javascript
    // 动态加载
    export const reload = [{
        path: '/reload',
        name: 'Reload',
        component: Main,
        meta: {
          title: '动态加载',
          icon: 'icon iconfont'
        },

        children: [{
            path: '/reload/smart-reload-list',
            name: 'SmartReloadList',
            component: () =>
              import('@/views/reload/smart-reload/smart-reload-list.vue')
          }
        ]
      }
    ];
    ```
  
  
  - __path的命名规范__
  
    采用kebab-case（小写横线）风格，必须以“/”开头，子路由需要把父节点的path也带上。<br/>
    :ok_person:推荐：
    ```javascript
    {
      path: '/file',
      name: 'File',
      component: Main,
      children: [
        {
          path: '/file/file-list',
          name: 'FileList',
          component: () => import('@/views/file/file-list.vue')
        }
      ]
    }
    ```
    :no_good:不推荐：
    ```javascript
    {
      path: '/file',
      name: 'File',
      component: Main,
      children: [
        {
          path: 'file-list',
          name: 'FileList',
          component: () => import('@/views/file/file-list.vue')
        }
      ]
    }
    ```  
<br/> 
### 目录规范

- __基础__

  vue项目中的所有文件、变量命名一定要和后端命名统一（尽可能吧，目前的开发流程似乎不能实现）
  
- __目录说明__ 

  所有文件名都采用kebab-case（小写横线）风格。
  ```
  src                               源码目录
  |-- api                              所有api接口
  |-- assets                           静态资源，images, icons, styles等
  |-- components                       公用组件
  |-- config                           配置信息
  |-- directives                       自定义指令
  |-- filters                          过滤器，全局工具
  |-- mock                             模拟接口，临时存放
  |-- public                           公共文件 
  |   |-- constants                        常量信息，项目所有Enum, 全局常量等
  |   |-- lang                             i18n国际化文本
  |   |-- lib                              外部引用的插件存放及修改文件                         
  |   |-- plugins                          插件，全局使用
  |   |-- utils                            工具方法
  |-- router                           路由，统一管理
  |-- store                            vuex, 统一管理
  |-- themes                           自定义样式主题
  |-- views                            视图目录
  |   |-- role                             role模块名
  |   |-- |-- role-list.vue                    role列表页面
  |   |-- |-- role-add.vue                     role新建页面
  |   |-- |-- role-update.vue                  role更新页面
  |   |-- |-- index.less                      role模块样式
  |   |-- |-- components                      role模块通用组件文件夹
  |   |-- employee                         employee模块
  ```

  - __api目录__ 
    - 文件、变量命名要与后端保持一致。
    - 此目录对应后端 API 接口，按照后端一个 controller 一个 api js 文件。若项目较大时，可以按照业务划分子目录，并与后端保持一致。
    - api 中的方法名字要与后端 api url 尽量保持语义高度一致性。
    - 对于 api 中的每个方法要添加注释，注释与后端 swagger 文档保持一致。
    
      :ok_person:推荐：
      ```javascript
      后端： 
          /user/add

      前端：
          /api/user/index.js
          
          addUser = (data) => {
            操作...
          }
      ```
      
  - __assets目录__

    存放静态资源，资源名使用kebab-case（小写横线）风格。<br/>
    ```
    |assets
    |-- icons
    |-- images
    |   |-- background-color.png
    |   |-- upload-header.png
    |-- styles
    ```

  - __components目录__

    组件目录。
    ```
    |components
    |-- error-log
    |   |-- index.vue
    |   |-- index.less
    |-- markdown-editor
    |   |-- index.vue
    |   |-- index.js
    |-- kebab-case
    ```

  - __public目录__

    存放各种js资源
    ```
    |public
    |-- constants                 存放常量（即可供全局使用，不变更的静态数据）
    |   |-- http-code.js              后端返回的code
    |-- lang                      国际化文本
    |   |-- en-us                     英文
    |   |-- zh-cn                     中文
    |   |-- index.js
    |-- plugins                   外部引用的插件存放及修改文件（自己写的，或者改造过的轮子）
    |   |-- moment.js                 结合项目改造的moment.js
    |-- utils                     存放工具方法
    |   |-- cookie.js                 专门处理cookie的
    |   |-- index.js                  不能区分类别的方法
    |   |-- storage.js                专门处理localStorage
    ```

## 其他

### 注释说明
必须添加注释的地方。<br/>
- 公共组件使用说明
- api 目录的接口 js 文件必须加注释
- store 中的 state, mutation, action 等必须加注释
- vue 文件中的 template 必须加注释，若文件较大添加 start end 注释
- vue 文件的 methods，每个 method 必须添加注释
- vue 文件的 data, 非常见单词要加注释

【其他】删除无用代码、尽量不要手动操作dom
