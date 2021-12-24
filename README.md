# elastic-search-study
엘라스틱 서치 공부


<h1>엘라스틱 서치란?</h1>
엘라스틱 stack은 elasticsearch + logstash + kibana로 이루어져 있으며 ELK stack으로 불립니다. <br>
엘라스틱은 rest api를 지원을 해 http method를 사용을 해서 CRUD를 수행을 하며 <br>
데이터 저장은 역 index구조로 cluseter형식으로 저장이 되어 search를 하게 되면 HashTable처럼 O(1)의 속도로 빠르게 접근을 할 수 있습니다.<br>
데이터들은 Cluster > Node > Shard 단위로 저장이 된다.<br>


<h2>Filter</h2>
1. lowercase : 대문자를 소문자로 변환 ex. Castle -> castle<br>
2. stop : 관사 같은 해석에 필요 없는 단어 삭제 후 저장 ex. the, a, an 같은 단어 제거<br>
3. snowball : s나 ing같은 부분을 제거 하고 단어를 기본형으로 저장한다. ex. Studing > study<br>
이렇게 저장을 함으로써 검색할 시에 사용자는 추상적으로 검색이 가능하여 편리성이 증가된다. <br>

<h2>bool, range</h2>
