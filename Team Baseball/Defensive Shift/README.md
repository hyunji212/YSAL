주제 : 수비시프트의 효과

<두 개의 하위 프로젝트로 나누어서 실행>

Project 1. MLB 데이터로 보는 수비 시프트의 효과 </br>
project 2. KBO 중계 이미지를 이요한 시프트 여부 판단

-> MLB에서는 타구의 낙하지점, 수비수의 위치 등 다양한 데이터를 제공해주어 데이터를 이용하여 수비 시프트를 분석할 수 있었지만 
kbo는 제공되는 데이터가 한정적이어서 MLB와 같은 분석이 불가능했다. 따라서 두 개의 프로젝트로 나눠 MLB 데이터로는 수비시프트의 효과 파악, KBO에선 중계 이미지를 이용해 수비수의 좌표를 파악하여 수비 시프트 여부를 파악하는 모델을 만드는 프로젝트를 진행하였다.

<기여>
project2 기획, 파이프라인 제작 , ppt 제작, 발표 등 전과정에 참여하였다.

<project2 목표>
수비수들의 좌표를 3차원 이미지에서 2차원 평면으로 근사시킨 뒤 나온 4개의 좌표를 넣어 수비시프트 여부를 판별하는 모델 제작.

<library>
  - open cv
  - Yolo
  - tensorflow 

  <code>
    - infielder cor.ipynb (파일 크기가 커 CRLF로 저장)
    - shift classifier.ipynb
</br></br>
  (자세한 내용은 ppt 참조)







