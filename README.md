## 规范

1. 统一使用破折号做间隔；
2. 破折号最好只使用一个，最多不能超过2个；
3. 每个网页都有独立的html，css；components的样式统一放在`app/styles/main/components`里；
4. 每写一个页面，都要在`app/index.html`写好，并备注是否完成（开发完成和检验完成）。

### css规范

1. 统一使用 `[pageName]-[classname]`命名，其中pageName为页面名，classname为该dom的命名，例如`logon-nav`为登陆页导航栏；若pageName本身带有破折号，那么使用其单词首字母作为pageName，如`goods-list`，使用`gl`；
2. classname的命名必须语义化，不能带有展示性描述，如`notice`是可以的，而`mg-10`,`rounded-corners`这种是不好的；
3. 非第三方依赖文件统一放在`app/styles/main`文件夹下，第三方依赖放在`app/styles/lib`内。

### html规范

1. 文件名必须语义化；
2. 页面如果同属于一类，例如商品列表，商品添加，同属于商品类，那么使用`goods-list`,`goods-add`该方法来写；
3. 组件统一放在`app/components`内，页面统一放在`app/pages`内；
4. 所有页面都以`app/components/layout.html`为基础开发。

## javascript规范

1. 每一个文件都以以下格式来写，以隔离作用域；
```
(()=>{
  //body...
})()
```
2. 函数使用箭头函数，变量只使用`let`,`const`。