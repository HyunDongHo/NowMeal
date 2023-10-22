# NowMeal

# 프로젝트 소개 
- CNN 이미지 인식 기반 개인화 맞춤 레시피 추천 서비스
- 사용자 보유 재료 이미지를 인식하여 사용자의 취향, 재료/요리 히스토리 반영 추천을 목적으로 개발

# 팀 프로젝트 개요 
- 제작기간 : 3주
- 팀원 : 3명
  
# 적용기술 
- DB : Oracle
- Language : Python + sklearn +  TensorFlow + Keras + OpenCV + UI/UX Template(Bootstrap)
- Open API : Selenium, BeautifulSoup, Numpy, Pandas, Matplot
- Framework : Flask

# 참여 부분
1. 데이터 수집 
- 구글 이미지 크롤링 이후 데이터 전처리 

2. 모델 개발 및 학습
- InceptionV3, VGG16, ResNet50 과 같은 이미 학습된 딥러닝 모델을 준비하여 Fine Tuning 전략을 사용해 모델 학습 후 학습된 모델을 파일로 저장 
- 학습 시간 대비 validation accuracy가 가장 높은 모델 선정 (val_acc : 0.976)

3. 실시간 Webcam 인식 시스템 구현
- 선정된 모델을 바탕으로 python 에서 openCV를 사용해 실시간으로 UI 구현


# 영상 
- Web Cam 인식 시스템 구현 영상 링크 : https://youtu.be/hTZ22nVsckw

# WebPage
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/e2ef0f92-c3c5-4816-8529-057593706b82)
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/d8ab251f-dab8-4fbe-9427-5cc57c234cda)
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/6251b49f-6618-4986-b0a4-f9e957762ed8)
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/198bd427-08fc-4bc9-a4c3-e463df35cb58)

