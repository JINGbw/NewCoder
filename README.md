# NewCoder
剑指Offer 66题刷题笔记
## 数组

1. [二维数组的查找](https://github.com/JINGbw/NewCoder/blob/master/%E6%95%B0%E7%BB%84/%E4%BA%8C%E7%BB%B4%E6%95%B0%E7%BB%84%E7%9A%84%E6%9F%A5%E6%89%BE.cpp)
- 题目：二维数组从左到右依次变大，从上到下依次变大，找到目标数字
- 思路：法一：利用二分法找到该数所在的行，再用二分法找到这个数。法二：从左下角或者右上角开始找，可以根据Target与当前元素的大小关系来缩小查找区间

2. [把数组排成最小的数](https://github.com/JINGbw/NewCoder/blob/master/%E6%95%B0%E7%BB%84/%E6%8A%8A%E6%95%B0%E7%BB%84%E6%8E%92%E6%88%90%E6%9C%80%E5%B0%8F%E7%9A%84%E6%95%B0.cpp)
- 题目：把数组（int类型）里所有数字拼接起来排成一个数，打印能拼接出的所有数字中最小的一个
- 思路：1.重新定义排序函数中调用的比较函数cmp 并排序 2. 将排好序的数组拼接起来返回
 

3. [数组中重复的数字](https://github.com/JINGbw/NewCoder/blob/master/%E6%95%B0%E7%BB%84/%E6%95%B0%E7%BB%84%E4%B8%AD%E9%87%8D%E5%A4%8D%E7%9A%84%E6%95%B0%E5%AD%97.cpp)
- 题目：找到数组中任意一个重复的数字
- 思路：如果第i个数不等于i,就把第i个数换到i的位置去，如果第i个数那个数的位置 等于那个数，就说明找到了重复的数字

4. [构建乘积数组](https://github.com/JINGbw/NewCoder/blob/master/%E6%95%B0%E7%BB%84/%E6%9E%84%E5%BB%BA%E4%B9%98%E7%A7%AF%E6%95%B0%E7%BB%84.cpp)

- 题目：给定数组A[0,1,...n-1]，要求构建B[0,1,...n-1],其中B的元素B[i] = A[0]A[1]...A[i-1]A[i+1]...A[n-1]。要求不能使用除法
- 思路：循环B数组两遍，将B中结果拆成两部分乘积，一部分是下三角形，一部分是上三角形。
    - 1. B[0] = 1 ,i从1到n-1 ,$B[i]=B[i-1]* A[i-1]$ 
    - 2. i从n-2到0 ，$ tmp*= A[i+1], B[i] = B[i]* tmp$
    
5. [调整数组顺序使奇数位于偶数前面](https://github.com/JINGbw/NewCoder/blob/master/%E6%95%B0%E7%BB%84/%E8%B0%83%E6%95%B4%E6%95%B0%E7%BB%84%E9%A1%BA%E5%BA%8F%E4%BD%BF%E5%A5%87%E6%95%B0%E4%BD%8D%E4%BA%8E%E5%81%B6%E6%95%B0%E5%89%8D%E9%9D%A2.cpp)
- 题目：调整数组中数字的顺序，使奇数在偶数前面
- 思路：1.奇数放在前半部分，从原来数组的后面开始找 ,从前面插入到双端队列 2.偶数放在后半部分，从前开始找，插入双端队列的后面 

6. [连续子数组的最大和](https://github.com/JINGbw/NewCoder/blob/master/%E6%95%B0%E7%BB%84/%E8%BF%9E%E7%BB%AD%E5%AD%90%E6%95%B0%E7%BB%84%E7%9A%84%E6%9C%80%E5%A4%A7%E5%92%8C.cpp)
题目：找到给定数组中连续子数组的最大和
- 思路：动态规划的状态转移方程：
    - //dp[i] = array[0] , (i = 0 ) 
    - //dp[i] = max(dp[i-1]+array[i],array[i]); (i = 1,2 ,3 ... n-1) 

- （力扣）上有一题是求最长上升子序列的长度，不要搞混了 

7. [顺时针打印矩阵](https://github.com/JINGbw/NewCoder/blob/master/%E6%95%B0%E7%BB%84/%E9%A1%BA%E6%97%B6%E9%92%88%E6%89%93%E5%8D%B0%E7%9F%A9%E9%98%B5.cpp)
- 题目：按照顺时针的顺序打印出矩阵中的每一个数字 
- 思路：1.从左到右 2. 从上到下 3.从右到左 4.从下到上 注意循环截止条件 （3.4.的时候考虑）(只有一行或者一列的情况)

## 字符串
1. [替换空格](https://github.com/JINGbw/NewCoder/blob/master/%E5%AD%97%E7%AC%A6%E4%B8%B2/%E6%9B%BF%E6%8D%A2%E7%A9%BA%E6%A0%BC.cpp)
- 题目：请实现一个函数，将一个字符串中的每个空格替换成“%20”
- 思路：1. 遍历字符串，统计字符串的空格个数和非空格个数，得到替换后的长度      2. 从后往前替换，如果是空格就换为“%20”

4. [字符流中第一个不重复的字符]()


5. [字符串的排列（全排列）](https://github.com/JINGbw/NewCoder/blob/master/%E5%AD%97%E7%AC%A6%E4%B8%B2/%E5%AD%97%E7%AC%A6%E4%B8%B2%E7%9A%84%E6%8E%92%E5%88%97%EF%BC%88%E5%85%A8%E6%8E%92%E5%88%97%EF%BC%89.cpp)
- 题目：输入字符串求全排列
- 思路：递归让每个数字当第一个，循环截止条件：递归到了最后一个数字/每次递归结束后再换回来。
    - 递归的条件：1. 当前数字是第一个或者当前值与第一个值不等才会交换和递归
 
## c++

1. int 转 string 

to_string(x)

2. sort函数重写比较函数（从大到小排列）

static bool cmp(int x, int y){
return x>y?true:false;
}

3. 哈希表

unordered_map(int,int)res;//哈希表 
//查看哈希表中某个数字的数目：
res.count(20);
4. 是奇数/偶数

x%2 == 0 -> 是偶数 / x%2 == 1 -> 是奇数 

5. 复制一个数组 （把dq中的复制到array中)

array.assign(dq.begin(),dq.end());
