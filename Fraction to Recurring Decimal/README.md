#第一百六十六题
##Fraction to Recurring Decimal

计算除法，结果转换成字符串，循环部分用括号括起来
###版本1
这一题的通过率是14%，但是又是一道media的题目，我就立刻明白了，这一题是非常多的边界条件要处理的题目。然后最后我还是提交了7次才通过，正好14%的通过率。囧Rz。

1. 第一次超时，未考虑无限循环之前，分子和分母不一定化简到了最简的情况，于是遇上1/6超时。
2. 忘记考虑负数
3. 忘记最小的负数的补是本身
4. 改为long long 之后，遇上1/99这种循环要写成0.(01)的情况，我写成了0.0(10)的情况，未考虑到这种提前很多久已经最简的情况
5. 加负号放在了最后，而余数为0直接返回了，负号忘记添上（已经傻了，胡乱就提交）
6. 忘记考虑-0要写成0
7. 终于通过了。