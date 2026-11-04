# ESE5023\_Assignments\_12632755

Comments on HW1 Liyl (92/100)

First, you don't need to add “.txt” to .py files; “.py” or “.ipynb” is fine.

1-2: Good writting! I only has a small suggestion: you can define M matrix lengeth by "len(M\[0])",
rather than a 5\*5 zeo matrix, which will make your function "Matrix\_multip" can apply to matrix products of other lengths.

1-5: you defined dfs(1,"1"),this will hard-coding the first item
as `“1”` did not account for multi-digit leading numbers
(such as `12+3...`, `123+4...`, and `123456789`). you can:

&#x20;   def dfs(pos, current\_expr):
if pos == len(digits):
if eval(current\_expr) == target:
print(current\_expr + " = " + str(target))
return
for i in range(pos, len(digits)):
num\_str = digits\[pos:i + 1]
if pos == 0:
dfs(i + 1, num\_str) # 首项可以是一/多位数，前面不加符号
else:
dfs(i + 1, current\_expr + "+" + num\_str)
dfs(i + 1, current\_expr + "-" + num\_str)
dfs(0, "")  #从 0 开始，而不是 dfs(1, "1")



5.2 Same mistake as in 5.1, also you didn't draw a graph;
you just created a text histogram using `“\\\*” \\\* quantity`. (-8p)



HW2 from Lijh（100/100）

1.作业整体完成情况较好,数据读取和最终排序存在问题，部分结果可能受到影响。



2.代码正确，



3.部分结果展示不完整，闰年对 DOY 气候态的影响未得到处理



4.整体完成度较高，但部分数据筛选条件缺少明确依据。

你的作业AI痕迹比较明显，且未在pdf文档内说明，我们不希望你过度依赖AI工具完成作业，请自己独立思考

