# mongodb-practice
mongodb를 공부하면서 기억해야할 점 및 샘플 소스


# executionStats
- `db.getCollection('collection').find({...query...}).explain('executionStats')`로 호출하면 `queryPlanner`외에 실제 실행에 관한 정보를 `executionStats` 필드에서 추가적으로 확인 할 수 있다
- `executionStats.nReturned: 8` - 실제로 조회될 도큐먼트수
- `executionStats.executionTimeMillis: 333` - 실행에 걸리는 시간 ms
- `executionStats.totalKeysExamined: 88` - todo
- `executionStats.totalDocsExamined: 82` - 실제 조회건 추출을 위해 고려되는 도큐먼트 수
- `executionStats.executionStages.totalChildMillis` - todo
- `executionStats.executionStages` - 샤드별로 대상 추출건 수, 실행시간, 리턴되는 도큐먼트수 등을 알 수 
