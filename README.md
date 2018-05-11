# 微信小程序 wepyjs 第三方tabs组件

## 说明
菜单栏组件、可滑动、下划线、css动画
此组件依赖于[wepyjs](https://github.com/wepyjs/wepy)

## 使用

### 安装组件
```
npm install wepy-com-tabs --save
```

### 引入组件
```javascript
// index.wpy
<template>
    <tabs @change.user="tabChange" />
</template>
<script>
    import wepy from 'wepy';
    import Tabs from 'wepy-com-tabs';

    export default class Index extends wepy.page {
        components = {
            tabs: Tabs
        };
    }
</script>
```


### 属性值
属性 | 默认值 | 类型 | 必填 | 说明
---|---|---|---|---
height | 35 | String | 否 | 高度px
sliderWidth | 20 | String | 否 | 下划线宽度px
fontSize | 12 | String | 否 | 字体大小px
selectColor | #1AAD19 | String | 否 | 选择时颜色
color | #888888 | String | 否 | 颜色


### 调用方法
```javascript
this.$invoke('tabs','init',[
    {title:'选项1'},
    {title:'选项2'},
    {title:'选项3'}
]);
```
