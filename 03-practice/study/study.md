## Side Effect

UI 렌더링, 사용자 입력에 반응하여 필요시 UI 렌더링이다.

Side Effect는 어플리케이션에서 일어나는 렌더링 이외의 다른 모든 것을 뜻한다.

Side Effect를 처리하는 더 좋은 도구가 필요하다. 특별한 리액트 훅을 사용하면 된다.
=> useEffect hook

### useEffect 함수

- useEffect(()=>{...},[dependencies]);
- 두개의 매개변수, 두 개의 인수와 같이 호출됩니다.
- 첫번째 인수는 함수 : 모든 컴포넌트 평가 후 실행되어야 하는 함수이다. 지정된 의존성이 변경된 경우라면
- 두번쨰 인수는 지정된 의존성으로 구성된 배열이다.
- 의존성이 변경될 때마다 첫번째 함수가 다시 실행된다.

따라서 첫번째 함수에 어떤 sideEffect라도 넣을수 있다. 그 코드가 지정한 의존성이 변경된 경우에만 실행될 것이다.

컴포넌트가 다시 렌더링될 떄는 실행되지 않는다.

의존성이 변경된 경우에만 실행된다.

### useEffect() 종속성

- effect 함수에서 사용하는 "모든 것"을 종속성으로 추가해야함.
- 예외
  - 상태 업데이트 기능을 추가 할 필요 없음.
  - "내장" API 또는 함수를 추가할 필요 없음.
  - 변수나 함수를 추가할 필요 없다.

---