## 0.3 배열회전
배열의 일부를 오른쪽으로 1만큼 회전시키는 right_rotate()함수를 작성하라.
<pre>
	static void right_ratate(int[] arr, int startIndex, int endIndex)
	{
		int i, last;
		last = arr[endIndex];
		for(i = endIndex; i > startIndex; --i)
		{
			arr[i] = arr[i - 1];
		}
		arr[startIndex] = last;
        </pre>
