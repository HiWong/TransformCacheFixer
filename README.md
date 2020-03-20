## 起因
transform的增量编译有较多的bug, 其中一个是由于其对于dir inputs的命名不严谨造成的。
解决方式有很多种，这里选择了直接修改AGP的源码。

## 注意点
TransformTask中的outputConsumedInputs()和outputStream.save()方法建议只在本地测试时开启，切勿提交到团队代码中，以免影响编译速度。