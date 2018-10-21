# 0.2 두 변수의 값 바꾸기
### Q.값을 바꾸는 함수 Swap 만들기

<pre>
public class SwapEx {
       static void Swap(int[] a, int[] b)
       {
              int temp = a[0];
              a[0] = b[0];
              b[0] = temp;
       }

       public static void main(String[] args)
       {
              int[] a = new int[] {1};
              int[] b = new int[] {2};
              System.out.println("a:"+a[0]+" b:"+b[0]);
              Swap(a, b);
              System.out.println("a:"+a[0]+" b:"+b[0]);
       }
}
</pre>

### How to Write a basic swap function in Java?
https://stackoverflow.com/questions/3624525/how-to-write-a-basic-swap-function-in-java/3624566
