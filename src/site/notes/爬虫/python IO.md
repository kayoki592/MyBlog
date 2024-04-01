---
{"dg-publish":true,"permalink":"/爬虫/python IO/"}
---


```javascript
<%* fileName = await tp.system.prompt("请输入笔记名", "新建笔记") await tp.file.rename(fileName) tp.file.cursor() -%> --- dg-publish: true title: <% fileName %> dg-created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss.SSS+08:00") %> tags: [""]
```



```python
f = open(name[.mode[.buffering]])
f = open(r'c:\text\qiye.txt')
```

| 值 | 功能 |  |
| ---- | ---- | ---- |
| r | 读模式 |  |
| w | 写模式 |  |
| a | 追加模式 |  |
| b | 二进制模式 |  |
| + | 读写模式 |  |
文件读取 
```python
read() : 读到内存  
read(size) 读取一定字节
readline()  每次读取一行内容
readlines()  一次读取所有内容
close ()
```

使用 **with** 关键字系统会自动调用 f.close() 方法， with 的作用等效于 try/finally 语句是一样的。
我们可以在执行 with 关键字后检验文件是否关闭：
```python
with open('./test_runoob.txt', 'w') as file:  
    file.write('hello world !')
```
- 获得当前Python脚本工作的目录路径：os.getcwd（）。
- 返回指定目录下的所有文件和目录名：os.listdir（）。例如返回C盘下的文件：os.listdir（“C：\\”）
- 删除一个文件：os.remove（filepath）。
- 删除多个空目录：os.removedirs（r“d：\python”）。
- 检验给出的路径是否是一个文件：os.path.isfile（filepath）。
- 检验给出的路径是否是一个目录：os.path.isdir（filepath）。
- 判断是否是绝对路径：os.path.isabs（）。
- 检验路径是否真的存在：os.path.exists（）。例如检测D盘下是否有Python文件夹：os.path.exists（r“d：\python”）
- 分离一个路径的目录名和文件名：os.path.split（）。例如：
·os.path.split（r“/home/qiye/qiye.txt”），返回结果是一个元组：（‘/home/qiye’，‘qiye.txt’）。
·分离扩展名：os.path.splitext（）。例如os.path.splitext（r“/home/qiye/qiye.txt”），返回结果是一个元组：（‘/home/qiye/qiye’，‘.txt’）。
·获取路径名：os.path.dirname（filetpah）。
·获取文件名：os.path.basename（filepath）。
·读取和设置环境变量：os.getenv（）与os.putenv（）。
·给出当前平台使用的行终止符：os.linesep。Windows使用‘\r\n’，Linux使用‘\n’而Mac使用‘\r’。
·指示你正在使用的平台：os.name。对于Windows，它是‘nt’，而对于Linux/Unix用户，它是‘posix’。
·重命名文件或者目录：os.rename（old，new）。
·创建多级目录：os.makedirs（r“c：\python\test”）。
