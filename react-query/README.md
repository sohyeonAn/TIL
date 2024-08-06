# react-query

### QueryClient

- `QueryClient`는 데이터 캐시와 쿼리 상태 관리를 위해 사용되기 때문에 `react-query` 의 핵심이라 볼 수 있다.
- 앱이 재렌더링 되더라도 캐시가 유지될 수 있도록 가장 상위 컴포넌트의 외부에서 생성한다.
- 리액트 외부에서 생성한다면 컴포넌트에서 상호작용하기 위해 `QueryClientProvider` 를 사용해야 한다.
  - 변경되지 않는 "정적 객체" 로 전달되기 때문에 재렌더링을 걱정할 필요 없다.

### QueryClientProvider

- `react-query` 에서 `context`는 상태관리를 위해 사용한다기 보단 하위 컴포넌트들이 `queryClient`에 "접근" 할 수 있게 하기 위해 사용한다.

---

### useQuery

- `useQuery` 를 통해 캐시와 상호작용 한다.
- `queryCache`를 구독하고 있어서 캐시에서 관심있는 데이터가 변경될 때마다 컴포넌트를 재렌더링 할 수 있다.
