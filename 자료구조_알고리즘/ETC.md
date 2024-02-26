# 코딩테스트에 필요한 자바
## 1. int VS long
- int  : -2147483648 ~ 2147483647
- long : -9223372036854775808 ~ 9223372036854775807
     
<img width="515" alt="Snag_32b9718f" src="https://github.com/Minchae128/TIL/assets/122027566/36f0bb06-b447-45fb-bf6a-32f4aaa30300">
<br>
<br>

> 코딩테스트에서는 문제의 답이나 풀이 과정에서 **자료형의 범위를 넘어가는 경우**가 종종 있습니다.
<br><br>
**Case1.** 모든 자료형에서 표현이 불가능한 경우 -> 정답 값을 XX로 나눈 나머지를 출력하세요.
<br><br>
**Case2.** int 로는 불가능하고 long으로 표현 가능한 경우 -> 별도 언급 없음
<br><br>
**이럴 때 의심해보세요!!**
<br>
-> 특정 테스트 케이스에서 **실패**
<br>
-> 테스트 케이스 성공! But **믿지 마세요** 

> Ex)
<br>
int answer = 1000000000;
<br>
answer += 2000000000;
<br>
System.out.println(answer);
<br>
**= -1294967296**
<br>
<br>
long answer = 1000000000;
<br>
answer += 2000000000;
<br>
System.out.println(answer);
<br>
= 3000000000

> **웬만하면 long 사용!!!**

## 2. Scanner VS BufferedReader 
## 3. i++ VS ++i
## 4. Array 오름차순 정렬 VS Array 내림차순 정렬
## 5. Comparable
## 6. static 변수
## 7. for VS while
## 8. if VS switch
## 9. 정답을 XX을 나눈 나머지를 출력하세요.
## 10. ArrayList 배열

# Reference
* https://www.youtube.com/watch?v=x-cYdsjfVKU&list=PLFgS-xIWwNVXv1mM7cH1X4ycjB47z1EL-