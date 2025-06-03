# 양중창

> iOS Developer

- **Email**: didwndckd@gmail.com
- **Phone**: 010-3334-9929
- **GitHub**: https://github.com/didwndckd

## 소개

현재 크몽에서 iOS 개발자로 근무하며 크몽앱 개발 및 유지 보수를 진행하고 있습니다.

기본을 중요하게 생각하고 개발에 정성을 들이는 것을 좋아해 생각이 정리되기 전에는 키보드에 손을 올리지 않습니다.

Clean Architecture, MVVM을 사용하여 개발하며 RxSwift, Combine 등을 사용한 리액티브 프로그래밍에 적극적입니다.

요즘은 Swift Concurrency에 관심을 가지고 프로젝트에 적용중에 있습니다.

현재 iOS 팀 내에서 Git을 통해 형상 관리를 하고 있으며 코드 리뷰 후 병합하는 방식으로 진행하고 있습니다.

- 사용 언어: Swift, Objective-C
- 모듈화: Tuist
- 업무 툴: Slack, Jira, Confluence, Figma
- 형상관리: Git, Github, GitLab

## 경력 (5년차)

### (주)크몽

> 2023.07.13 ~ 재직중

프리랜서/아웃소싱 플랫폼

![Kmong_preview](Assets/Kmong_preview.png)

- `Tuist`를 사용한 모듈화 작업환경 구성 및 관리
  - Tuist 설치
  - 빌드 세팅 설정
  - 크몽 앱 디버그 타겟 분리
  - 공통 UI 모듈 분리
- 채팅 개선
  - `UICollectionViewDiffableDataSource` 적용하여 메세지 데이터와 UI 간의 안전한 동기화
  - 메세지 리스트 관리 로직 개선
  - 채팅 화면에서의 **비정상 종료 0건**으로 개선
- 화면 이동 관리를 위한 Router 모듈 구현
  - 화면 이동 로직, 트랜지션 등의 책임 분리
  - 바텀 시트, 툴팁 등을 위한 커스텀 트랜지션 구현
  - 추후 Feature 별 모듈 분리를 위한 선행 작업
- 기존 화면 Clean Architecture, SwiftUI 적용
- 데이터 마이그레이션 관리 모듈 구현
- 캐러셀 뷰 구현
  - `UICollectionView`를 이용하여 구현

  - 호출자가 원하는 사이즈, 여백을 조정하여 사용할 수 있도록 구현

  - 오토 스크롤 구현

- 일정 관리 기능 작업
  - FSCalendar의 `FSCalendarCell` 서브 클래싱으로 달력 UI 커스텀
  - 캘린더 주/월 단위로 볼 수 있도록 구현

### (주)캐플릭스

> 2020.09.07 ~ 2023.06.30

#### 모자이카

원하는 곳에서 렌터카를 픽업하고 반납할 수 있는 렌터카 서비스

![Mosaicar_preview](Assets/Mosaicar_preview.png)

- 앱 리뉴얼
  
  - 앱 전체 리뉴얼 작업으로 기획 단계부터 참여하여 모든 화면의 UI와 기능 개선
  
  - Lottie를 사용한 애니메이션 구현
  
  - `UIViewControllerTransitioningDelegate`, `UIViewControllerAnimatedTransitioning`을 사용하여 화면 전환 애니메이션 커스텀
  - FSCalendar의 `FSCalendarCell` 서브 클래싱으로 달력 커스텀 및 렌트 일정 선택 기능 구현
  - OCR SDK를 커스텀 하여 디자인에 맞춰 카드 스캔 기능 구현
  
- MVVM 패턴 적용
  
  - 기존의 VIPER 패턴이 현재 프로젝트와 맞지 않는다고 판단하여 MVVM 패턴으로 리팩터링
  
  - UI와 로직을 좀 더 명확하게 분리하며 가독성과 유지 보수성 향상
  - 개발 속도 향상
  
- 네트워크 통신 모듈 개발

  - Moya를 도입하여 타입 및 케이스별로 명확한 API 관리가 가능하게 함

  - Moya `TargetType` 프로토콜을 채택한 타입과 파싱 할 타입을 전달받아 `Observable<파싱 타입>`을 반환하여 구독할 수 있도록 Request 함수 구현
  - `Observable`을 확장하여 내부 정의 네트워크 에러 타입으로 `onError`를 전달받을 수 있는 `subscribe` 함수 구현

- 로딩 모듈 개발

  - Rx 기반으로 `subscribe`와 `dispose` 횟수를 카운트하여 로딩 여부를 판단하는 클래스 작성
  - 주로 비동기 네트워크 통신 작업에 사용되며 여러 작업을 동시에 진행하더라도 명확한 로딩 시작, 종료 시점을 알 수 있음
  
- `propertyWrapper`를 사용하여 `UserDefaults` 저장 로직 간편화 작업

