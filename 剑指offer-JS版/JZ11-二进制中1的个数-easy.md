### 题目描述
请实现一个函数，输入一个整数，输出该数二进制表示中 1 的个数。例如，把 9 表示成二进制是 1001，有 2 位是 1。因此，如果输入 9，则该函数输出 2。



### 思路

n & (n-1)可以每次消掉一个1。用count来计数，当n变为0,执行了几次就有几个1

### 代码

```js
function NumberOf1(n)
{
    let count = 0;
    while(n){
        n = n &(n - 1);
        count++;
    }
    return count;
}
```

