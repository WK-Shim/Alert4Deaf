# ALERT4DEAF - 청각장애인을 위한 인공지능 경보 시스템

# 💡 프로젝트 제작 동기
![image](https://github.com/WK-Shim/Alert4Deaf/assets/138008395/e74d18eb-3c22-40e8-8957-9fcc1779e8ce)
###### 화장실과 같은 시설이 사용 중인지 알 수 없는 청각장애인들


![image](https://github.com/WK-Shim/Alert4Deaf/assets/138008395/198dfd00-21d1-47e2-af3d-bdf37fcc6c6c)
###### 수돗물이 나오는 소리, 냉장고의 알림음 등을 듣지 못해 불편함을 겪는 청각장애인들


![image](https://github.com/WK-Shim/Alert4Deaf/assets/138008395/2f0f63fb-53e3-4130-9300-a9ba812a9743)
###### 긴급 상황에 사이렌이 울려도 인지하지 못해 제대로 대응할 수 없는 청각장애인들


사회에서 공존하며 살아가는 장애인들이 겪는 어려움들 중, 청각장애인들이 일상에서 소리가 잘 들리지 않아 발생하는 불편함들이 눈에 띄었습니다.
이 중 경보음이나, 대중교통 알림음 등의 부재로 발생하는 불편함들에 포커스를 맞추어 해당 소리들을 인식 및 구별, 진동으로 장애인에게 알려주는 기기를 제작하게 되었습니다.

# 📜 기획
## 형태
기본적으로 상시 신체 밖으로 노출이 되어야 하고, 그와 동시에 거동에 불편함을 제공하지 않기 위해
축구팀 주장들이 착용하는 스트랩에서 아이디어를 얻어 벨크로로 팔뚝에 착용하는 형태를 갖추게 되었습니다.

## 경고 방식
청각장애인이 과도한 자극을 받지 않는 동시에 확실하게 구별 가능한 자극 방식은 진동이라고 생각하여
내부에 진동모터를 내장해 가장 주요한 경보 기능으로 삼았습니다.

## 부가 기능
기본적으로 일상에서 착용하기를 목적으로 하는 제품이고, 착용방식의 특성상 최대한 간소화하는 것이 좋을 것 같아
전원 ON / OFF를 제외한 다른 특수한 기능들은 넣지 않기로 하였습니다.

# 🖱 개발
크게 소프트웨어와 하드웨어로 나누어 분류하였습니다.

---

# 💻 소프트웨어
## 🎵 샘플 수집
### 목적
청각장애인의 일상 속 불편함을 해소하고 위험·돌발 상황을 알리고자 하는 프로젝트의 목적에 따라
크고 작은 위험을 알리는 소리들을 녹음하였습니다.
### 수집
#### 샘플 수집
수집한 소리들에 따라 쉽게 접할 수 있는 소리들은 직접 녹음을, 쉽게 접할 수 없는 소리들은 인터넷에서 검색을 통해 수집하였습니다.
#### 배경음 수집
낮이나 밤, 지하철역 안이나 거리 등 다양한 시간대와 장소에서 주변 소리들을 녹음하였습니다.
### 모델 생성
Teachable Machine을 통해 입력받은 소리를 카테고리에 따라 분류하는 모델을 만들었습니다.
# 🔧 하드웨어
## 📋 워크플로우
주어진 기능을 수행하는 것에 초점을 맞추어 PCB를 먼저 디자인 후 하우징 CAD를 맞추어 디자인하였습니다.
## 📟 회로기판 | PCB
### 목적
- 작품의 완성도를 추구하기 위해 테스트 회로를 기반으로 기판을 제작했습니다.
- 몸에 부착되는 웨어러블에 속하기에 크기의 최소화를 목표로 삼았습니다.
- 부품 구성을 최소화하고 THT 부품들로 구성하여 제작이 용이하도록 디자인했습니다.
### 스케매틱
![image](https://github.com/WK-Shim/Alert4Deaf/assets/138008395/64fc0636-1f41-45a0-9bbc-265a156ccbd3)
- 라즈베리파이 피코, MAX9814의 일반적인 결선법을 사용했습니다. (Gain, AR 미사용)
- 충전모듈의 출력 GND를 스위치에 연결하여 ON/OFF를 구현했습니다.
### 디자인
#### 툴
JLCPCB와 연동되어있는 EasyEDA 웹 디자이너를 사용했습니다. 
#### 과정
![image](https://github.com/WK-Shim/Alert4Deaf/assets/138008395/28a8afc2-90f4-4de1-ae97-b7040a7e963d)
- 가장 중심이 되는 컴포넌트들을 배치했습니다.

## 📼 하우징 CAD
