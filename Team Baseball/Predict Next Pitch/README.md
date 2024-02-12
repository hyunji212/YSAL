<개요>
strategic pitch location - the role of two pitch sequences in pitching success by John Z. Clay의 칼럼을 통해 pitch location 을 이용해 Markov chain을 이용해 투수들을 그룹화 할 수 있다는 것을 접함. 이 후 이 그룹화한 결과를 새로운 column으로 넣어주어 다음 투구를 예측하는 데에 활용하고자 함

<diff>
- 위 칼럼에선 투수 location을 13개로 나눠 location에 대한 그룹화만 진행하였지만, 사용하는 구종으로 transition matrix를 만든 뒤 그룹화를 진행


<코드>
- data preprocessing.ipynb :92개의 칼럼을 feature selection을 이용해 17개로 줄이고 세분화된 구종을 6개로 묶어줌
- pitcher group.ipynb : type과 zone별로 투수의 transition matrix를 만들어준뒤 elbow plot을 활용해 적당한 그룹 (=5) 개수를 정하고 해당 결과를 바탕으로 kmeans를 진행하여 그룹을 만들어줌
- zone modeling.ipynb : zone group만 활용하여 다음 타구 예측에 활용
- type modeling.ipynb : type group만 활용하여 다음 타구 예측에 활용 (group없이 진행한 예측 포함)

model은 pycaret의 결과, 두 경우 모두에서 좋은 성능을 가진 xgboost classifier 사용.

<결과>
No group : 0.6180
type : 0.6187
zone : 0.8897

type은 그룹화하지 않은 경우보다 아주 소폭 예측력이 좋아졌고,
zone은 크게 상승함.

</br>

(자세한 내용은 ppt 참조)