- 메모리 누수 제거

  - 기존 코드의 화면 이동 방식의 결함으로 모든 화면에 순환 참조가 존재하였으나 분석 후 순환 참조 제거
  - `WKUserContentController` 브릿지 등록 시 전달하는  `WKScriptMessageHandler` 객체를 강한 참조하여 순환 참조 발생
    - 대신 강한 참조 받을 클래스를 정의하고 내부에 `WKScriptMessageHandler` 객체를 받아 약한 참조하여 메모리 누수 제거
    
  



#### 제주패스

항공, 숙박, 렌터카 가격 비교와 예약을 한 번에 할 수 있는 서비스

![JejuPass_preview](Assets/JejuPass_preview.png)

- 웹뷰 브릿지를 통한 네이티브 기능 동작 구현
- 웹뷰 자바스크립트 함수 호출 모델 구현
- 화면 전환 애니메이션 커스텀
  - `UIViewControllerTransitioningDelegate`, `UIViewControllerAnimatedTransitioning`을 사용하여 화면 전환 애니메이션 커스텀을 위한 수퍼 클래스 구현
  - 뷰 컨트롤러의 자체 크기만큼만 올라오는 바텀 시트 컨트롤러 구현
- `SkeletonView`를 사용하여 스켈레톤 로딩 구현
- 로그인 모듈 개발
  - 앱 로그인을 처리하고 관리하는 모듈 개발
  - 아이디 로그인, SNS 간편 로그인(네이버, 카카오, 애플), 생체 인증 로그인 기능 구현
- `Moya.PluginType`을 사용한 네트워크 통신 플러그인 개발
  - API 요청, 응답 로그를 찍는 플러그인 개발
  - API 응답 시 서버에서 갱신된  `AccessToekn`과 `RefreshToken`이 헤더에 들어오게 되면 앱 내의 토큰을 갱신하는 플러그인 개발
- FCM 푸시 처리 모듈 개발
  - fcmToken을 관리 하고 푸시 이벤트를 처리하는 서비스 클래스 구현
  - 알림 수신 여부와 fcmToken 갱신에 따른 서버 토큰 등록 로직 구현
- 다이나믹 링크 처리 모듈 개발
  - 다이나믹 링크로 앱에 진입하게 되면 해당 링크의 데이터를 추출하고 앱 내에서 사용될 데이터로 가공 후 방출하는 서비스 클래스 구현
  - 방출된 데이터를 받아 처리하는 기능 구현
- 사용자 위치 정보 관리 모듈 개발
  - `CoreLocation`을 사용하여 사용자 위치 데이터, 권한 등을 관리하는 매니저 클래스 구현
  - **위치 권한 요청** > **위치 데이터 방출** 순으로 동작하고 `Observable`로 반환하는 함수 구현
- 퀵 액션 처리 모듈 구현
  - 홈 화면에서 `Shortcut Item`이 선택 되었을 때의 이벤트를 처리하는 서비스 클래스 구현
  - `UIApplicationShortcutItem`의 타입을 체크하고 앱 내에서 사용될 데이터로 가공 후 방출
  - 방출된 데이터를 받아 처리하는 기능 구현

- 프로젝트 디자인 패턴에 맞춘 파일 생성 템플릿 작성
  - 화면 모듈의 이름을 넣고 파일을 만들면  `ViewModel`, `ViewController` 클래스를 만들고 기본 코드를 제공하는 템플릿을 작성하여 동료에게 제공



#### 리본 배반차 파트너

당사의 렌터카 영업관리 시스템과 연동되어 배차, 반차를 앱으로 관리할 수 있는 서비스

![RebornCar_preview](Assets/RebornCar_preview.png)

- 다국어 지원 (일본어, 한국어)
- 멀티 타겟으로 한국 버전, 일본 버전 앱을 따로 배포 및 관리
- iPad, iPhone을 지원하는 UI 구현
- 가로 모드, 세로 모드 지원
- 출고할 차량 사진을 찍을 카메라 기능 구현
  - `AVCaptureSession`을 사용하여 카메라 기능 구현
  - `CMMotionManager`의 **가속도계 센서**를 사용하여 사용자의 화면 회전 잠금 여부와 상관없이 **모든 방향으로의 UI 회전**과 **올바른 방향으로 이미지 저장**

- 차량 파손 상태를 저장할 캔버스 기능 구현
  - 사용자의 터치 이벤트를 받아 `CGContext`를 생성하고 라인을 그리거나 지우는 기능 구현




#### 영수증챙겼니??

사내 식대, 법인카드, 개인경비 영수증 이미지를 업로드 하고 관리하는 사내 서비스

![SMTM_preview](Assets/SMTM_preview2.png)

- 다크모드 지원

- `UISearchController`를 사용한 영수증 데이터 검색 기능 구현

- 이미지 업로드 기능 구현

  - `Moya`의 `Multipart`를 사용한 이미지 업로드 구현
  - `Mantis` 라이브러리를 사용하여 이미지 **Crop** 기능 구현
  - 서버에서 받을 수 있는 이미지 용량 제한을 위한 이미지 압축 기능 구현

