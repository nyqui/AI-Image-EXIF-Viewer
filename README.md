# AI-Image-EXIF-Viewer
https://greasyfork.org/ko/scripts/464214

## 이곳은 개발중인 장소입니다.
 코드가 안정화되지 않았을 수 있으며, main에 merge 및 Greasy Fork로 release되기 전 언제던 변경될 수 있습니다.
 
## TODO:
 1. 메타데이터 없는 이미지 팝업에서 Image Open 하면 팝업도 동시에 닫히도록?
 1. 드래그 + 드롭한, 메타데이터 없는 이미지도 분석이 어떻게 가능하지 않을까? deepdanbooru는 될 거로 보였었는데 며칠째 503 뜨면서 열리질 않아서 확인 못함
 
## Version changes
### 1.10.2 2023-04-21 07:09

 1. 토스트형 알림 지속시간 일괄적으로 변경 및 3초로 변경
 1. 드래그 + 드롭으로 분석한 파일에서 메타데이터를 찾지 못했을 때 토스트형 알림을 띄우도록 변경
 1. 그 외 코드 일부 클린업

### 1.10.1 2023-04-21 04:13

 1. 버튼 색깔 일관성 패치
     - 옵션1: #5cc964
     - 옵션2: #ff9d0b
     - 닫기: #b41b29
 1. 드래그 + 드롭으로 분석한 파일에서 메타데이터를 찾지 못했을 때의 루틴 분리
 1. infer에 Tiled Diffusion 인식 추가

### 1.10.0 2023-04-20 02:49
 
 1. infer에 LyCORIS 인식 추가
 1. "메타데이터 요약" 창에서 "이미지 열기", "이미지 저장" 기능 버튼화

### 1.9.6 2023-04-17 22:35

 1. "메타데이터 요약" 창과 "메타데이터 없음" 창에 버전, Greasy Fork 링크, GitHub 링크 추가 (엔드유저의 버전 확인 용이성 확보) 
 1. WD 1.4 Tagger 로딩시에도 DeepDanbooru와 같게 loader(바람개비) 나오도록 수정
 1. 글 수정시에도 글 작성시처럼 인식되도록 수정함.
    - 이제 해당 채널에서 글 수정시에도 이미지 업로드 창에 "Exif 데이터 보존" 체크박스가 기본값으로 체크됨
    - 글 수정시에도 창에 드래그 + 드롭 식으로 이미지를 업로드할 수 있음
        - (그러나 **드래그 + 드롭으로 업로드시 체크박스 값에 관계 없이 EXIF를 보존하지 않으므로** 참고)

### 1.9.5 (initial release) 2023-04-17 17:46

 1. arca.live 이미지 링크 expiry 관련 토큰 추가로 인한 기능 불량 수정
 1. Denoising strength 표시 및 Image Open | Save 위치 변경
 1. infer에 DINO, LLuL, Cutoff 인식 추가
 
 
 
## Original script 
by shounksu:  
 https://greasyfork.org/ko/scripts/452822
