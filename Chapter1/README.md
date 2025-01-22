### Chapter 1 Vue.js 基礎入門

- Vue.js 是採用 MVVM 模式
- ![vueAndMvvm](image/vueandmvvm.png)
- ![mvvm](image/MVVM.png)
- 將 Dom 的事件監聽與狀態資料綁定封裝，當使用者透過操作 View 或觸發網頁上的事件，ViewModel 層的 Vue.js 就會將狀態回存至 Model。
- 若 Model 裡的狀態被修改了，Vue.js 也會同步更新網頁 ( View ) 的對應內容
- 事件綁定: v-on

  - v-on:[事件名稱] = '運算式'

  ```js
  <p> Count:{{ count }} </p>
  <button v-on:click="count++">Plus</button>


  const vm = Vue.createApp({
    data() {
        return {
            count:0
        }
    },
  }).mount('#app');
  ```

- 為什麼 key 很重要？

  - 在 Vue 的虛擬 DOM 中，v-for 用於生成列表元素時，key 提供了一個唯一的標識，幫助 Vue 在更新列表時有效追蹤每個元素的狀態。
  - 如果缺少 key，Vue 可能會重用 DOM 節點，導致響應式數據的綁定錯亂，例如多個選項共享相同的 v-model。

- Vue.js 的生命週期
  ![lifecycle](image/lifecycle.png)
