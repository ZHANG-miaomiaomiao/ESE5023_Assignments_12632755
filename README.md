# ESE5023_Assignments_12632755

Comments on HW1 Liyl (92/100)

First, you don't need to add “.txt” to .py files; “.py” or “.ipynb” is fine.

1-2: Good writting! I only has a small suggestion: you can define M matrix lengeth by "len(M[0])",
rather than a 5*5 zeo matrix, which will make your function "Matrix_multip" can apply to matrix products of other lengths.

1-5: you defined dfs(1,"1"),this will hard-coding the first item
as `“1”` did not account for multi-digit leading numbers
(such as `12+3...`, `123+4...`, and `123456789`). you can:

    def dfs(pos, current_expr):
        if pos == len(digits):
            if eval(current_expr) == target:
                print(current_expr + " = " + str(target))
            return
        for i in range(pos, len(digits)):
            num_str = digits[pos:i + 1]
            if pos == 0:
                dfs(i + 1, num_str) # 首项可以是一/多位数，前面不加符号
            else:
                dfs(i + 1, current_expr + "+" + num_str)
                dfs(i + 1, current_expr + "-" + num_str)
    dfs(0, "")  #从 0 开始，而不是 dfs(1, "1")

5.2 Same mistake as in 5.1, also you didn't draw a graph; 
you just created a text histogram using `“*” * quantity`. (-8p)
    

