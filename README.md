# 이미지 분석 기반의 인공지능 플랫폼 개발자 양성과정 과정 수료 (주관 : 한국생산성본부)
- 기간 : 2020.06 ~ 2020.12

# NowMeal

# 프로젝트 소개 
- CNN 이미지 인식 기반 개인화 맞춤 레시피 추천 서비스
- 사용자 보유 재료 이미지를 인식하여 사용자의 취향, 재료/요리 히스토리 반영 추천을 목적으로 개발

# 팀 프로젝트 개요 
- 제작기간 : 3주
- 팀원 : 3명
  - 현동호 : 크롤링, CNN 모델개발, WebCam 인식, 웹 퍼블리싱
  - 이현경 : 기획, DB구축, 웹 퍼블리싱
  - 이재성 : 추천 모델 개발, 모델 평가, 웹 퍼블리싱
  
# 적용기술 
- DB : Oracle
- Language : Python + sklearn +  TensorFlow + Keras + OpenCV + UI/UX Template(Bootstrap)
- Open API : Selenium, BeautifulSoup, Numpy, Pandas, Matplot
- Framework : Flask

# 참여 부분
1. 데이터 수집 
- 구글 이미지 크롤링 이후 데이터 전처리 
  ![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/b1e4833b-2db2-44bb-a387-bf7a5532d2da)

2. 모델 개발 및 학습
- InceptionV3, VGG16, ResNet50 과 같은 이미 학습된 딥러닝 모델을 준비하여 Fine Tuning 전략을 사용해 모델 학습 후 학습된 모델을 파일로 저장 
- 학습 시간 대비 validation accuracy가 가장 높은 모델 선정 (val_acc : 0.976)
  ![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/406a7db3-89ff-41f7-90c8-6e1c53d264c3)


3. 실시간 Webcam 인식 시스템 구현
- 선정된 모델을 바탕으로 python 에서 openCV를 사용해 실시간으로 UI 구현
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/60cfa7db-9f64-4681-89a9-fd088730b8ce)


# 영상 
- Web Cam 인식 시스템 구현 영상 링크 : https://youtu.be/hTZ22nVsckw

# 회고록 
- 프로젝트를 하면서 어려웠던 점이 있었는데 첫 번째는 딥러닝 관점에서 이미지 분류 문제를 푸는 것이였다. 내가 준비한 라벨링 된 데이터 종류는 5개인데 어떻게 학습을 시킬 것인지 처음에는 감이 오지 않았었다.
하지만 구글링을 통하여 여러 레퍼런스 될만한 자료를 찾을 수 있었고 그 중 Transfer Learning 기법이 높은 정확도를 비교적 짧은 시간 내에 달성할 수 있다는 사실을 알게 되었으며 이를 적용하게 되었다.
따라서 Fine Tuning 전략을 사용해 사전에 학습된 모델을 내 프로젝트에 맞게 재정의하여(데이터셋 크기와 유사성 비교) 적절한 전략을 선택 할 수 있었으며 classifier와 convolutional base의 높은 레벨 계층(뒷단의 계층) 일부만 학습시키면서
개발을 진핼 할 수 있었다.
- 두 번쨰로 어려웠던 점은 실시간 식재료 인식 시스템 구현이였다. webcam을 통하여 식재료 인식을 해야 할 때 실재 식재료를 사용하여 인식하고 싶었지만 내가 구성한 데이터 셋은 흰색 바탕에 식재료 이미지였다.
그 결과 매 Frame에서 객체 추출 시 원활하게 객체 인식을 하지 못하는 문제가 있었다. 따라서 실시간으로 흰색 바탕의 식재료 이미지로 테스트를 진행 할 수 밖에 없었는 데, 여기서 양파, 홍고추는 제대로 객체 인식과 bounding box가 생겼으나
무는 객체 인식에 성공 했지만 무의 흰색 부분이 바탕과 차이가 미미하여 정확한 bounding box가 생기지 않는 아쉬움이 있었다. 다음에 이러한 문제를 푼다면, 지금 보다 많은 이미지 셋을 구축하여 모델을 학습을 해야겠다고 생각했고
경계선 검출에 관한 알고리즘을 찾아보거나 여러 레퍼런스를 찾아 봐서 구현 해야겠다고 생각했다.  


# WebPage
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/e2ef0f92-c3c5-4816-8529-057593706b82)
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/d8ab251f-dab8-4fbe-9427-5cc57c234cda)
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/6251b49f-6618-4986-b0a4-f9e957762ed8)
![image](https://github.com/HyunDongHo/NowMeal/assets/46379443/198bd427-08fc-4bc9-a4c3-e463df35cb58)