- 영수증 이미지 뷰어 기능 구현

  - `KingFisher`를 사용한 이미지 다운로드 프로그레스 구현

- 공유 기능 구현

  - `Share Extension`을 사용하여 앨범 등에서 바로 영수증 이미지를 업로드할 수 있도록 구현



### RoboRisen(외주)

> 2021.10.21 ~ 2021.12.29

### 코딩로비

블루투스 연결을 통해 로봇을 제어하며 놀 수 있는 아이들을 위한 코딩 교육 앱

**시연 영상**: https://www.youtube.com/watch?v=2jRoFh67k18

![CodingRoby_preview](Assets/CodingRoby_preview.jpeg)

- RxSwift, MVVM 패턴, 스토리보드 사용
- `CoreBluetooth`를 사용하여 큐브 연결과 데이터 입출력 제어
- 블루투스 데이터 전송 간 `Queue`를 구현하여 데이터를 안전하게 전송할 수 있도록 구현
- 컨트롤러 프로토콜(버튼, 조이스틱, 움직임 등)을 정의하고 로봇 구조체에 필요한 프로토콜들을 채택하여 구현
- 각도 값, 중앙에서 떨어진 정도를 알 수 있는 커스텀 조이스틱 뷰 구현



## 수상 경력

### AngelHack Seoul 2020

> 2020.07.13 ~ 2020.07.19

AngelHack Seoul 2020에 참가하여 코로나와 같은 재난 격리, 도서 산간 거주 등 불가피한 원격 상황에서도 학습 의지 부여와 완주율을 높이는 교육, 학습 솔루션을 주제로 온라인 스터디 앱을 개발하여 우승

**GitHub**: https://github.com/didwndckd/AngelHack2020

**시연 영상**: https://www.youtube.com/watch?v=k_3of0Qic5c

![Fastcampus_preview](Assets/Fastcampus_preview.png)

- 성과: **우승** (상금 160만원)

- 참여 인원: 5명 (iOS 3명, 디자인 2명)

- 기본 강의 재생 화면 구현

  - `AVFoundation`을 사용하여 영상 재생 및 영상 제어 기능 작업

- 스터디 입장 대기 화면 구현

  - 스터디 내용에 대한 설명과 남은 시간을 표시하며 스터디 시작 시간이 지나면 자동으로 스터디 진행 화면으로 이동하도록 구현

- 스터디 강의 재생 화면 구현

  - 스터디 시작점과 현재 시간을 계산해 모든 스터디원이 동시에 같은 강의 구간을 보도록 구현
  - 질문 시점과 동영상 재생 시간 비율을 계산하여 재생바에 핀을 등록하는 질문 등록 기능 구현

- 채팅 기능 구현

  - `UICollectionView`와 `UITableView`를 사용하여 질문별로 다른 채팅 내용을 보여주도록 구현
  - Firebase/Firestore를 사용한 실시간 채팅 기능 구현

- 상장

  <img src="Assets/Angelhack2020.jpeg" style="float: left; width:35%;"/>



## 오픈소스 프로젝트

### JCJoystick

> 2022.04.14 ~ 2022.04.30

게임이나 컨트롤러 등에 사용 가능한 조이스틱 뷰

**GitHub**: https://github.com/didwndckd/JCJoystick

![JCJoystick_preview](Assets/JCJoystick_preview.jpeg) 

- CocoaPods 배포
- 사용자 터치 이벤트를 따라 뷰를 이동시키고 각도값과 중간지점에서 떨어진 정도를 `delegate`를 통해 전달
- 터치 이벤트가 가이드 뷰를 벗어나면 현재 터치 포인트 방향의 외곽 지점으로 위치를 조정하여 부드럽게 움직이는 조이스틱 구현



## 개인 프로젝트

### Netflix Clone

> 2020.03.20 ~ 2020.04.29

패스트 캠퍼스에서 진행한 팀 프로젝트로 Backend 팀과 협업하며 기존 Netflix 앱 서비스를 기반으로 같은 형태의 서비스를 만들어보는 클론 프로젝트

**GitHub**: https://github.com/didwndckd/Netflix_Clone_iOS

**시연 영상**: https://www.youtube.com/watch?v=qguomgFr5IQ

![Netflix_Clone_preview](Assets/Netflix_Clone_preview.png)

- 참여 인원: 6명 (iOS 4명, Backend 2명)
- 담당 작업 내용
  - 영상 재생 기능 구현
  - 콘텐츠 저장 기능 구현
  - 로그인, 회원가입 기능 구현
  - 통신 모듈 작업



## 교육

### 국가평생교육진흥원 학점은행

> 2019.09 ~ 2023.08

- 컴퓨터공학사(4.1/4.5)

### 패스트캠퍼스 iOS 스쿨

> 2019.11 ~ 2020.04

- iOS 개발 과정 수료 및 다수의 프로젝트 진행
