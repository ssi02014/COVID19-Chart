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
2. 명시적인 `any` 선언하기
   - `tsconfig.json`파일에 `noImplicitAny`값을 `true`로 추가
   - 가능한 구체적인 타입으로 타입 정의
3. 프로젝트 환경 구성
   - babel, eslint, prettier 등의 환경 설정
4. 외부 라이브러리 모듈화
   - 외부 라이브러리 `npm i`로 설치

<br />

## 👨🏻‍💻 자바스크립트 프로젝트에 타입스크립트 적용 절차

1. 타입스크립트 환경 설정 및 ts 파일로 변환
2. any 타입 선언
3. any 타입을 더 적절한 타입으로 변경

### 🏃 1. 타입스크립트 프로젝트 환경 구성

- 프로젝트 생성 후 NPM 초기화 명령어로 `package.json` 생성
- 프로젝트 폴더에서 `npm i typescript -D`로 타입스크립트 라이브러리 설치
- 타입스크립트 설정 파일 `tsconfig.json`을 생성하고 기본 값을 추가

```
  npm i typescript -D //타입스크립트 다운로드
  npm init -y //package.json 생성
  tsc --init  //tsconfig.json 생성
```

<br />

```json
{
  "compilerOptions": {
    "allowJs": true,
    "target": "ES5",
    "outDir": "./dist",
    "moduleResolution": "Node",
    "lib": ["ES2015", "DOM", "DOM.Iterable"]
  },
  "include": ["./src/**/*"],
  "exclude": ["node_modules", "dist"]
}
```

- 서비스 코드가 포함된 자바스크립트 파일을 타입스크립트 파일로 변환한다.
- 타입스크립트 컴파일 명령어 tsc로 타입스크립트 파일을 자바스크립트 파일로 변환한다.

<br />

### 🏃 2. 엄격하지 않은 타입 환경(loose type)에서 프로젝트 돌려보기

- 프로젝트에 테스트 코드가 있다면 테스트 코드가 통과하는지 먼저 확인합니다.
- 프로젝트의 js 파일을 모두 ts 파일로 변경합니다.
- 타입스크립트 컴파일 에러가 나는 것 위주로만 먼저 에러가 나지 않게 수정합니다.
  - 여기서, **기능을 사소하게라도 변경하지 않도록 주의합니다.**
- 테스트 코드가 성공하는지 확인합니다

<br />

### 🏃 3. 명시적인 any 선언하기

- 프로젝트 테스트 코드가 통과하는지 확인합니다
- 타입스크립트 설정 파일에 `noImplicitAny: true`를 추가합니다.
- 가능한 타입을 적용할 수 있는 모든 곳에 타입을 적용합니다.
  - 라이브러리를 쓰는 경우 [DefinitelyTyped](https://definitelytyped.org/)에서 `@types 관련 라이브러리`를 찾아 설치합니다.
  - 만약, 타입을 정하기 어려운 곳이 있으면 명시적으로라도 `any`를 선언합니다.
- 테스트 코드가 통과하는지 확인합니다.

<br />

### 🏃 4. strict 모드 설정하기

- 타입스크립트 설정 파일에 아래 설정을 추가한다.

```json
{
  "strict": true,
  "strictNullChecks": true,
  "strictFunctionTypes": true,
  "strictBindCallApply": true,
  "strictPropertyInitialization": true,
  "noImplicitThis": true,
  "alwaysStrict": true
}
```

- `any`로 되어 있는 타입을 최대한 더 적절한 타입으로 변환한다.
- `as`와 같은 키워드를 최대한 사용하지 않도록 고민해서 변경한다.

<br />

## 🔍 모듈화 진행을 위한 프로젝트 환경 구성

- [프로젝트 환경 구성]()

<br />

## 📃 참고 자료

- [존스 홉킨스 코로나 현황](https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6)
- [Postman API](https://documenter.getpostman.com/view/10808728/SzS8rjbc?version=latest#27454960-ea1c-4b91-a0b6-0468bb4e6712)
- [Type Vue without Typescript](https://blog.usejournal.com/type-vue-without-typescript-b2b49210f0b)

<br />
