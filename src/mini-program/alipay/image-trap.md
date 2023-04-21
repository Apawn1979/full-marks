---
tags:
- 支付宝
- 小程序
- 踩坑
- 图片
---

# 踩坑记——支付宝小程序图片预览

## tap 事件

原生的 `<image>` 对 tap 事件的支持是理想的，如：

```xml
<image src="xxxx" catchTap="doSth"></image>
```
一旦你有把图片封装为自定义组件的需求时，就要小心了，上述的 `onTap` 或 `catchTap` 
很可能不会按你的预期工作，假设你封装了一个自定义组件 `my-image`：
```xml
<my-image src="xxxx" catchTap="doSth"></my-image>
```
你可能需要在你的组件外层再包装一层父盒子：
```xml
<view catchTap="doSth">
  <my-image src="xxxx"></my-image>
</view>
```

## 预览

图片预览的 API 是这样的，
```javascript
// 支付宝
my.previewImage({
  current: 0, // 当前预览的图片的索引，基于 0
  urls: [], // 预览的图片 url 的集合
});

// 微信、百度等小程序
xx.previewImage({
  current: '', // 当前预览的图片的 url
  urls: [], // 预览的图片 url 的集合
});
```
看出差异了吗？小坑一枚！
