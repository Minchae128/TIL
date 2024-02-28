# 코딩테스트에 필요한 자바
## 1. int VS long
- int  : -2147483648 ~ 2147483647
- long : -9223372036854775808 ~ 9223372036854775807
     
<img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/36f0bb06-b447-45fb-bf6a-32f4aaa30300">
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
<img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/eace151c-6ce3-4f39-b7e9-fbd5c94d4d5f">
<br><br>

**이럴 때 의심해보세요!!**
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

## 3. ++i VS i++ 
- ++i : 전위연산자 (이기적 / 나 먼저)<br>
<img width="500" 
src="https://github.com/Minchae128/TIL/assets/122027566/f03a39e8-021c-4e85-8987-94d832512e63">
<br><br>
- i++ : 후위연산자 (이타적 / 다른 거 먼저)<br><img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/525cf88a-2210-4e89-be15-2715cbd30de5">

<br>
<span style="font-size: 25px;">++i 그리고 i++ <b>동작방식의 차이를 이해하고 사용하기!!</b></span>

## 4. Array 오름차순 정렬 VS Array 내림차순 정렬
- 오름차순(ASC) : 갈수록 숫자가 커지는 정렬 (1 -> 2-> 3 -> 4 -> ...)
- 내림차순(DESC) : 갈수록 숫자가 작아지는 정렬 (5 -> 4 -> 3 -> 2 -> 1)

> Ex)<br> <img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/2fb780ad-0f34-47c3-beca-19d69bc5a055">
<br> - 오름차순 : Arrays.sort()
<br><br><img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/44c20361-954f-4aec-aa88-da800c8cbe08">
 <br> <b>이 내림차순 방법은 아주 깔끔하지 않음 WHY?</b>
<br> - 내림차순을 하기 위해 <br>&nbsp;&nbsp;<b>Collections.reverseOrder()</b>사용 (Collections.reverseOrder()는 객체 형태만 적용 가능 그래서 배열선언을 Integer로 함)
<br><br><img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/1be2a3a8-952a-4e8e-bd34-aa40c6c5336c">
 <br> <b>이 방법은 친근한 int로 로직을 이어갈 수 있어 좋지만, 문법이 길어 외우기 힘들다.</b>
 <br><br><img width="395" src="https://github.com/Minchae128/TIL/assets/122027566/3869fb4f-0bf0-4073-8ab1-7a0565f805b0">
 <br> 이방법은 -1을 곱하는것이 어려울 수 있다.

## 5. Comparable (데이터 정렬)
- sort : 단일 기준
- Comparable : 정렬 기준이 여러 개

> Ex)<br><img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/f420c611-1fc6-4a69-9d7e-347f7927a6f2"><br><img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/09c42358-0f55-4904-919d-c5885df947f7">
<br><img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/edb3d676-c6f3-4c1d-b869-00309e13a727">
<br>내림차순으로 정렬할때<br><img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/8063c4d8-dada-4e13-8d4f-58c45b05bfd5">
<br><img width="500" src="https://github.com/Minchae128/TIL/assets/122027566/1fb93de9-d9cb-4805-922a-41c7ba6943f0">

## 6. static 변수


## 7. for VS while


## 8. if VS switch


## 9. 정답을 XX을 나눈 나머지를 출력하세요.


## 10. ArrayList 배열

# Reference
* https://www.youtube.com/playlist?list=PLFgS-xIWwNVXv1mM7cH1X4ycjB47z1EL-
