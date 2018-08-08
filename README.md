/// &lt;reference path="..." /> Demo
=================================

这个Demo很花了我一些时间，主要原因是现在的TypeScript（`1.6`以后）已经基本上不再使用这个指令指定类型文件了，而是使用安装了npm `@types`库就可以直接使用了。
（参看<https://basarat.gitbooks.io/typescript/docs/types/@types.html>）

只是在当年那个时代，一切还在探索之中，规范还没有形成。所以就有了这个奇怪的“三斜线注释指令”用来告诉typescript编译器去哪里找类型声明文件。

在这个Demo中，我们定义了一个简单的JavaScript module `my-module`，名为`a`，并在`package.json`中声明为本地依赖供使用，
同时还手写了`a.d.ts`文件，对`a`进行类型声明。

- `hello1.ts`中通过`<reference>`引用不`a.d.ts`，所以当参数类型不符合声明时，编译会报错
- `hello2.ts`未使用，同样的代码编译不会报错

对于这个指令，理解就好，平时基本不需要用了。

Resources
----------

- 三斜线指令说明：[英文](https://www.typescriptlang.org/docs/handbook/triple-slash-directives.html) [中文](https://zhongsp.gitbooks.io/typescript-handbook/doc/handbook/Triple-Slash%20Directives.html)
  - 文档根本看不懂，所以才需要demo
- 写这个Demo时的提问，开始有很多地方想错了：<https://stackoverflow.com/questions/51746138/how-to-use-typescript-triple-slash-reference-comments-to-import-another-module-a>
- 这篇文章终于让我知道哪儿错了：<http://ivanz.com/2016/06/07/how-does-typescript-discover-type-declarations-definitions-javascript>
- 什么时候用`import`，什么时候用`<reference>`: <https://stackoverflow.com/questions/39121354/in-typescript-when-to-use-reference-when-to-use-import>
