# **1. STACK**

## 1.1 스택의 개념

    후입선출 (LIFO, Last In First Out) 방식
    -> 가장 마지막에 삽입된 자료가 가장 먼저 삭제되는 구조
<br/>
<p align="center"><img src="../images/stack.png" width="350" alt="stack"></img></p>
<br/>
<br/>

## 1.2 스택의 특징
    - 정해진 방향으로만 쌓을 수 있으며 top 으로 정한 곳을 통해서만 접근할 수 있다.
    - 삽입되는 새 자료는 top이 가리키는 자료의 위에 쌓이게 되며 스택에서 자료를 삭제할 때도 top을 통해서만 가능하다.
<br/>

## 1.3 스택의 장/단점
    - top 을 통해 접근하기 때문에 데이터 접근, 삽입, 삭제가 빠르다.
    - top 위치 이외의 데이터에 접근할 수 없기 때문에 탐색이 불가능하다. 탐색하려면 모든 데이터를 꺼내면서 진행해야 한다.
<br/>

## 1.4 스택의 연산

    1. pop(): 스택에서 가장 위에 있는 항목을 제거한다.
    2. push(item): item 하나를 스택의 가장 윗 부분에 추가한다.
    3. peek(): 스택의 가장 위에 있는 항목을 반환한다.
    4. isEmpty(): 스택이 비어 있을 때에 true 를 반환한다.
<br/>


## 1.5 스택의 사용방법
```java
Stack stack = new Stack();

stack.push(1);
stack.push(3);
stack.push(5);

System.out.println(stack.pop()); //5반환
```
<br/>

# **2. QUEUE**
## 2.1 큐의 개념
    선입선출 (FIFO, First in first out) 방식
    -> 가장 먼저 들어간 데이터가 가장 먼저 삭제되는 구조
<br/>

<p align="center"><img src="../images/queue.png" width="450" alt="queue"></img></p>
<br/>
<br/>

## 2.2 큐의 특징
    - 정해진 곳에서 삽입, 삭제가 이루어지는 스택과 달리 큐는 한쪽 끝에서 삽입 작업이, 다른 쪽 끝에서는 삭제 작업이 양쪽으로 이루어진다.
    - 삭제 연산만 수행되는 곳을 프론트(front), 삽입 연산만 이루어지는 곳을 리어(rear)로 정하여 각각의 연산작업만 수행된다.  
    - 리어에서 이루어지는 삽입 연산을 인큐(Enqueue)라 부르며 프론트에서 이루어지는 삭제 연산을 디큐(Dequeue)라고 부른다.
<br/>

## 2.3 큐의 장/단점

    - 데이터 접근, 삽입, 삭제가 빠르다.
    - 큐 역시 스택과 마찬가지로 중간에 위치한 데이터에 대한 접근이 불가능하다.
<br/>

## 2.4 큐의 연산
    1. Enqueue(삽입)하는 메서드 
        add(value), offer(value) 제공
    2. Dequeue(삭제)하는 메서드 
        remove(), poll() 제공
    3. 맨 앞에 있는 요소를 꺼내는 메서드 
        element(), peek() 제공

    ※ add(value), remove(), element() 와 offer(value), poll(), peek()의 차이점은?
    -> 예외를 발생시키는가 아니면 null이나 false를 반환하는가!!
<br/>

## 2.5 큐의 사용방법
```java
Queue queue = new LinkedList<>();

queue.add(1);
queue.offer(2);

//현재 queue에는 1,2가 담겨있음

queue.remove(); //1꺼내짐
queue.poll(); //2꺼내짐

queue.element(); //큐가 비어서 예외 발생
queue.peek(); //큐가 비어서 null 반환
```