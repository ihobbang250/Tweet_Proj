# [Private5th] Twitter Sentiment Analysis

## Pre-Processing

트위터 텍스트라 전처리에서 성능이 크게 달라졌습니다. 전처리 방식은 아래와 같습니다.

1) 은어 처리, 해시 태그 처리

2) 특수, 구두문자, URL 처리

3) Contractions, Abbreviation 처리

4) N-gram 이용하여 Acronym 처리

## Pretrained Model

Bertweet-large : based on the RoBERTa pretrained 850M English Tweets

## Enviroment

Saturn Cloud : A10G-G54XLarge - 16 cores - 64 GB RAM - 1 GPU - 40Gi Disk

## Result

Text Augmentation 사용 결과 성능 저하로 인해 사용X

Hugging face Trainer API 사용

사전 학습 모델과 감정 라벨이 달라 변환을 해주었습니다.

일정 학습 뒤에 Overfitting이 발생해 Early Stop을 적용하였습니다.

Validation loss 가장 낮은 모델과 F1 score가 가장 높은 모델 중

F1 score가 가장 높은 모델이 더 높은 점수를 도출했습니다.

따라서 예측 시, 해당 모델을 불러와 추론에 사용했습니다.
