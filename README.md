# SwordTarget-OFFER
## 剑指OFFER的题目
1.二维数组查找。<br>
自己的思路：将二维数组每一行当做一个数组。然后分别对其进行对半搜索，搜索到则停。时间复杂度大概为O（nlogm），n为二维数组行数，m为二维数组列数。<br>
参考答案思路：由于二维数组左下角的元素是这一行的最小元素，同时也是这一列的最大元素，那么从这个位置开始对比，若目标元素大则往右走，若目标元素小
则往左走。
