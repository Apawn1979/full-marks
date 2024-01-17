---
tags:
- 可迭代
- 迭代器
---

# 迭代协议

## 包括
1. 可迭代协议
2. 迭代器协议

## 什么是可迭代？

一个对象，实现了`@@iterator`方法，该方法返回一个【**迭代器**】对象。

```ts
interface Iterable {
  @@iterator: () => Iterator;
}
```

> 注：`@@iterator`方法无法按常规语法访问，可这样访问：
> `obj[Symbol.iterator]`

## 什么是迭代器？

一个对象，实现了 `next()`方法，该方法返回一个【**迭代器结果**】对象。

```ts
interface Iterator {
  next: () => IteratorResult;
}
```

## 迭代器结果长什么样？
```ts
interface IteratorResult {
  value: any;
  done: boolean;
}
```

说明：本文仅提炼最核心的概念，详情请参考：[MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols#%E5%8F%AF%E8%BF%AD%E4%BB%A3%E5%8D%8F%E8%AE%AE)。
