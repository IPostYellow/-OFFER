# SwordTarget-OFFER
## 剑指OFFER的题目
### 按难度顺序查看：[简单](### 简单)<br>
### 简单：<br>
1.[二维数组查找](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E4%BA%8C%E7%BB%B4%E6%95%B0%E7%BB%84%E6%9F%A5%E6%89%BE.py)<br>
直接思路：将二维数组每一行当做一个数组。然后分别对其进行对半搜索，搜索到则停。时间复杂度大概为O（nlogm），n为二维数组行数，m为二维数组列数。运行时间221 ms，占用内存5732K<br>
参考答案思路：由于二维数组左下角的元素是这一行的最小元素，同时也是这一列的最大元素，那么从这个位置开始对比，若目标元素大则往右走，若目标元素小则往左走。运行时间205 ms，占用内存5852K<br>
2.[替换空格](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E6%9B%BF%E6%8D%A2%E7%A9%BA%E6%A0%BC.py)<br>
直接思路:将字符串以" "为分割点分割。然后再用"20%"组合起来。运行时间32 ms，占用内存5724K<br>
参考思路:直接使用replace方法将" "替换成"20%"。运行时间23 ms，占用内存5752K<br>
不使用函数自己写的思路:遍历一遍字符串，同时生成一个新的字符串，遍历到空格的时候生成字符串的时候生成"%20"。运行时间24ms，占用内存5860K<br>
3.[从尾到头打印链表](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E4%BB%8E%E5%B0%BE%E5%88%B0%E5%A4%B4%E6%89%93%E5%8D%B0%E9%93%BE%E8%A1%A8.py)<br>
直接思路:和链表逆置挺像的，头插法插入列表里。如果没有insert方法的话。用堆栈放进去再弹出来。运行时间30 ms，占用内存5728K<br>
4.[重建二叉树](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E9%87%8D%E5%BB%BA%E4%BA%8C%E5%8F%89%E6%A0%91.py)<br>
直接思路:先序-》第一个是根节点-》中序中寻找到这个根节点，然后将左右切分，左边的结点个数就是根节点左子树的结点个数。去先序接着根找依次这个个数的片段，找到后，又第一个是根节点，以此类推。运行时间66ms，占用内存5984K<br>
5.[二叉树的深度](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E4%BA%8C%E5%8F%89%E6%A0%91%E7%9A%84%E6%B7%B1%E5%BA%A6.py)<br>
直接思路:递归把每个子树的高度都算出来，递归停止条件是空树，递归返回是max{左子树高度，右子树高度}+1(当前层)。运行时间23ms,占用内存5752K。<br>
参考思路:或者借助队列使用层次遍历方法，在开始时记录队列长度，然后将这个长度的个数的元素依次出队列，出队时如果此结点还有左右子树，那么将其左右子树入队。在队列长度个元素出队之后，树的高度+1。运行时间46ms,占用内存5736K<br>
6.[不用加减乘除运算符做加法](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E4%B8%8D%E7%94%A8%E5%8A%A0%E5%87%8F%E4%B9%98%E9%99%A4%E5%81%9A%E5%8A%A0%E6%B3%95.py)<br>
直接思路:转换成列表型的二进制，然后用if判断来模拟手算二进制的情况，重点在于要补位。（此方法提交时内存溢出）<br>
参考思路:使用位运算符进行操作，两数异或后在左移一位取得进位。值得注意的是，此方法对于C/JAVA来说即使遇到异号数相加大于0的情况也最终会溢出并计算出正确结果，但是python是没有位数限制的，会不断无限的迭代至负无穷，所以对于此类情况应该反着来计算，并将最后结果取反。运行时间20ms，占用内存5860K<br>
7.[构建乘积数组](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E6%9E%84%E5%BB%BA%E4%B9%98%E7%A7%AF%E6%95%B0%E7%BB%84.py)<br>
直接思路:使用双重循环直接实现。外层循环是传入的列表的长度，内层循环是列表中元素的乘积，遇到索引相同的则跳过这次循环。运行时间33ms，占用内存5716K<br>
参考思路:经过分析可以发现，B[i]=C[i]\*D[i],其中C[i]=A[0]\*A[1]*...*A[i-1]，D[i]=A[i+1]*...*A[n],则不难发现C[i]=C[i-1]*A\[i-1\](i=1,2...n),C[0]=1。D[i]=D[i+1]*A\[i+1\](i=0,1...n-1)，D[n]=1。有此规律，直接使用两个for循环计算出C和D数组。运行时间27ms，占用内存5816K<br>
8.[变态台阶跳](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E5%8F%98%E6%80%81%E8%B7%B3%E5%8F%B0%E9%98%B6.py)<br>
直接思路:通过数学归纳法可以得到n台阶有的跳法为2^(n-1)。则可以直接得到结果。运行时间32 ms，占用内存5840K。<br>
参考思路:设n级台阶能够有的跳法数为f[n]，则很显然f[n]=f[n-1]+f[n-2]+...+f[0]（上一层在n-1层再跳1层+上一层在n-2层再跳2层...上一层没有再跳n层）。运行时间26ms，占用内存5860K<br>
9.[二叉树的镜像](https://github.com/IPostYellow/SwordTarget-OFFER/blob/master/%E4%BA%8C%E5%8F%89%E6%A0%91%E7%9A%84%E9%95%9C%E5%83%8F.py)<br>
直接思路:使用递归方法不断交换节点的左右子树。运行时间22ms,占用内存5876K。<br>
间接思路:消去递归，使用堆栈，将根节点压入栈中，然后开始循环：若栈不空，出栈一个元素，并交换其左右节点，然后再将其左右节点入栈。否则结束。运行时间21ms，占用内存5736K。<br>
