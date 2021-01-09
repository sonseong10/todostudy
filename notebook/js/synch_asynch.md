# Synchronous & Asynchronous

- JavaScript is **synchronous.**

- Execute the code block by **order after**

- **hoisting: var, function declaration**

![js synchronous](https://adrianmejia.com/images/async-vs-sync-concurrency-in-javascript-large.png)

## Synchronous & Asynchronous 활용법

[Callback.pdf](https://github.com/sonseong10/todostudy/files/5779209/Callback.pdf)

[Promise.pdf](https://github.com/sonseong10/todostudy/files/5779211/Promise.pdf)

[Async Await.pdf](https://github.com/sonseong10/todostudy/files/5779604/async__await_.pdf)

```jsx
//setTimeout(): browser api
console.log(1)
setTimeout(() => console.log("Hi"), 1000)
console.log(3)

// synchronous
function printAll(print) {
  print()
}
printAll(() => console.log("hello!"))

// asynchronous
function printAllDelay(print, timeout) {
  setTimeout(print, timeout)
}
printAllDelay(() => console.log("hello...Dlay"), 2000)
```
