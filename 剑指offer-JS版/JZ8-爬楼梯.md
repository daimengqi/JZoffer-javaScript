### 题目描述
一只青蛙一次可以跳上1级台阶，也可以跳上2级。求该青蛙跳上一个n级的台阶总共有多少种跳法（先后次序不同算不同的结果）

### 思路一：dp

### 代码一

```js
function jumpFloor(number)
{
    if(number == 1) return 1
    if(number == 2) return 2;
    let dp = new Array(number).fill(0);
    dp[1] = 1, dp[2] = 2;
    for(let i = 3; i <= number; i++){
        dp[i] = dp[i-1] + dp[i - 2];
    }
    return dp[number];
}
```
