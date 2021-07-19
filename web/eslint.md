# ESLint

## 简介

略

## 安装 

```bash
npm i -g eslint eslint-config-airbnb eslint-plugin-import
```

## 使用

命令行静态代码检查

```bash
eslint *.js
cd nodejs-demo
find . | grep "^\.\/[0-9]\{2\}.*js$" | xargs eslint
```

vim 集成，编辑 .vimrc 文件

```
let g:syntastic_javascript_checkers=['eslint']
```

## ESLint 输出格式

```bash
/home/wangding/wd/demo-code/node/01-introduction/01-hello-world.js（下划线）
  4:1  warning  Unexpected console statement  no-console
```

下划线上是被测代码文件路径和名称，下划线下是该代码文件中的警告和错误，错误信息格式如下：
行号:列号  错误类型 [warning、error]  错误信息  规则名称

所有规则可以在 ESLint 官网的[规则文档](http://eslint.cn/docs/rules/)中查看规则的具体说明文档。

## ESLint 配置

ESLint 配置有两种主要方法：
- 注释配置，使用 JavaScript 注释将配置信息直接嵌入代码文件中
- 文件配置，使用 JavaScript、JSON 或 YAML 文件指定整个目录及其所有子目录的配置信息
可以是 package.json 文件中的 `.eslintrc.*` 文件或 eslintConfig 字段的形式，这两个 ESLint 都将自动查找和读取，也可以在命令行中指定配置文件。

ESLint 配置有三个层次：
- env 环境配置
- global 全局配置
- rules 规则配置

配置方法有多种，JavaScript、JSON 和 YAML，最简单的是 JSON 配置方法，这一点跟 JSHint 的 .jshintrc 配置类似。

## ESLint 规则

根据 node-demo 中的 Node.js 程序报的错误，查看并了解了如下规则：
- no-console
- no-var
- func-names


【参考资料】
- ESLint 官网：https://eslint.cn/
- ESLint 使用入门：https://csspod.com/getting-started-with-eslint/
- https://segmentfault.com/t/eslint/blogs
- JavaScript 代码检查工具对比：https://segmentfault.com/a/1190000010264410


