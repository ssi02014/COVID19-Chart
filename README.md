# 💻 COVID19-Chart

### 자바스크립트로 작성 된 COVID19-Chart📈를 TypeScript로 점진적 적용 프로젝트

<br />

## 🖐 자바스크립트 코드에 타입스크립트를 적용할 때 주의해야 할 점

- 기능적인 변경은 절대 하지 않을 것
- 테스트 커버리지가 낮을 땐 함부로 타입스크립트를 적용하지 않을 것
- 처음부터 타입을 엄격하게 적용하지 않을 것 (점진적으로 strict 레벨을 증가)

<br />

## 📖 자바스크립트 프로젝트에 타입스크립트 적용하기

0. 자바스크립트 파일에 JSDoc으로 타입 시스텝 입히기
1. 타입스크립트 기본 환경 구성
   - [x] NPM 초기화
   - [x] 타입스크립트 라이브러리 설치
   - [x] 타입스크립트 설정 파일 생성 및 기본 값 추가
   - [x] 자바스크립트 파일을 타입스크립트 파일로 변환
   - [x] `tsc` 명령어로 타입스크립트 변환

```
  npm i typescript //타입스크립트 다운로드
  npm init -y //package.json 생성
  tsc --init  //tsconfig.json 생성
```

<br />

## 📃 참고 자료

- [존스 홉킨스 코로나 현황](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6)
- [Postman API](https://documenter.getpostman.com/view/10808728/SzS8rjbc?version=latest#27454960-ea1c-4b91-a0b6-0468bb4e6712)
- [Type Vue without Typescript](https://blog.usejournal.com/type-vue-without-typescript-b2b49210f0b)

<br />

## 👨🏻‍💻

### 🏃
