# Is it AI?
AI로 생성된 이미지인지 아닌지 판별하는 모델을 개발 및 배포하여 cv 모델 설계 복습 및 MLOps를 익히는 것이 목적.

# TODO

- [ ] 웹에서 AI/non-AI 이미지 크롤링  
- [ ] binary classification 모델 설계  
- [ ] 모델 배포  
- [ ] 테스트 결과를 자동으로 수집해 학습하는 환경 구축

# 1. 웹에서 AI/non-AI 이미지 크롤링
- 크롤링 대상: 겔부루, 단부루, 픽시브
- 태그를 사용해 AI/non-AI, sfw 이미지 크롤링
- GUI 프로그램으로 완성하는 것이 목표
- 참고
  - https://github.com/Akaisorani/pixiv-crawler
  - https://github.com/savantshuia/poolbooru_gelscraper
  - https://github.com/20chan/danbooru-py

# 2. 이미지 판별
## 2-1. binary classification model
- 일단은 resnet으로 실험 후 정확도에 따라 모델 변경 예정
- 주피터가 아닌 .py로 코드 나눠서 설계 예정

1. Cat vs Dog dataset으로 mvp 제작 후 dataset 변경  
참고: https://junstar92.tistory.com/121

## 2-2. Classification model
- StableDiffusion, StyleGAN3 등 모델 별 이미지를 클래스로 두고 학습해 input 이미지가 어떤 클래스에 가장 가까운지 판별

## 2-3. Trace detector
- Frequency-domain에서의 model간 trace를 비교
- 논문 참고: [링크](https://velog.io/@hanlyang0522/On-the-detection-of-synthetic-images-generated-by-diffusion-model)
