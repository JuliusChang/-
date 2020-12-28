# Vim命令

### 插入

i  当前光标前插入

a 当前光标后插入

I 当前行首插入

A 当前行尾插入



### 移动

w 移动到下一单词首字符

e 移动到当前单词首字符

home 移动到行首

end 移动到行尾

### 编辑

#### 删除

S 删除当前行

D 从光标位置删除一直到最后

“+p  从系统剪切板复制

c% 删除下一个括号匹配内容，并放入系统剪切板

```java
//例如将下述代码用变量替换
if (!entry.used && equivalent(entry.key(),qk.key())  && (curcontext & entry.contexts))
    
//替换后的样子
bool equiv = equivalent(entry.key(),qk.key());
if (!entry.used && equiv  && (curcontext & entry.contexts))
    
//步骤1
//在nomal模式下将光标切换到需要替换变量 使用c%命令
if (!entry.used &&   && (curcontext & entry.contexts))
//键入equiv，并切换到nomal模式，输入O ，输入bool equiv =
bool equiv = 
if (!entry.used && equiv  && (curcontext & entry.contexts))
//在nomal模式键入"+p就完成了，你学废了吗？
```

