스택(Stack)
===========

'쌓다'. 스택은 후입선출 , LIFO방식을 사용한다. 즉 한쪽 끝에서만 데이터를 넣고 뺄 수 있는 자료구조이다.
Stack은 데이터의 조회, 추가, 삭제 모두 가장 최근 값에서 시작된다. 그리고 최 상단 데이터를 Top이라 한다.

Java에서의 Stack 클래스
===========
자바에서의 Stack Class는 따로 지원해준다.
기본적으로 Stack<Element> stack = new Stack<>(); 으로 생성할 수 있다.
 
지원하는 함수는
  <pre>
  <code>
public Element push(Element item); //데이터 추가
public Element pop(); //최근 추가된 데이터 삭제
public Element peek(); //최근 추가된 데이터 조회
public boolean emply(); //Stack의 값이 비었는지 확인
public int seach(Object o); //인자값으로 받은 데이터의 위치 반환
</code>
</pre>
 
 #### 예제
 <pre>
 <code>
Stack<Integer> stack = new Stack<>();
        for (int i = 0; i < 5; i++) {
            stack.push(i + 1);
            System.out.println(stack.peek());
        } // 1, 2, 3, 4, 5 가 현재 들어가 있음
        stack.pop(); // 1, 2, 3, 4
        System.out.println(stack.peek()); // 4
        System.out.println(stack.search(1)); // 4
        System.out.println(stack.empty()); // false
</code>
</pre>
pop은 후입선출이므로 가장 늦게들어온 5가 빠져나감
search동작 방식은 -> 인덱스를 반환하는 것이 아니라, 순번을 반환하는 것. 즉 값이 몇번째에 있는지를 반환하는 것임.
