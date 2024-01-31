# 尺寸单位 rpx 转换为 vmin

## 原理
1rpx 是屏宽的 $\frac{1}{750}$，1vmin 是屏宽的 $\frac{1}{100}$。

## rpx 和 vmin 的对应关系  
$$
1rpx=\frac{100}{750}vmin=\frac{10}{75}vmin
$$
$$
1vmin=\frac{750}{100}rpx=7.5rpx
$$
## 例如：10rpx，换算为 vmin
$$
10rpx=10\times\frac{10}{75}=\frac{100}{75}=1.\dot{3}vmin
$$
## 对应 wxss 为
```css
.selector {
  font-size: calc(10vmin * 10 / 75);
}
```
