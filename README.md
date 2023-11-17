# 은행 창구 관리 앱

### Table of Content

> **1️⃣ OverView**
>
> - 결과물
> - 프로젝트 참여자
> - 프로젝트 기간
>
> **2️⃣ 프로젝트 구현**
>
> - 프로젝트 설계
> - 사용 기술/구성
> - 태스크 매니지먼트
> - 프로젝트 파일 구조
> - 구현 기능
> - 구현 상세
>
> **3️⃣ 습득 지식**

## 1️⃣ OverView

### 📍 결과물

### 📍 프로젝트 참여자

<table>
<tr>
<th>🧑🏻‍💻 Roks</th>
<th>🐠 Janine</th>

</tr>
<tr>
<td>
<img src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/d90a04e2-29e5-4157-9225-98540c4e7e80" width="90" height="90">
<div>@KimRoks</div>
</td>
<td>
<img src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/71ba2492-82c0-4b45-8565-e542688565d9" width="90" height="90"> 
<div>@janine-kang</div>
</td>
</tr>
</table>

### 📍 프로젝트 기간

> 2023.10.30 ~ 2023.11.17 (3 weeks)

## 2️⃣ 프로젝트 구현

### 📍 프로젝트 설계

- 디자인 패턴: `MVC`

### 📍 사용 기술/구성

- Swift 기반 어플리케이션 작성
- UIKit framework
- AutoLayout
- Grand Central Dispatch
- Git-flow 기반 협업

### 📍 태스크 매니지먼트

- Notion
- Discord

### 📍 프로젝트 파일 구조

```
├── Controllers
│   └── ViewController.swift
├── Info.plist
├── Models
│   ├── Bank.swift
│   ├── UIUpdateDelegate.swift
│   └── WorkTimer.swift
├── Resources
│   ├── AppDelegate.swift
│   ├── Assets.xcassets
│   │   ├── AccentColor.colorset
│   │   │   └── Contents.json
│   │   ├── AppIcon.appiconset
│   │   │   └── Contents.json
│   │   └── Contents.json
│   ├── Base.lproj
│   │   └── LaunchScreen.storyboard
│   └── SceneDelegate.swift
└── Views
    ├── BankView.swift
    ├── ListView.swift
    └── UIText.swift
```

### 📍 기능 구현

#### 메인 화면

<table>
<tr>
<th>구동 화면</th>
<th>구현 기능</th>
</tr>
<tr>
<td>
<div width="523px">
<img width="auto" height="250" alt="Screenshot 2023-11-17 at 4 14 29 PM" src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/0ebe2044-b798-4bdf-bdb8-c579681094e3">
<img width="auto" height="250" alt="Screenshot 2023-11-17 at 4 14 26 PM" src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/d908674f-d8e2-443c-8746-dd7b5609ab55">
</div>
<div width="523px">
<img width="auto" height="250" alt="Screenshot 2023-11-17 at 4 14 04 PM" src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/206959dc-58da-4dd5-8824-cc541749f1ed">
<img width="auto" height="250" alt="Screenshot 2023-11-17 at 4 14 00 PM" src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/45b0371c-67da-49d4-9ab9-78aad79a7a63">
</div>
<div width="523px">
<img width="auto" height="250" alt="Screenshot 2023-11-17 at 4 13 30 PM" src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/339bf990-6086-40a8-9341-45dad2e498e1">
<img width="auto" height="250" alt="Screenshot 2023-11-17 at 4 13 16 PM" src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/acde993e-4c6d-4aad-91c4-caee0019120c">
</div>
</td>
<td>
  <li>코드로 UI 구성</li>
  <li>iPhone/iPad 화면 AutoLayout 호환</li>
  <li>타이머 기능</li>
</td>
</tr>
</table>

#### 고객 10명 추가 버튼 클릭

<table>
<tr>
<th>구동 화면</th>
<th>구현 기능</th>
</tr>
<tr>
<td>
<img src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/c37de1ac-2def-4557-85c4-eb0443fa7a4c" width="auto" height="350" />
</td>
<td>
  <li>버튼 클릭 시 대기열에 고객 추가</li>
  <li>업무 시작 시 타이머 동작</li>
  <li>예금 업무는 동시에 2개, 대출 업무는 동시에 1개 처리</li>
  <li>업무 진행 상태에 따라 Label 이동</li>
  <li>모든 업무 종료 시 타이머 정지</li>
</td>
</tr>
</table>

#### 고객 10명 추가 버튼 중첩 클릭

<table>
<tr>
<th>구동 화면</th>
<th>구현 기능</th>
</tr>
<tr>
<td>
<img src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/9c6deccf-ca2c-4319-97a6-9a66ad8d3d35" width="auto" height="350" />
</td>
<td>
  <li>화면 스크롤 지원</li>
  <li>순차적인 고객 대기 번호 부여</li>
  <li>이전 업무 종료 후 고객 추가 버틐 클릭 시 기존 상황에서 업무 재개</li>
</td>
</tr>
</table>

#### 초기화 버튼 클릭

<table>
<tr>
<th>구동 화면</th>
<th>구현 기능</th>
</tr>
<tr>
<td>
<img src="https://github.com/KimRoks/ios-bank-manager/assets/76927263/3009bec7-bc08-4f8b-a671-4f6b25b2da86" width="auto" height="350" />
</td>
<td>
  <li>타이머 초기화</li>
  <li>대기중 업무 취소</li>
  <li>대기 번호 초기화</li>
</td>
</tr>
</table>

### 📍 구현 상세

- `Xcode 프로젝트 관리 구조`를 활용하여 ConsoleApp과 UIApp 두 가지 어플리케이션 내 파일 공유
- Scrolling과 Timer 동시 수행을 위해 `Runloop` 조정
- `OperationQueue` 활용하여 동시성 프로그램 구현
- Race Condition 방지를 위한 `DispatchSemaphore` 활용(Thread-safe)
- 스토리보드 사용하지 않고 `코드로 UI` 작성
- 재사용과 유지 보수를 고려하여 `Type Extension ` 작성(소수점 절삭, 타이머 단위 설정, UILabel convenience init 등)
- `SOLID 법칙`에 입각하여 `LinkedList`를 활용한 `Queue` 구조 구현
- `Protocol`의 기본 구현을 활용하여 코드의 재사용성을 높이고 객체 간 의존성 감소
- `디미터 법칙 준수`를 위한 UI Update Methods 정의

## 3️⃣ 습득 지식

<table>
<tr>
<th>🧑🏻‍💻 Roks</th>
<th>🐠 Janine</th>
</tr>
<tr>
<td>
<li>객체 지향 프로그래밍</li>
<li>동시성 프로그래밍</li>
<li>Type Extension 활용하여 재사용성 고려</li>
<li>RunLoop</li>
<li>코드 UI를 통한 AutoLayout 작성(ScrollView, StackView, CHCR 등)</li>
</td>
<td>
<li>DispatchQueue와 Operation</li>
<li>DispatchSemaphore 개념 및 활용</li>
<li>Main Queue에 대한 이해와 활용</li>
<li>디미터 법칙</li>
<li>SOLID 법칙</li>
</td>
</tr>
</table>
