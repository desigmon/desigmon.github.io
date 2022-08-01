---
layout: article

title: 관계 모형
excerpt: 서비스의 그림을 그리는 7개의 방법

tags: 
  - UX/UI

article_header:
  type: cover
  image:
    src: /img/017/00.jpg


description: 
  - UX 개발
  - 관계모형
  - Relation Model

author: derano
show_edit_on_github: false
toc: true

---
# Summary
보이지 않는 것은 보여주고, 구체적으로 서비스를 그리기 위한 단계  
관계 모형이 필요한 이유는 공통된 서비스에 대한 구조를 가지고 작업할 수 있게끔 한다.
  
# Contents
## 관계 모형(Relation Model)
**데이터에 형성된 상호 관계를 시각화한 것**이다. 사람과 환경, 사람과 환경, 사람과 디바이스, 사람과 사람 등 관계 속에서 찾을 수 있는 데이터를 시각화하는 것이다.  
관계를 찾아내는 것 자체도 중요하지만 연결 고리 속에 숨어있는 의미를 발견하는 것이 중요하다. 단순히 화살표 찍찍 그어서 연결하는 것에서 끝나는 것이 아니라 그 연결점 속에 숨겨진 의미를 끌어내어 적절하게 표현하는 것이 중요하다.

### Stakeholder Map
![Stakeholder Map](/img/017/01.jpg "Stakeholder Map")
서비스 이해 관계자들이 관계를 시각화한 지도, 그림이다.
- 사용자
- 서비스 제공자
- 기획자
- 디자이너
- 개발자
프로젝트에서 산정할 수 있는 이해 관계자들을 찾고 비즈니스 구조를 그려보기 위한 도구로 사용할 수 있다.
  
### System Map
![System Map](/img/017/02.jpg "System Map")
구성원간의 협업 정도 및 관계도를 파악하는 도구로 제공하고자 하는 시스템의 기술적인 연결을 설명하기 위한 시각적 설명이며, 시스템에 포함된 각각 다른 행위자와 자금의 연결, 재화, 에너지, 정보, 자금의 흐름 등 표현 가능

### Cultural Model
![Cultural Model](/img/017/03.jpg "Cultural Model")
Cultural Model은 업무를 수행하는 사람을 둘러싼 외부적 영향 또는 내부의 문화적인 관계를 시각화한 것이다. Cultural Model은 조직 또는 지역적 위치 내에 존재하는 문화적 이슈, 사용되는 도구, 사람들의 감정 관계, 숨겨진 니즈 등 관찰된 내용을 문화 관계 중심으로 맵핑해주는 것이 중요하다.


### Touch Point Matrix
![Touch Point Matrix](/img/017/04.jpg "Touch Point Matrix")
사용자들이 서비스를 이용하면서 접하게 되는 Touch Point를 시각화하는 것이다. 서비스 제공 방식이나 새로운 서비스 기회 영역에 대한 아이디어를 얻기 위해 활용할 수 있다. 서비스와 사용자, 이해 관계자의 연결 구조를 파악하고 다양한 유형의 접촉점을 정의하는 것이 중요하다.

### Use Case Diagram
![Use Case Diagram](/img/017/05.jpg "Use Case Diagram")
Use Case Diagram은 사용 Scene에 대한 과정을 한눈에 볼 수 있게 시각화한 Diagram을 말힌다. 특별히 정형화된 형태는 없으며 서비스/제품 사용 시작 시점부터 종료 시점까지 '누가', '무엇'을 할 수 있는지에 대해 상세하게 기술해놓은 시나리오다.

### Actors Map
![Actors Map](/img/017/06.jpg "Actors Map")
Actors Map은 사용자와 서비스/이해 관계자 간의 위치 관계와 역할을 정의하기 위한 도구이다. 형태적으로는 Stakeholder Map하고 유사한 형태를 가지고 있으나 내용적으로는 조금 다른 구조를 가지고 있다. Stakeholder Map이 비즈니스적인 측면에서 이해 관계자들의 관계를 고려한 맵이라고 하면 Actors Map은 사용자 중심으로 사용자와 서비스의 연결 구조를 그려낸 냅이다. 사용자와 서비스가 어떠한 연결 구조를 가지고 있는지 정의함으로써 새로운 서비스 기획시 고려해야 하는 전달 경로나 Touch Point들을 찾을 수 있다.

### Value Web Diagram
![Value Web Diagram](/img/017/07.jpg "Value Web Diagram")
시장이나 산업에서의 현재 혹은 잠재적인 구조와 가치의 흐름을 설명하는 방법이다. 각 요소 간에 교환되는 가치를 알려주고 이러한 가치 사슬에서 집중해야 할 부분을 명확하게 찾아내는 것이 중요합니다. 돈, 정보, 서비스, 제품 흐름의 관계를 한눈에 볼 수 있게 시각화하는 방식이다.

----
## 이미지 출처
- https://dribbble.com/shots/4417208-Stakeholder-map-for-scaled-Agile-02
- https://images.squarespace-cdn.com/content/57ec7e58cd0f683aa71b7f16/1516774298104-9LKMPNY479B8JBCISP10/Mother+Together-07.png?format=1000w&content-type=image%2Fpng
- https://www.interaction-design.org/literature/book/the-encyclopedia-of-human-computer-interaction-2nd-ed/contextual-design
- https://blendinmedia.wordpress.com/design-assignment/conceptual-design/highlights-concept/components-touchpoint-matrix/
- https://blendinmedia.wordpress.com/design-assignment/conceptual-design/highlights-concept/components-touchpoint-matrix/
- https://stackoverflow.com/questions/6829062/help-deciding-on-use-case-diagram-parts
- http://servicedesigntools.org/sites/default/files/res_images/58299511_2bcff18db2_b.jpg
- https://dribbble.com/shots/3294450-UX-Flow-Diagram