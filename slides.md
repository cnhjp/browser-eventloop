---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
# support download
download: true
---

# 浏览器中的事件循环机制

<div class="abs-br m-6 text-left">
  <div class="mb-1">
    <ph-user-bold class="mr-2" />
    <span>黄静平</span>
  </div>
  <div>
    <ph-calendar-bold class="mr-2" />
    <span>2022/06/29</span>
  </div>
</div>

---

# 先看一段代码

```javascript
// 下面代码的输出结果是什么？

console.log('script start');

setTimeout(function() {
  console.log('setTimeout');
}, 0);

new Promise(resolve => {
  console.log('Promise')
  resolve('resolve')
}).then(res => {
  console.log(res)
})

console.log('script end');
```

<details class="mt-4">
  <summary>答案</summary>
  <p>script start、Promise、script end、script end、resolve、setTimeout</p>
</details>

---


# 回头看

```javascript {all|3|10-11|16|13|6|all}
// 下面代码的输出结果是什么？

console.log('script start');

setTimeout(function() {
  console.log('setTimeout');
}, 0);

new Promise(resolve => {
  console.log('Promise')
  resolve('resolve')
}).then(res => {
  console.log(res)
})

console.log('script end');
```

---

# 引用

[]()

[How JavaScript works: Event loop and the rise of Async programming](https://blog.sessionstack.com/how-javascript-works-event-loop-and-the-rise-of-async-programming-5-ways-to-better-coding-with-2f077c4438b5)

[菲利普·罗伯茨：到底什么是Event Loop呢？](https://www.youtube.com/watch?v=8aGhZQkoFbQ)

[JS事件循环机制（event loop）之宏任务/微任务](https://juejin.cn/post/6844903638238756878)

[【前端进阶】深入浅出浏览器事件循环](https://juejin.cn/post/6880419772127772679)