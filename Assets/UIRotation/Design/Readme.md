# UI Rotaion 사용법 
## 목적
Screen이 가로 모드 또는 세로 모드일 때 UI의 배치 및 크기가 달라지는 것을 대응하기 위한 모듈입니다.
GameView에서 가로 해상도로 UI 작업을 완료한 후 저장을 하고 마찬가지로 세로 해상도에서 UI 작업을 완료한 후 저장한 다음에
화면이 회전이 되면 각 해상도에 맞게 불러오는 작업을 수행합니다.

## 사전 준비
- 빈 오브젝트에 `ComponentsManager` 스크립트 부착

## 저장
### 정적인 UI 데이터 저장
1. Target이 될 Canvas에 `ComponentProperty` 스크립트 부착
2. 가로 또는 세로 해상도에서 UI 화면 작업 진행
3. ComponentProperty의 컴포넌트 메뉴에서 `SaveStatic` 버튼 클릭(또는 `shift + s` 단축키 입력)
4. Assets/Resources/JsonData/{Orientation}/{SceneName}/{CanvasName} 경로에 저장 완료
### 런타임 중 생성되는 UI(Prefab UI) 저장
1. Prefab 수정 화면에 진입 후 최상단 오브젝트에 `ComponentProperty`를 부착
2. 가로 또는 세로 해상도에서 UI 화면 작업 진행
3. ComponentProperty의 컴포넌트 메뉴에서 `SaveDynamic` 버튼 클릭
4. Assets/Resources/JsonData/{Orientation}/{SceneName}/{CanvasName} 경로에 저장 완료

## 불러오기
### 에디터 모드에서 불러오기
1. 가로 또는 세로 해상도로 변경
2. `ComponentsManager` 스크립트가 부착된 오브젝트를 하이어라키 창에서 클릭 후 'shift + l` 단축키 입력
### 플레이 모드 중 불러오기
1. 플레이 버튼 클릭
2. 해상도를 바꾸면 자동으로 해당 해상도로 작업했던 UI 화면이 불러와 짐