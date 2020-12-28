# Sungply :: Realtime Music Recommender

## Summary
```
추천시스템의 실시간성 향상을 위한 Load Balanced Music Recommender model 제작
< Tag입력시 해당Tag와 관련된 음악 추천 >

1. 기간 : 2020.09 ~ 2020.12
2. 내용 : 로드밸런싱을 이용한 추천시스템의 실시간성 향상
3. 개인 기여
- Data process 
- Embedding(Skip-Gram model) 
- Clustering(Kmeans Clustering)
- Load Balancer(self made algorithm)
4. Challenge
- 데이터의 범위 설정 및 전처리
- 새로운 기술의 습득 및 적용
- Learning Curve(Python-Dataframe, embedding, clustering algorithm, version managemnet)
5. 결과요약 
- 베이스라인 모델 대비 약 4~6배 성능향상(latency 측정) --> Neural CF 모델과 비교
- 정확성 저하X(Recall, Precision 측정) --> Neural CF, SVD 모델과 비교
```
Contributors
- joqjoq966 (https://github.com/joqjoq966)
- csy1204 (https://github.com/csy1204)
- sallyeric (https://github.com/sallyeric)



## Env

```
python 3.8
Node v12
```
## Web Demo

http://49.50.162.241:3000/


## Result

### Latency
- 성능향상(시간단축) 비교
```
All(Neural CF) : Baseline 1
v1 : Using only 1 cluster
v2 : Using load balanced model
```

![image](https://user-images.githubusercontent.com/18041103/101727712-5bb7ba80-3af8-11eb-86be-003d90110204.png)

### Recall
- 실제 True(추천되어야 할 음악)인 것 중 모델이 True(추천한 음악)라고 예측한 비율
```
All(Neural CF) : Baseline 1
v1 : Using only 1 cluster
v2 : Using load balanced model
SVD : Baseline 2
```
![image](https://user-images.githubusercontent.com/18041103/101727721-62463200-3af8-11eb-84fe-ec28416fa0ff.png)

### Precision
- 모델이 True(추천한 음악)라고 분류한 것 중 실제 True(추천되어야 할 음악)의 비율
```
All(Neural CF) : Baseline 1
v1 : Using only 1 cluster
v2 : Using load balanced model
SVD : Baseline 2
```
![image](https://user-images.githubusercontent.com/18041103/101727737-6a05d680-3af8-11eb-83c1-be0693cbe069.png)




