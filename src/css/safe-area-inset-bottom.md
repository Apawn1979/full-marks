---
tags:
- safe-area-inset-bottom
---

# 适配底部安全区

以 `padding-bottom` 为例：
```css
/* 一般这样写即可 */
.selector {
  padding-bottom: env(safe-area-inset-bottom);
}

/* 如果你需要考虑不支持 env 而支持 constant 的老环境，注意顺序!!! */
.selector {
  padding-bottom: constant(safe-area-inset-bottom);
  padding-bottom: env(safe-area-inset-bottom);
}

/* 如果你需要在安全区的基础上再多“让”出一点，例如 50px */
.selector {
  padding-bottom: calc(50px(假设值) + constant(safe-area-inset-bottom));
  padding-bottom: calc(50px(假设值) + env(safe-area-inset-bottom));
}
```
