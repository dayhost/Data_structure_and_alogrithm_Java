# Valid Parentheses
### 问题
Given a string containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid. The brackets must close in the correct order, "()" and "()[]{}" are all valid but "(]" and "([)]" are not.
### 解题思路
- 这个问题属于字符串处理，一般情况下会把字符串转化成字符的数组（char array）然后利用一些处理list或者array的方式来解题。对于本题来说，我们可以看到整个字符串里同样类型的括号应该是对应的，所以解题的关键在于如何判断对称。
- 这个问题存在两种情况需要处理：1，字符串是左右对称的，比如"[{()}]"，2，字符串不是左右对称的，比如"{}[]()"。这两种情况都可以根据“遇到右括号就消耗掉一个相应的左括号”模式。这样我们就需要把左括号都存起来，遇到右括号就删除对应的左括号
- 我们需要一个线性的存储空间，比如说list，queue，stack来存储左括号。在这里我们选用stack，它具有“后进先出”的特性，就是说后压入栈的元素会先弹出站，可以想象成一个箱子，先放进去的衣服会先拿出来
- 这样，我们就先scan整个char array，遇到左括号就存起来，遇到右括号就把元素从栈中弹出来一个，判断弹出的左括号是不是和右括号相同类型的，如果相同就接着scan，不相同就报错（return false）
### 代码
[code at github](https://github.com/dayhost/Leetcode/blob/master/ValidParenthes.java)
### 边界问题
- 写完代码之后，我们要讨论一下边界条件，也就是说在我们刚才考虑的两种可能性之外的情况，比如说传入字符串为空，或者只有一个左括号，或者只有一个右括号的情况，考察边界条件是否成立是解体很重要的的一环
- 我们讨论一下边界情况：
- 1.字符串为空，我们应该返回true，因为null也应该是valid。 
- 2.只有一个左括号，我们在scan完整个string之后会发现我们的括号的stack并不为空（如果valid应该为空），应该返回false。
- 3.如果只有右括号，我们在代码中每次遇到右括号都会检查stack是否为空，如果为空就return false

	
