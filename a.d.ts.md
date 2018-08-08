之前的定义是由ts文件生成的(`tsc --declaration a.ts`)，内容如下：

```
export declare function hello(name: any): void;
```

可惜这种定义无法跟`/// <reference ...`配合使用，因为没有声明`module`。

最后参考了其它文章，改成了现在的样子，主要就是加了`declare module 'a'`的声明。