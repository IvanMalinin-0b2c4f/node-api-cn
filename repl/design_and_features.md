
`repl` 模块导出了 [`repl.REPLServer`] 类。
当 [`repl.REPLServer`] 实例运行时，它接收用户输入的每一行，根据用户定义的解释函数解释这些输入，然后输出结果。
输入可以是 `stdin`，输出可以是 `stdout`，或者也可以连接到其他任何 Node.js [流][stream]。

[`repl.REPLServer`] 实例支持输入的自动补全、完成的预览、精简 Emacs 风格的行编辑、多行输入、类似 [ZSH] 的反向i搜索、类似 [ZSH] 的基于子字符串的历史搜索、ANSI 风格的输出、当前 REPL 会话状态的保存与恢复、错误校正、以及可定制的解释函数。
不支持 ANSI 风格和 Emacs 风格的行编辑的终端会自动地回退到有限的特性集。


