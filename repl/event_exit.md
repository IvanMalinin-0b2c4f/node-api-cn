<!-- YAML
added: v0.7.7
-->

当接收到 `.exit` 命令、或按下两次 <kbd>Ctrl</kbd>+<kbd>C</kbd> 发出 `SIGINT` 信号、或按下 <kbd>Ctrl</kbd>+<kbd>D</kbd> 发出 `'end'` 信号而使 REPL 被退出时，触发 `'exit'` 事件。
监听器的回调函数被调用时不带任何参数。

```js
replServer.on('exit', () => {
  console.log('从 REPL 接收到 "exit" 事件！');
  process.exit();
});
```

