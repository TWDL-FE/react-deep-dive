## 메모이제이션

- `useMemo`, `useCallback`, `memo`는 리액트 렌더링을 최소한으로 줄이기위해 제공된다.
  ### 필요한 곳에만 메모이제이션 추가하기
  - 메모이제이션도 비용이 드는 작업이다. 값을 비교하고, 재계산이나 렌더링이 필요한지 확인하고, 결과물을 저장해 뒀다가 꺼내오는 비용이 발생한다.
  - 대부분의 가벼운 작업은 매번 새로 작업을 하는게 더 빠를 수 있다.
  - 만능이었다면 이미 기본적으로 사용하도록 패치되었을 것이다.
  - 예측하는 섣부른 최적화가 아닌, 앱을 어느정도 만든 이후에 개발자도구나 `useEffect`를 활용해서 필요한 곳에서만 최적화 한다.
  ### 모두 메모이제이션 하기
  - 일부 컴포넌트에서는 메모이제이션 하는 것이 성능에 도움이 된다.
  - 앱의 규모가 커지면 최적화에 시간을 쏟기 힘들다. 그냥 다 해버리는게 낫다.
  - 리액트의 재조정 알고리즘을 활용하면 실제로 발생하는 비용이 비교 뿐이다. 다 하는게 다 안하는 경우의 잠재적 비용보다 비용이 적게 든다.
