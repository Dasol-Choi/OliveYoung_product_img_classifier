# OliveYoung product classifier
### 프로젝트 개요
 * 올리브영 화장품 30종의 이미지를 분류하는 모델 설계 
 * 추후에 이미지로 화장품을 검색하는 어플리케이션 개발
### Dataset
 * 총 1,8000장의 올리브영 기초케어 화장품 이미지 (총 30종, 각 class 당 600장)
 * 10개의 서로 다른 올리브영 매장에서 직접 촬영한 이미지 60% + 웹사이트에서 크롤링한 이미지 40%로 구성
### Modeling
 * transfer learning model - 대표적인 CNN 모델 4가지를 기반으로 한 전이학습
   * ResNet
   * MobileNet
   * VGG16
   * Xception
 * my model
   * mobileNet의 depthwise 층을 활용한 경량화 모델
   * image size 1/2로 축소
### 평가
 * MobileNet, VGG16, Xception 세 가지 모델에서 0.97 5 ~0.99의 Test Accuracy 기록 
 * ResNet의 경우 상대적으로 저조한 0.479의 Accuracy 기록 
 * 경량화한 my model에서는 최대 0.95의 Accuracy 기록 -> 추후 성능 향상 시도 예정 
