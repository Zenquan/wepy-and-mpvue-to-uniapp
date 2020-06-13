# wepy-and-mpvue-to-uniapp

## 背景

最近接到一个需求，就是把有用wepy写的小程序合并到由mpvue写的小程序里，本来是打算基于一个框架去重写另一部分，而且其中一个还要迭代到2.0，
但是产品给的最后给的时间实在太短，所以只能是把其中一个转成类似于mpvue，最后定下来uniapp的方案，因为uniapp一部分代码是基于mpvue，所以
从mpvue没什么难度，另一部分wepy的从github看到这个轮子[wepy-to-uniapp](https://github.com/zhangdaren/wepy-to-uniapp)，虽然不完整，
但完善一下还是可以用的。所以以下分别从wepy to uniapp和mpvue to uniapp的迁移展开。

## wepy to uniapp

这个项目的wepy-to-uniapp来自于[wepy-to-uniapp](https://github.com/zhangdaren/wepy-to-uniapp), 并做了完善。

[文档](./wepy-to-uniapp/wepy-to-uniapp.md)

- [ ] 模板标签转换：
  <!-- - [x] 把view转换成div，
  - [ ] 把image标签转换成img， 现在处在`<img></img>`还要改一下
  - [ ] navigator
  - [ ] scroll-view
  - [ ] swiper --> 原生支持
    <!-- - [ ] block -->
  - [ ] repeat
  - [ ] import
  - [ ] 去掉data: {}
  - [ ] :@
  - [ ] fillter引入
  - [ ] mixins改写
- [x] 模板逻辑判断：wx:if="{{info.label}}" 转换成 v-if="info.label"
- [x] 模板循环：wx:for="{{info.label}}" 转换成v-for="(item,key) in info.label"
- [x] 事件绑定：@tap="follow" 转换成 @click="follow"


本地运行

```bash
//windows
node .\bin\etu -i yourProject
```

## mpvue to uniapp


参考资料：

- [微信小程序文档](https://developers.weixin.qq.com/miniprogram/dev/component/navigator.html)
- [vue](https://cn.vuejs.org/v2/guide/forms.html)
- [wepy](https://wepyjs.github.io/wepy-docs/)
- [uni-app](https://uniapp.dcloud.io/)
- [[AST实战]从零开始写一个wepy转VUE的工具](https://juejin.im/post/5c877cd35188257e3b14a1bc#heading-7)
