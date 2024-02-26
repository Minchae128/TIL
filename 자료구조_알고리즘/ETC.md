# 코딩테스트에 필요한 자바
## 1. int VS long
- int  : -2147483648 ~ 2147483647
- long : -9223372036854775808 ~ 9223372036854775807
     
<img width="515" alt="Snag_32b9718f" src="https://github.com/Minchae128/TIL/assets/122027566/36f0bb06-b447-45fb-bf6a-32f4aaa30300">
<br>
<br>

### 보통 long로 많이 선언한다 WHY??

> 코딩테스트에서는 문제의 답이나 풀이 과정에서 **자료형의 범위를 넘어가는 경우**가 종종 있습니다.
<br><br>
**Case1.** 모든 자료형에서 표현이 불가능한 경우 -> 정답 값을 XX로 나눈 나머지를 출력하세요.
<br><br>
**Case2.** int 로는 불가능하고 long으로 표현 가능한 경우 -> 별도 언급 없음

<br>

**이럴 때 의심해보세요!!**
<br>
-> 특정 테스트 케이스에서 **실패**
<br>
-> 테스트 케이스 성공! But **믿지 마세요** 

<br>

> Ex)
<br>int answer = 1000000000;
<br>answer += 2000000000;
<br>System.out.println(answer);
<br>**= -1294967296**
<br><br>long answer = 1000000000;
<br>answer += 2000000000;
<br>System.out.println(answer);
<br>= 3000000000

<span style="font-size: 25px;"><b>웬만하면 long 사용!!!</b></span>

## 2. Scanner VS BufferedReader 
### 코딩테스트에서 Scanner 보다 **BufferedReader**이 더 좋다!!
### WHY? 
<img width="500" alt="Snag_32ebcd48" src="https://github.com/Minchae128/TIL/assets/122027566/eace151c-6ce3-4f39-b7e9-fbd5c94d4d5f">
<br><br>

> **이럴 때 의심해보세요!!**
<br>
-> 시간 초과로 **실패**

> 사용법 비교 Ex)
<br>입력값이 Input data : 1, 2, 3 일때,
<br><br>**Scanner**
<br>Scanner sc = new Scanner(System.in);
<br>int a = sc.nextint();
<br>int b = sc.nextint();
<br>int c = sc.nextint();
<br>**= 간단하게 3개의 변수에 값을 저장할 수 있음**
<br><br>**BufferedReader**
<br>BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
<br>**=  BufferedReader 객체 생성하고 그안에 InputStreamReader객체를 생성해 주어야 합니다.**
<br><br>StringTokenizer st = new StringTokenizer(br.readLine());
<br>**또한, readLine함수로 받으면 한줄씩 String형태로 받게 됩니다. 때문에 StringTokenizer생성해 받아주어야 합니다.**
<br><br>int a = Integer.parseInt(st.nextToken());
<br>int b = Integer.parseInt(st.nextToken());
<br>int c = Integer.parseInt(st.nextToken());
<br>**=  StringTokenizer로 받은 값을 int형태로 파싱까지 해주어야 합니다.**
<br><br>**Scanner보다 BufferedReader 더 복잡하지만 BufferedReader가 더 빠르다.**


<br>
<span style="font-size: 25px;"><b>입력 데이터가 많다면 BufferedReader 사용!!</b></span>

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
