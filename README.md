# SwordTarget-OFFER
## 剑指OFFER的题目
1.二维数组查找。<br>
自己的思路：将二维数组每一行当做一个数组。然后分别对其进行对半搜索，搜索到则停。时间复杂度大概为O（nlogm），n为二维数组行数，m为二维数组列数。运行时间221 ms，占用内存5732K<br>
参考答案思路：由于二维数组左下角的元素是这一行的最小元素，同时也是这一列的最大元素，那么从这个位置开始对比，若目标元素大则往右走，若目标元素小
则往左走。运行时间205 ms，占用内存5852K<br>
2.替换空格。<br>
第一次的思路:将字符串以" "为分割点分割。然后再用"20%"组合起来。运行时间32 ms，占用内存5724K<br>
第二次的思路:直接使用replace方法将" "替换成"20%"。运行时间23 ms，占用内存5752K<br>
不使用函数自己写的思路:遍历一遍字符串，同时生成一个新的字符串，遍历到空格的时候生成字符串的时候生成"%20"。运行时间24ms，占用内存5860K<br>
3.从尾到头打印链表。<br>
直接思路:和链表逆置挺像的，头插法插入列表里。如果没有insert方法的话。用堆栈放进去再弹出来。运行时间30 ms，占用内存5728K<br>
4.重建二叉树<br>
直接思路:先序-》第一个是根节点-》中序中寻找到这个根节点，然后将左右切分，左边的结点个数就是根节点左子树的结点个数。去先序接着根找依次这个个数的片段，找到后，又第一个是根节点，以此类推<br>
5.二叉树深度<br>
直接思路:递归把每个子树的高度都算出来，递归停止条件是空树，递归返回是max{左子树高度，右子树高度}+1(当前层)。或者借助队列使用层次遍历方法，在开始时记录队列长度，然后将这个长度的个数的元素依次出队列，出队时如果此结点还有左右子树，那么将其左右子树入队。在队列长度个元素出队之后，树的高度+1。
