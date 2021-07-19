# JSHint

## 参考资料

主要内容参考一下 Node.js 应用开发课程的中篇调试话题中的 JSHint 静态代码检查的教案。

其他细节问题：
- js 文件中嵌入模板代码后，jshint 提示警告：Misleading line break before '+'; readers my interpret this as an expression boundary。增加 .jshintrc 配置文件，消除警告：

```json
{
  "laxbreak": true

}
```
详细信息参考：https://github.com/mytcer/jshint-docs-cn/blob/master/relaxing_options.md
