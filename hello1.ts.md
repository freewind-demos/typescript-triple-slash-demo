当指定了类型声明文件时：

```
/// <reference path="./a.d.ts" />
```

如果参数类型和声明的不一样，编译会报错：

```
npx ts-node hello1.ts
```

```
⨯ Unable to compile TypeScript:
hello1.ts(4,7): error TS2345: Argument of type '1' is not assignable to parameter of type 'string'.
```