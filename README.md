# KCGS2023-Establishing-an-XR-Studio-with-Anti-Glare-Monitors-Case-Studie

## 안티글레어 모니터를 이용한 XR 스튜디오 구성 및 작품 제작 사례*

[프로젝트 페이지](https://cg.catholic.ac.kr/~mgchoi/publications/XRStudio/)

[DBpia](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE11492748)

[원본 논문 읽기](https://github.com/Cybecho/KCGS2023-Establishing-an-XR-Studio-with-Anti-Glare-Monitors-Case-Studie/blob/main/XR%EC%8A%A4%ED%8A%9C%EB%94%94%EC%98%A4_KCGS2023.pdf)

Dept. of Media Technology and Media Contents, The Catholic University of Korea
 - Kyungmin Na
 - Byunguk So
 - Dohee kim
 - Seonmin Yoon
 - Myung Geol Choi
  
```
* 구두발표논문
* 본 논문은 학부생 발표 논문임
* 이 성과는 정부(과학기술정보통신부)의 재원으로 한국연구재단
의 지원을 받아 수행된 연구임 (No. 2021R1F1A1048002)
```

<br/>

> 요약

본 연구는 안티글레어 모니터를 사용하여 가상의 배경 을 만들고 그 앞에 실제 상품을 두고 촬영하는 XR 스튜 디오 구현 방법을 제시한다. 
가상의 배경과 실제 사물 사이의 조명 일치를 위해 강한 조명의 사용이 필요하다.
하지만 강한 조명은 모니터 화면에 반사되는 글레어를 유발하여 가상 배경의 신뢰성을 떨어뜨린다. 
본 연구에 서는 안티글레어 필름을 적용한 모니터를 사용하여 물 리적 글레어를 최소화한 후 남아있는 글레어를 이미지 처리 기술로 제거하여 가상 배경의 신뢰성을 높이는 방 법을 제시한다. 
이러한 과정을 통해 실제 상품을 촬영하는 소형 스튜디오에서 XR 스튜디오 구성하는 방법을 제시한다.

<br/>

> 1. 서론

XR (eXtended Reality) 스튜디오는 대형 LED 화면에 가상의 배경을 출력하고 그 앞에 실제 피사체를 두고 촬영하는 방식으로, 주로 가상 배경 위에 사람 등의 실 체 피사체를 합성하여 촬영하는 목적으로 사용된다[1].
이러한 방식은 촬영하는 사람과 연기하는 사람 모두 현 장에서 가상 환경을 확인하면서 작업할 수 있다는 장점 이 있다. 
또한 많은 후반 작업이 요구되는 크로마키 방 식과는 달리 가상환경의 빛이 실물 피사체 표면에 반사 되거나 굴절하는 효과가 직접 표현되고 촬영되므로 전 체 작업 시간을 크게 절약할 수 있다. 
하지만 일반적으로 XR 스튜디오 시스템은 사람 피사체를 고려하여 넓은 공간에 막대한 비용이 투자되어 건설되므로 작은 상품 을 주로 촬영하는 소형 스튜디오에서는 적용하기 어렵다. 
본 연구에서는 비교적 작은 상품을 촬영하는 소형스튜디오에서도 XR 스튜디오의 장점을 누릴 수 있도록 하기위해 TV용 모니터를 이용하여 XR 스튜디오 환경을 구성하는 방법을 제안한다.
피사체를 가상의 배경 속에 존재하는 것처럼 보이도록 하기위한 가장 중요한 요소는 조명의 차이를 최소화하 는 것이다. 이를 위해 피사체에 여러 가지 인공 조명을 비추어 조명 조건을 최적화해야 한다. 하지만 조명의 사용은 모니터 화면에 글레어를 유발하며, 가상 배경에 대한 신뢰성을 크기 떨어뜨리게 된다. 이미지 상의 글레어 를 제거하는 기술은 활발히 연구되고 있으나[2] 여전히 고해상도 이미지에 대한 완전한 글레어 제거는 어려운 문제로 여겨지고 있다. 본 연구에서는 먼저 안티글레어 필름을 적용한 모니터를 사용하여 물리적 글레어를 최소화한 후 남아있는 글레어를 간단한 이미지 처리 기술로 제거하는 방법을 제시한다.

![스크린샷 2024-05-22 233502](https://github.com/Cybecho/KCGS2023-Establishing-an-XR-Studio-with-Anti-Glare-Monitors-Case-Studie/assets/42949995/211c4bc9-a039-4545-b7b7-9de6450423fb)

<br/>

> 2. 소형 XR스튜니오 구성 

Figure 1은 본 연구에서 구성한 소형 XR 스튜디오 실험 환경을 나타낸다. 가상 환경 출력을 위한 모니터로안티글레어 필터가 장착된 삼성 더 프레임 85인치QLED TV를 사용하였다. 피사체를 비추는 조명으로SmallRig RC 120 모델 조명과 색 변화가 가능한 여러가지 소형 LED 조명을 사용하였다. 촬영 시 카메라의 공간상 위치와 방향을 측정하고 기록하기 위해 카메라 상단에 바이브 모션 트랙커를 부착하였다. 기록된 카메라 위치와 방향 정보는 촬영 이미지 상에서의 글레어 위치 변화 분석에 사용되었다. 또한 가상 배경이 실시간 3차원 그래픽으로 표현되는 경우 가상 환경의 투영이 현재 카메라 시점에 부합하도록 정합 하는데 사용된다. 피사체의 정확한 위치 설정을 위해 밀리미터 단위 높이 조절이 가능한 전동 테이블을 사용하였다.

<br/>

> 3. 안티글레어 모니터의 글레어 제거

Figure 2의 왼쪽 그림은 원본 배경 이미지이고 가운데 그림은 안티글레어 모니터에 조명을 비추어 카메라로 촬영한 결과이다. 왼쪽 상단에 글레어 현상이 나타남을 확인할 수 있지만 조명의 모양이 거울처럼 반사되지는 않으며 흐리게 퍼지는 것을 관찰할 수 있다. 이와 같은 글레어 현상 제거를 위해 먼저 원본 배경 이미지를 변형하여 촬영된 이미지 상에 배경 이미지와 정합 시킨다. 다음 두 이미지를 블렌딩 하면서 각 픽셀에 대한 블렌딩 가중치를 루미넌스의 차이에 비례하도록 조정하여글레어 현상이 심한 영역에서는 원본 배경 이미지를 더 많이 사용하도록 하였다. Figure 2의 오른쪽 그림은 이러한 과정을 거친 결과이다. 글레어 현상이 인지하기 어려울 정도로 사라진 것을 볼 수 있다. 반면 안티글레어 필름이 없는 모니터를 대상으로 한 실험에서는 반사되는 조명의 모양이 선명하고 주변 그림과 비연속적이기때문에 동일한 블렌딩을 적용하여도 반사된 형체의 경계 부분에 잔상이 남는 것을 관찰할 수 있었다.

![스크린샷 2024-05-22 234152](https://github.com/Cybecho/KCGS2023-Establishing-an-XR-Studio-with-Anti-Glare-Monitors-Case-Studie/assets/42949995/718abd37-8b96-452b-b5b6-39b1770d4ce9)

<br/>

> 4. 실험

여러 가지 상황에 대한 실험을 수행하여 제시된 방법의 유용성을 검증하였다. Figure 3의 첫번째 행은 화창한 날의 해변을 배경으로 병 맥주 상품 광고를 촬영하는 예로 왼쪽은 촬영 과정이며 오른쪽은 최종 결과이다. 일반적인 크로마키 합성에서 요구되는 후반 작업이 없어도 맥주 병으로 굴절되어 보이는 배경이 표현되는 것을 볼 수 있다. 두번째 행의 왼쪽 그림은 저녁 무렵의 야외 조명을 연출한 것이고 오른쪽 그림은 외부 빛이 차단된 실내에 초록색 비상 등이 켜진 상태를 연출한 것이다. 같은 물리적 장소에서도 가상 환경을 다양하게 교체해가며 촬영할 수 있는 XR 스튜디오의 장점을 확인할수 있다. 세번째 행은 커튼 상품을 촬영하는 예이다. 창밖의 가상 환경이 커튼의 반투명한 재질에 투영되어 표현되는 것을 볼 수 있다. 후반 작업으로도 합성이 쉽지않은 반투명한 재질의 표현이 실시간으로 가능하다는것을 확인할 수 있다.

![스크린샷 2024-05-22 234259](https://github.com/Cybecho/KCGS2023-Establishing-an-XR-Studio-with-Anti-Glare-Monitors-Case-Studie/assets/42949995/5dec9854-a023-4762-82d1-69da85017a42)

<br/>

> 5. 결론

본 연구에서는 안티글레어 모니터를 이용하여 XR 스튜디오를 구성하고 촬영된 이미지에서 글레어 현상을 제거하는 과정을 소개하였다. 실험을 통해 제시된 방법으로 대형 XR 스튜디오의 장점을 유지하는 소형 XR 스튜디오를 구성할 수 있음을 확인하였다.

<br/>

---

## 참고문헌

[1] Kavakli, M. and Cremona, C., The Virtual Production Studio
Concept–An Emerging Game Changer in Filmmaking. In 2022
IEEE Conference on Virtual Reality and 3D User Interfaces
(VR) pp. 29-37, 2022.


[2] Ye, S., Yin, J.L., Chen, B.H., Chen, D. and Wu, Y., October.
Single image glare removal using deep convolutional networks.
In 2020 IEEE International Conference on Image Processing
(ICIP) pp. 201-205, 2020
