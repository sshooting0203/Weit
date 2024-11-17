<h1>사용한 데이터</h1>
<a href="https://www.kaggle.com/datasets/mnassrib/telecom-churn-datasets">Telecom Churn Dataset</a>
<p>통신 서비스 데이터의 고객 이탈을 결정트리로 예측하는 미니 프로젝트</p>

<p>샘플링 : 전체 데이터 집합이나 모집단에서 특정한 기준에 따라 일부 데이터를 선택하여 분석/처리하는 과정</p>
<ol>
  <li>확률적 샘플링 : 모든 데이터가 선택될 확률이 동일/예측 가능한 방식으로 샘플 선택</li>
  <li>비확률적 샘플링 : 특정 기준에 따라 데이터가 선택</li>
  <ul>
    <li>오버 샘플링 : 소수 클래스를 늘려서 학습(ex. SMOOTHE)</li>
    <li>언더 샘플링 : 다수 클래스를 줄여서 학습(ex. NearMiss)</li>
  </ul>
</ol>
<p>Yes클래스를(서비스를 그만둘 고객) 예측하는 것이 중요하지만, No클래스가 다수를 차지하는 상황</p>
<p>SMOOTHE 샘플링 기법을 통해 가상의 소스 클래스를 데이터를 생성하여 정확도를 향상</p>
<code>
  from imblearn.over_sampling import SMOTE
  # SMOTE를 사용하여 소수 클래스 증강
  smote = SMOTE(random_state=42)
  X_resampled, y_resampled = smote.fit_resample(X_train, y_train)
</code>
<img width="561" alt="teeele" src="https://github.com/user-attachments/assets/59452f64-bfec-442a-9f98-ec8b3c78b735">
