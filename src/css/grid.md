---
 tags:
   - 网格布局
---

# grid 布局最基本用法示例

html：
```html
<div class="father">
  <div class="child">1</div>
  <div class="child">2</div>
  <div class="child">3</div>
  <div class="child">4</div>
  <div class="child">5</div>
</div>
```

css：
```css
.father {
  display: grid;
  
  /* 3 列，列宽 160px */
  grid-template-columns: repeat(3, 160px);
  /* 不限列数（自动增减），列宽 160px 
  grid-template-columns: repeat(auto-fill, 160px); */
  
  /* 最小网格高度 80px，最大网格高度不限（被内容撑起） */
  grid-auto-flow: minmax(80px, auto);
  
  /* 行间距和列间距都是 10px */
  gap: 10px;
  /* 行间距 10px，列间距 6px
  gap: 10px 6px; */
}
.child {
  /* 可使子元素和网格边界对齐 */
  margin: 0;
}
```
