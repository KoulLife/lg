### 개별 IF의 수행 시점, 처리 시간, 레코드 수, Msg Size 확인

<details>
<summary>접기/펼치기</summary>
    
    **처리 시간**
    
    - 목적
        - 병목 구간 혹은 성능 파악을 위해 SLO, SLA 파악도 가능
    - 데이터 타입
        - Histogram 사용 가능할 것으로 판단
    - 시각화
        - 타임시리즈
    
    **수행 시점**
    
    - 목적
        - 이벤트 발생 시간 확인, 교차 검증
    - 데이터 타입
        - DateTime
    - 시각화
        - Bar Chart
        
    
    **레코드 수**
    
    - 목적
        - 추세 확인
    - 데이터 타입
        - 카운터
    - 시각화
        - Bar Chart
    
    **메세지  사이즈**
    
    - 목적
        - 데이터 볼륨 변화 파악
    - 시각화
        - Bar Chart
</details>

___

### 개별 IF의 컨슈머별 통계 정보

<details>
<summary>접기/펼치기</summary>
    - 시각화
        - Table 형태로 만들고 클릭 시, 드릴 다운으로 상세 조회로 넘어가게 한다.
        - 사용량 혹은 에러별로 Bar Chart를 구성
    - 목적
        - IF를 많이 사용하는 컨슈머 동향 파악
</details>

___

### 일간 / 주간/ 월간 총 트랜잭션 양 추이 확인

<details>
<summary>접기/펼치기</summary>
    - 목적
        - 전체 시스템의 사용 추이를 확인, 이상 징후 혹은 용량 계획 가능
    - 방법
        - 카운터와 increse 함수를 사용하여 일간 / 주간/ 월간동안 누적 트랜잭션 수 계산
    - 시각화
        - Time Series
</details>

___

### 대량 호출 건에 대한 식별

<details>
<summary>접기/펼치기</summary>
    - 목적
        - 시스템에 과부하를 줄 수 있는 특정 트랜잭션을 식별
    - 시각화
        - Table 형태 클릭시 로그 상세 보기
</details>

___

### 시스템 별 담당자 에러 알림 셋팅

<details>
<summary>접기/펼치기</summary>
    
    비즈니스 파악이 우선이라고 생각.
    
    0(위험)단계 부터, 5(주의) 까지 설정하여
    이메일 알람, 슬랙 알람, pagerduty 등으로 확대
</details>

___

### 로깅 항목 또는 옵션의 조정(Leveling)

<details>
<summary>접기/펼치기</summary>
    - 리벨링의 목적과 의도 파악을 하지 못함
    - warn, error, infro 와 같은 로깅을 바꾼다라고 하면 JMX 혹은 application.yml에서 수정해야하는 것 아닌가?
</details>

___

### 특정 시스템 또는 IF 별 로그 레벨링 (X)
