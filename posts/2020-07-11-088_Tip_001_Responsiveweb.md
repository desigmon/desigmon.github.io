---
layout: article

title: 디자이너들을 위한 반응형 구분 변수
excerpt: CSS3 Media Query for Responsive Web

tags: 
- Tech
- Development

article_header:
  type: cover
  image:
    src: /img/088/00.jpg


description: 
- CSS3 미디어쿼리
- CSS3 Media Query

author: derano
show_edit_on_github: false
toc: true

--- 
# 조건문이 될 수 있는 특징들
## width / height
뷰포트의 너비와 높이. 뷰포트의 크기는 HTML body 콘텐츠를 표시하는 영역으로 실제 스크린의 크기와는 다르다. 반응형 웹 구현시 가장 일반적으로 사용하는 조건이 된다.
- Value: <length>
- Applies to: visual and tactile media types
- Accepts min/max prefixes: yes
  
\{% Example %}
@media all and (min-width:768px) and (max-width:1024px) { … } // 뷰포트 너비가 768px 이상 '그리고' 1024px 이하이면 실행
@media all and (width:768px), (width:1024px) { … } // 뷰포트 너비가 768px 이거나 '또는' 1024px 이면 실행
@media not all and (min-width:768px) and (max-width:1024px) { … } // 뷰포트 너비가 768px 이상 '그리고' 1024px 이하가 '아니면' 실행
\{% Example %}
  
## device-width / device-height
스크린의 너비와 높이. 스크린은 출력 장치가 픽셀을 표시할 수 있는 모든 영역으로 일반적으로 HTML body 콘텐츠를 표시하는 뷰포트 보다 크다.
- Value: <length>
- Applies to: visual and tactile media types
- Accepts min/max prefixes: yes
  
\{% Example %}
@media all and (device-width:320px) and (device-height:480px) { … } // 스크린 너비가 320px '그리고' 높이가 480px 이면 실행
@media all and (min-device-width:320px) and (min-device-height:480px) { … } // 스크린 너비가 최소 320px 이상 '그리고' 높이가 최소 480px 이상이면 실행
\{% Example %}
  
## orientation
뷰포트의 너비와 높이 비율을 이용하여 세로 모드인지 가로 모드인지를 판단한다.
- Value: portrait | landscape
- Applies to: bitmap media types
- Accepts min/max prefixes: no

\{% Example %}
@media all and (orientation:portrait) { … } // 세로 모드. 뷰포트의 높이가 너비에 비해 상대적으로 크면 실행
@media all and (orientation:landscape) { … } // 가로 모드. 뷰포트의 너비가 높이에 비해 상대적으로 크면 실행
\{% Example %}

## aspect-ratio
뷰포트의 너비와 높이에 대한 비율. ‘너비/높이’ 순으로 조건을 작성한다. min/max 접두사를 사용하면 너비 값의 최소/최대 비율을 정할 수 있다.
- Value: <ratio>
- Applies to: bitmat media types
- Accepts min/max prefixes: yes
  
\{% Example %}
@media all and (aspect-ratio:5/4) { … } // 뷰포트 너비가 5, 높이가 4 비율이면 실행
@media all and (min-aspect-ratio:5/4) { … } // 뷰포트 너비가 5/4 비율 이상이면 실행
@media all and (max-aspect-ratio:5/4) { … } // 뷰포트 너비가 5/4 비율 이하면 실행
\{% Example %}
  
## device-aspect-ratio
스크린의 너비와 높이에 대한 비율. ‘너비/높이’ 순으로 조건을 작성한다. min/max 접두사를 사용하면 너비 값의 최소/대최 비율을 정할 수 있다.
- Value: <ratio>
- Applies to: bitmap media types
- Accepts min/max prefixes: yes
  
\{% Example %}
@media all and (device-aspect-ratio:5/4) { … } // 스크린 너비가 5, 높이가 4 비율이면 실행
@media all and (min-device-aspect-ratio:5/4) { … } // 스크린 너비가 5/4 비율 이상이면 실행
@media all and (max-device-aspect-ratio:5/4) { … } // 스크린 너비가 5/4 비율 이하면 실행
\{% Example %}
  
## color
출력 장치의 색상에 대한 비트 수. 출력 장치가 컬러가 아닌 경우 0의 값에 대응한다.
- Value: <integer>
- Applies to: visual media types
- Accepts min/max prefixes: yes
  
