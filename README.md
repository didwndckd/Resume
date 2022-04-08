# 양중창

> iOS Developer

- **Email**: didwndckd@gmail.com
- **Phone**: 010-3334-9929
- **GitHub**: https://github.com/JoongChangYang

## 소개

2년 차 개발자로 현재 캐플릭스에서 iOS 개발자로 근무하며 렌터카 서비스인 모자이카 앱 외 여러 서비스를 개발 및 유지 보수를 진행하고 있습니다.

기본을 중요하게 생각하고 개발에 정성을 들이는 것을 좋아해 생각이 정리되기 전에는 키보드에 손을 올리지 않는 편입니다.

RxSwift와 MVVM 패턴을 사용하여 개발하며 코드 베이스와 스토리보드 두 가지 방법으로 UI 구현이 가능합니다. 현재 iOS 개발자 동료와 Git/GitLab을 통해 형상관리를 하고 있으며 코드 리뷰 후 Merge 하는 방식으로 진행하고 있습니다.

## 기술

- 사용 언어: Swift, Obhective-C
- 주요 사용 라이브러리: RxSwift, RxCocoa, SnapKit, Moya, Alamofirem, Kingfisher
- 기타: Git/Github

## 경력

### (주)캐플릭스

> 2020.09.07 ~ 현재

#### 모자이카

원하는곳에서 렌터카를 픽업하고 반납할 수 있는 렌터카 서비스

[<img src="Assets/icon_app_store_download.png" style=" height: 50px;"/>](https://apps.apple.com/kr/app/%EB%AA%A8%EC%9E%90%EC%9D%B4%EC%B9%B4-%EB%8B%A8%EA%B8%B0%EB%A0%8C%ED%8A%B8%EC%B9%B4-%EC%9E%A5%EA%B8%B0%EB%A0%8C%ED%84%B0%EC%B9%B4-%EC%9E%90%EB%8F%99%EC%B0%A8-%EA%B5%AC%EB%8F%85/id1529825302)

- 앱 리뉴얼
  
  - 앱 전체 리뉴얼 작업으로 기획 단계부터 참여하여 모든 화면의 UI와 기능 개선
  
  - `UIViewControllerTransitioningDelegate`, `UIViewControllerAnimatedTransitioning`을 사용하여 화면 전환 애니메이션 커스텀
  - FSCalendar의 `FSCalendarCell` 서브 클래싱으로 달력 커스텀 및 렌트 일정 선택 기능 구현
  - OCR SDK를 커스텀하여 디자인에 맞춰 카드 스캔 기능 구현
  - RxSwift의  `flatMapLatest`를 사용하여 주소 검색 자동완성 기능 구현
  - RxSwift의 `combineLatest`를 사용하여 차량 필터 멀티 선택 기능 구현
  
- MVVM 패턴 적용
  
  - 기존의 VIPER 패턴이 현재 프로젝트와 맞지않는다고 판단하여 MVVM 패턴으로 리팩터링
  
  - UI와 로직을 좀더 명확하게 분리하며 가독성과 유지 보수성 향상
  - 개발 속도 향상
  
- 네트워크 통신 모듈 작업

  - Moya를 도입하여 타입 및 케이스별로 명확한 API관리가 가능하게 함

  - Moya `TargetType` 프로토콜을 채택한 타입과 파싱할 타입을 전달받아 `Observable<파싱타입>`을 반환 하여 구독할 수 있도록 Request 함수 구현
  - `Observable`을 확장하여 내부 정의 네트워크 에러 타입으로 `onError`를 전달받을 수 있는 `subscribe` 함수 구현

- 메모리 누수 제거

  - 기존 코드의 화면 이동 방식의 결함으로 모든 화면에 순환 참조가 존재하였으나 분석 후 순환 참조 제거


#### 기타

- 제주패스 렌트 iOS 앱 유지보수
- 카페패스 iOS 앱 유지보수
- 제주패스 맛집 iOS 앱 유지보수

## 수상 경력

### AngelHack Seoul 2020 우승

> 2020.07.13 ~ 2020.07.19

<img src="Assets/Angelhack2020.jpeg" style="float: left; width:35%;"/>

AngelHack Seoul 2020에 참가하여 코로나와 같은 재난 격리, 도서 산간 거주 등 불가피한 원격 상황에서도 학습 의지 부여와 완주율을 높이는 교육, 학습 솔루션을 주제로 온라인 스터디 앱을 개발하여 우승하였습니다.

- 참여 인원: 5명 (iOS 3명, 디자인 2명)

- 링크

  [<img src="Assets/icon_youtube.png" width=70px/>](https://www.youtube.com/watch?v=XIDqwjuPcsk)&nbsp;&nbsp;&nbsp;&nbsp;[<img src="Assets/icon_github.png" width=60px/>](https://github.com/JoongChangYang/AngelHack2020)


## 개인 프로젝트

## 교육

## 이미지 저작권

- <a href="https://www.flaticon.com/free-icons/youtube" title="youtube icons">Youtube icons created by Freepik - Flaticon</a>

- <a href="https://www.flaticon.com/kr/free-icons/github" title="github 아이콘">Github 아이콘  제작자: riajulislam - Flaticon</a>

