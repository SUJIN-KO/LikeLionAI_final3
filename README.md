# LikeLionAI_final3
LikeLion AI 멋쟁이사자처럼 파이널 프로젝트 3팀 

<img src="https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcDRMJ7%2FbtqYxpaq9P5%2FUzOTR5qIHDumg5pmj6apyK%2Fimg.png"/>

# WISH099 프로젝트 
[![made-with-Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)](http://commonmark.org)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/ohahohah/readme-template/graphs/commit-activity) 
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

> WISH099 프로젝트는 시각장애인의 이동권을 보장하기 위해 시작되었습니다.  
- www.wish099.com (3월 배포 예정)
- 자세한 Code 와 PT 파일은 **wish099** branch에서 확인 가능합니다

​
## Walk assistant Object Detection
-- Where I SHould Head WISH 0.99 project
​
​
​
본 프로젝트는 공공 데이터 구축 목적인 AI HUB '인도(人道) 보행 영상 AI데이터'를 통해 데이터가 제공됩니다. (https://www.aihub.or.kr/aidata/136)
인도 보행 데이터를 통해 우리나라 보행 도로 중 존재하는 물체을 분석하고, Yolov5를 이용해 분석된 도로의 물체나 방해물을 인식하는 모델입니다.
​
​
​
## INTRODUCTION
​
WISH 0.99 프로젝트는 시각적으로 어려움을 겪는 이들의 이동권 확보를 위한 것으로 시작했습니다. WISH는 14만장의 인도 보행에 있어서 장애가 되는 
객체 29종에 대해 '박스'형태로 annotation한 데이터(images, xml files)를 학습 후 yolov5모델과 결합하여 도보에 있는 장애물들을 인식합니다.
​
​
추후에 깊이 인식과 음성 알림이 가능하다면, 웨어러블 기기로 영상을 입력받고 다가오는 위험물체에 대한 알림을 전달할 수 있습니다.
 
WISH 0.99는 모두의 이동이 자유롭고 안전하길 바랍니다.
​
​
## INSTALLATION
​
Our current implementation is tested on:
                Python 2.7
                openCV 2.4.9
                Yolov5 
(더보기-> requirements.txt)
​
​
​
## USE
​
```
  -- train
     |-- images
     |   |-- MP_SEL_000001.jpg
     |   |-- MP_SEL_000002.jpg
     |   |-- MP_SEL_000003.jpg
     |   |-- MP_SEL_000004.jpg
     |   |-- ...
     |-- label
     |   |-- MP_SEL_000001.xml
     |   |-- MP_SEL_000002.xml
     |   |-- MP_SEL_000003.xml
     |   |-- MP_SEL_000004.xml
     |   |-- ...
-- test
     |-- images
     |   |-- MP_SEL_000008.jpg
     |   |-- MP_SEL_000009.jpg
     |   |-- MP_SEL_000010.jpg
     |   |-- MP_SEL_000011.jpg
     |   |-- ...
     |-- label
     |   |-- MP_SEL_000008.xml
     |   |-- MP_SEL_000009.xml
     |   |-- MP_SEL_000010.xml
     |   |-- MP_SEL_000011.xml
     |   |-- ...
-- valid
     |-- images
     |   |-- MP_SEL_000013.jpg
     |   |-- MP_SEL_000014.jpg
     |   |-- MP_SEL_000015.jpg
     |   |-- MP_SEL_000016.jpg
     |   |-- ...
     |-- label
     |   |-- MP_SEL_000013.xml
     |   |-- MP_SEL_000014.xml
     |   |-- MP_SEL_000015.xml
     |   |-- MP_SEL_000016.xml
     |   |-- ...
```     
     
1. WISH 0.99의 실습은 모두 colab으로 이용합니다.Yolov5실습을 위해서는 GPU설정을 꼭 해주세요.
2. colab에서 실습이 끝났으면, 원하는 객체가 담긴 영상을 업로드하고 분석하면됩니다.
3. 학습 --> 
<!python train.py --img 416 --batch 16 --epochs 50 --data ../data.yaml --cfg  models/yolov5s.yaml --weights '' --name aihub>
4. 결과도출 -->
<!python detect.py --weights /content/yolov5/runs/train/aihub/weights/best.pt  --conf 0.4 --source 영상.mp4>
​
​
## Contacts
​
> 강혜승 kanghazel1@gmail.com
> 고수진 khucomsujin@likelion.org
> 김연주 rladuswn7@likelion.org
> 신원희 wonhee1104@gmail.com
> 허정은 huhjobs@gmail.com
​
​
### all rights reserverd  - likelion 인공지능 1기 final project  