\{% Example %}
@media all and (color) { … } // 출력 장치가 컬러를 지원하면 실행
@media all and (color:0) { … } // 출력 장치가 컬러가 아니면 실행
@media all and (color:8) { … } // 출력 장치가 8비트 색상이면 실행
@media all and (min-color:8) { … } // 출력 장치가 8비트 이상 색상이면 실행
@media all and (max-color:8) { … } // 출력 장치가 8비트 이하 색상이면 실행
\{% Example %}
  
## color-index
출력 장치가 색상 색인 테이블을 사용하는 경우 표현할 수 있는 색의 수. 출력 장치가 색상 색인 테이블을 사용하지 않으면 0의 값에 대응한다. 현재 제대로 지원하는 브라우저가 없다.
- Value: <integer>
- Applies to: visual media types
- Accepts min/max prefixes: yes
  
\{% Example %}
@media all and (color-index) { … } // 출력 장치가 색상 색인 테이블을 사용하면 실행
@media all and (color-index:0) { … } // 출력 장치가 색상 색인 테이블을 사용하지 않으면 실행
@media all and (color-index:256) { … } // 출력 장치가 256 색을 지원하면 실행
@media all and (min-color-index:256) { … } // 출력 장치가 256 이상 색을 지원하면 실행
@media all and (max-color-index:256) { … } // 출력 장치가 256 이하 색을 지원하면 실행
\{% Example %}
  
## monochrome
출력 장치가 흑백인 경우 픽셀당 비트 수. 출력 장치가 흑백이 아니라면 0의 값에 대응한다.
- Value: <integer>
- Applies to: visual media types
- Accepts min/max prefixes: yes
  
\{% Example %}
@media all and (monochrome) { … } // 출력 장치가 흑백이면 실행
@media all and (monochrome:0) { … } // 출력 장치가 흑백이 아니면 실행
@media all and (min-monochrome:2) { … } // 출력 장치가 흑백이고 2비트 이상이면 실행
@media all and (max-monochrome:2) { … } // 출력 장치가 흑백이고 2비트 이하이면 실행
\{% Example %}

## resolution
출력 장치의 해상력에 대응한다. min/max 접두사는 사각형 아닌 픽셀(인쇄 장치)에도 대응하지만 접두사 없는 resolution 조건은 사각형 픽셀에만 대응한다. 조건의 값으로 dpi와 dpcm 단위를 사용할 수 있다.
- Value: <resolution>
- Applies to: bitmap media types
- Accepts min/max prefixes: yes
  
\{% Example %}
@media all and (resolution:96dpi) { … } // 1인치당 96개의 사각형 화소를 제공하면 실행
@media all and (min-resolution:96dpi) { … } // 1인치당 96개 이상의 화소를 제공하면 실행
@media all and (max-resolution:96dpi) { … } // 1인치당 96개 이하의 화소를 제공하면 실행
\{% Example %}
  
## scan
TV의 스캔 방식에 따라 대응한다. progressive 값은 초당 60회 수준의 고화질 스캔에 대응하고 interlace 값은 초당 30회 수준의 일반 스캔에 대응한다. 대부분의 HDTV는 progressive와 interlace 방식을 모두 지원하고 있다.
- Value: progressive | interlace
- Applies to: “tv” media types
- Accepts min/max prefixes: no
  
\{% Example %}
@media tv and (scan:progressive) { … } // 초당 60회 수준의 고화질 스캔 방식 TV에 대응한다
@media tv and (scan:interlace) { … } // 초당 30회 수준의 일반 스캔 방식 TV에 대응한다
\{% Example %}
  
## grid
출력 장치가 그리드 방식이면 대응한다. 그리드 방식은 타자기와 같이 고정된 글꼴만 사용하는 장치이다. 통상 출력 장치는 비트맵이 아니면 그리드 방식이다. 값은 정수 0과 1 뿐이고 0의 값은 비트맵 방식에 대응한다.
- Value: <integer> 0 | 1
- Applies to: visual and tactile media types
- Accepts min/max prefixes: no
  
\{% Example %}
@media all and (grid) { … } // 출력 장치가 그리드 방식이면 실행
@media all and (grid:0) { … } // 출력 장치가 그리드 방식이 아니면 실행
@media all and (grid:1) { … } // 출력 장치가 그리드 방식이면 실행
\{% Example %}
  


출처
- https://naradesign.github.io/article/media-query.html