# 微信小程序 wepyjs 第三方tabs组件

## 说明
菜单栏组件、可滑动、下划线、css动画

此组件依赖于[wepyjs](https://github.com/wepyjs/wepy)

需要开启 Promise 支持
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
this.$invoke('tabs','init',['选项1','选项2','选项3']);

methods = {
    tabChange(index){
        console.log(index);
    }
};
```

## 展示
![image](https://github.com/weimingxuan/wepy-com-tabs/blob/master/example/demo.gif?raw=true)
