# Outer Product Convolutional DeepCF Using Side Information
+ Collaborative Filtering을 기반으로 한 DeepCF 아키텍처를 발전시켜 소비자의 Item 선호 정보와 소비자의 부가정보, Item의 정보 등을 폭넓게 추천 시스템에 반영할 수 있는 Outer Product Convolutional DeepCF with Side Information을 제안
+ 기존 DeepCF의 Aggregation Function인 Concatenation이나 Element-wise와 다르게 소비자와 아이템 간의 상관관계를 충분히 반영할 수 있도록 Outer Product 방식을 이용해 2D Interaction map을 생성
+ Side Information을 Embedding한 값을 활용해 또 하나의 Feature Map을 생성
+ 최종적으로는 만들어진 Feature map들을 Convolutional Layer를 통과시켜 예측에 활용+ 캐글의 도서 데이터를 이용해 제안 모델의 성능과 기존 DeepCF 모델의 성능을 비교 실험하였으며, 제안 모델이 앞서는 것을 확인
  - 1. DeepCF vs DeepCF with Outer Product&CNN: 약 4.2% 성능 향상
  - 2. DeepCF vs Contain Side Information: 약 9.9% 성능 향상
+ 결론
  - 1. 기존 DeepCF 아키텍처에 ONCF에서 활용된 Outer Product라는 새로운 Aggregation Function을 사용하여 성능 향상과 더불어 유의미한 상관관계 도출
  - 2. Structured, Text, Image data를 활용한 Side Information 구조를 제안함으로써, 다른 데이터셋의 다양한 종류의 Side Information에서도 활용 가능하다는 일반화 가능성 도출
