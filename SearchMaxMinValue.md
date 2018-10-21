# 최대와 최소
### Q.최대 값과 최소 값을 구하는 함수

간단한 문제부터 시작하자. 두 개의 정수(int 형)를 인자로 받아서 둘 중 큰 값을 반환하는 함수  max()와
둘 중 작은 값을 반환하는 함수 main()을 작성하자.

### 내가 적은 답
<pre>
package src;
public class Main {
static int Max(int value1, int value2)
{
    if(value1 > value2)
    {
        return value1;
    }
    else
    {
        return value2;
    }
}
       
static int Min(int value1, int value2)
{
    if(value1 < value2)
    {
        return value1;
    }
    else
    {
        return value2;
    }
}     
</pre>

### 문제풀이 답
<pre>
static int Max(int value1, int value2)
{
    if(value1 > value2)
        return value1;
    return value2;
}
       
static int Min(int value1, int value2)
{
    if(value1 < value2)
        return value1;
       
    return value2;
}
</pre>


### Q.배열의 최대 값을 구하는 함수

정수 배열에서 가장 큰 값을 반환하는 함수max_arr()을 작성해보자.
배열과 배열의 크기를 인자로 받는다.

### 내가 적은 답
<pre>
static int max_arr(int arrSize, int[] arr)
{
    int maxValue = 0;
    int count = arrSize/2;
    if(arrSize%2 == 1)
    {
    ++count;                   
    }
    
    System.out.println("count:"+count);
    for(int i = 0; i < count; ++i)
    {
        int temp = arr[i];
        int temp2 = arr[arrSize - 1 - i];
                                  
        int bigCount = temp;
        if(temp < temp2)
        {
            bigCount = temp2;
        }
                     
        if(bigCount > maxValue)
        {
            maxValue = bigCount;
        }
    }
              
    return maxValue;
}
</pre>

### 문제풀이 답
<pre>
static int max(int x, int y)
{
    if(x > y)
        return x;
    return y;
}
static int max_arr2(int[] arr, int arrSize)
{
    if(arrSize == 1)
        return arr[0];
    else
    return max(arr[arrSize - 1], max_arr2(arr,arrSize - 1));
}
</pre>

### 문제풀이
* int[] intArr = {1, 7, 3}; 일 때 <br/>
1. max_arr2(intArr, 3);
2. arrsize != 1
3. max(3, max_arr2(arr, 2));
4. arrsize != 1
5. max(7, max_arr2(arr, 1));
6. arrsize == 0 이므로 return 1;
7. 5번으로 되돌아가서 max(7, 1) 이므로 return 7
8. 3번으로 되돌아가서 max(3,7) 이므로 return 7
9. 가장 큰 수는 7