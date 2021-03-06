
## public static void main(String[] args)
자바 프로그램의 시작지점!  
하나의 클래스에는 하나의 main 메소드만 있을 수 있다.  
### main 메소드에서 `static`의 의미:  
메소드가 클래스 내의 특정 객체에 대해 정의 되는 것이 아니라 클래스에 대해서 정의된다는 의미  
main으로부터 인스턴스를 호출하려면 객체를 생성한 후, 그 객체에서 인스턴스 메소드를 호출해야 함. (다른 static 메소드의 경우, 직접 호출 가능)  

-----------
### 메소드

1. 멤버 메소드(Member Method)  
  1-1. static 메소드  
  1-2. 인스턴스 메소드  
  
2. 비멤버 메소드(Non-member Method)  
   ex) main 메소드  

#### 1-1. static 메소드  
  1) 클래스 로드 (+ static 메소드가 메모리에 할당됨->바로 사용 가능)  
     ```java
     // java.lang 패키지 내의 클래스는 프로그램 실행시 자동으로 로드되므로 이 코드를 쓸 필요 없음
     import java.lang.Math;
     ```
  
  2) static 메소드 활용  
     ```java
     double d = Math.random();
     // public static double random()
     ```
     * Math.random() 메소드와 같은 결과를 내는 인스턴스 메소드  
       ```java
       import java.util.Random;   // 클래스 로드
       Random r = new Random();   // 객체 생성
       double d = r.nextDouble(); // 메소드 활용 // public double nextDouble()
       ```
       
     
#### 1-2. 인스턴스 메소드  
  1) 클래스 로드  
     ```java
     import java.util.Scanner;
     // java.util 패키지에 있는 Scanner라는 클래스를 불러옴
     ```
  2) 객체 생성 (+ 인스턴스 메소드가 메모리에 할당됨)  
     ```java
     Scanner sc = new Scanner(System.in);
     // System.in은 InputStream(클래스)의 객체임
     // 인스턴스 sc가 생성
     ```
     - 객체와 인스턴스 차이  
       - 객체: 소프트웨어 세계에 구현할 대상   
         붕어빵틀(class)로 `붕어빵`을 만들어야지~! (아직 안 만듦!!)           
       - 인스턴스: 소프트웨어 세계에 구현된 실체 (메모리에 할당됨)  
         붕어빵틀로 `붕어빵`을 구웠다!! (먹을 준비!!)  
         
  3) 인스턴스 메소드 활용  
     ```java
     int n = sc.nextInt();
     // 인스턴스인 sc를 통해서 nextInt() 메소드를 호출
     ```

___
 [메소드 내용 참조](http://kin.naver.com/qna/detail.nhn?d1id=1&dirId=1040201&docId=64370479&qb=7J247Iqk7YS07IqkIOuplOyGjOuTnCDtgbTrnpjsiqQg66mU7IaM65Oc&enc=utf8&section=kin&rank=1&search_sort=0&spq=0&pid=gKa/Cwoi5Ulssu0DroZsss--072431&sid=TMF@qbRSwUwAAEYZTLA)  
 [객체와 인스턴스 차이](http://cerulean85.tistory.com/149)  
