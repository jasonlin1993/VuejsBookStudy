- 元件( Component ) 是 Vue 最主要也是最強大的特性，它提供 HTML DOM 元素擴充性，也可將部分模板、程式碼封裝起來以便開發者維護以及重複使用
  ![components](image/2-1-component-01.25dce166.png)

```html
<div id="app">
  <header-component>...</header-component>
  <menu-component>...</menu-component>
  <main-component>...</main-component>
  <footer-component>...</footer-component>
</div>
```

![component2](image/1-1-component-tree.57f28ee7.png)

- 每一個被封裝後的元件單元，都含有自己的模板、樣式，與行為邏輯，並且可以被重複使用。
- 而在元件之中又可以含有元件，這樣由一個個元件單元組合而成的「元件樹」，就是 Vue.js 元件系統的概念。
