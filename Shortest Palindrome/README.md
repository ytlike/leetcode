#第二百一十四题
##Shortest Palindrome
在一个字符串前添加最短的字符串，使其成为回文串
###版本1
使用最直接的想法，从中间往前反复推断是否可以添加成为回文串，果然遇到长的就超时了。

###版本2
还是需要利用字符串自身的特性，加快回文串匹配判断，这里有两种解法，
第一种是利用最长会问子串中，给串中添加#，然后找到开头为s[0]的最长回文子串，该方法不详细解释，可以看上一题。

第二种办法就是利用KMP匹配的方法了，具体方法如下：   
1. 求字符串s的翻转s_rev   
2. 将两个字符串进行拼接：{s}#{s_rev}   
3. 找出新字符串中最长公共前缀后缀长度comLen   
4. s_rev.substring(0, s.length() - comLen)就是在原字符串头部插入的子串部分


其中，找出comLen就是KMP算法的用处了，具体不再详细解释，可以查看


> http://blog.csdn.net/v_july_v/article/details/7041827