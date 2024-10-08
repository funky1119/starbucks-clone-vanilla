# starbucks-clone-vanilla

참고
https://priceless-bhabha-83fc0d.netlify.app/

## CDN

- reset-css
- GOOGLE FONT
- MATERIAL ICONS
- LODASH
- GSAP & SCROLL TO PLUGIN
- SWIPER
- SCROLL MASIC

`-----------------------------------------------------------`

# HTML/CSS/JS

## 질문

HTML Doctype 선언의 의미와 역할을 설명해 주세요.

## 답변

HTML Doctype 선언은 HTML 문서가 웹 브라우저에 의해 어떤 방식으로 해석되어야 하는지 알려주는 역할을 하기 때문에, Doctype 선언은 HTML 문서(파일)의 첫 줄에 위치합니다.
`<!DOCTYPE html>` 태그는 HTML 문서가 HTML5 표준으로 작성되어 있고 웹 브라우저가 그에 맞게 해석해야 한다는 것을 명시하는 것입니다.
대표적인 HTML5 표준의 특징 중 하나로 빈 태그(Empty)를 닫는 `/` 기호 사용이 필수가 아닌 선택적이라는 것이 있고, `<header>`.`<main>`,`<footer>`,`<nav>` 같은 새로운 시멘틱 요소들이 추가되어 사용할 수 있다는 것이 있습니다.

———————————————————————————————————————————————————

## 질문

CSS 선택자 우선순위의 개념과 계산 방법을 설명해 주세요.

## 답변

CSS 선택자 우선순위는 하나의 요소에 여러 스타일이 적용될 때, 어떤 스타일이 최종적으로 적용될지 결정하는 개념입니다.
우선순위가 가장 높은 것은 CS 속성에서 직접 사용하는 `!important` 키워드고, 다음으로 HTML `style` 속성에서 선언하는 인라인 스타일이 있습니다.
그리고 아이디 선택자(`#id`), 클래스 선택자(`.class`), 태그 선택자(`tag`), 전체 선택자(`*`), 스타일 상속 등의 순서로 점수가 매겨지고 계산되어 순위가 결정됩니다.
각 점수는 인라인 스타일이 1000점, 아이디 선택자는 0100점, 클래스 선택자는 0010점, 태그 선택자는 0001점이며, 전체 선택자는 0000점, 상속은 점수가 없습니다.
만약 구글 크롬 브라우저 기준 99버전부터 지원하는 CSS `@layer` 규칙을 사용하면, 스타일 우선순위를 의도적으로 조정할 수 있습니다.

———————————————————————————————————————————————————

## 질문

브라우저 기본 스타일의 초기화(Reset)와 표준화(Normalize)의 차이점을 설명해 주세요.

## 답변

웹 브라우저 마다 기본적으로 제공하는 스타일이 조금씩 다르기 때문에, 브라우저 마다 일관성 있는 화면을 보여주기 위해서 초기화(Reset) 또는 정규화라고 하는 표준화(Normalize) 작업이 필요합니다.
그 중에서 초기화(Reset)는 모든 요소의 크기나 여백, 기타 모양을 말 그대로 초기화하여 처음부터 스타일을 다시 추가할 수 있게 하는 개념입니다.
반면에 표준화(Normalize)는 브라우저 간의 스타일 차이를 일관성 있게 적용하기 위해 기본 스타일을 유지하며 일치시키는 개념입니다.
그래서 페이지 스타일의 많은 부분을 원하는 대로 커스터마이징 하려면 초기화(Reset)를 사용하고, 브라우저의 기본 스타일을 활용하려면 표준화(Normalize)를 사용하는 것이 좋습니다.

———————————————————————————————————————————————————

## 질문

마진 병합(Margin Collapse) 현상이랑 무엇인지 설명해 주세요.

## 답변

마진 변합은 서로 다른 두 요소의 CSS `margin` 속성의 값이 중첩되어 하나의 값 으로만 출력되는 현상을 말합니다.
기본적으로 두 형제 요소의 위아래 마진이 만나면 중첩되어 더 큰 값으로 결합하고, 또 부모와 자식 요소의 위쪽이나 아래쪽 마진이 서로 만나면 중첩되어 부모 요소의 마진 값으로 결합됩니다.
그래서 마진 병합은 블록 요소 간의 수직 정렬 간격을 일정하게 유지하거나 자식 요소를 통한 부모 요소의 여백 설정에서 유용할 수 있지만,
레이아웃 코드에 대한 가독성이 떨어지므로 간접적인 여백 생성의 마진 병합을 피하고 최신의 Flex나 Grid를 사용하는 것이 좋습니다.

———————————————————————————————————————————————————

## 질문

오픈 그래프(Open Graph)는 무엇이고 어떤 역할을 하는지 설명해주세요.

## 답변

오픈 그래프는 웹 페이지의 제목, 설명, 이미지, URL 등의 메타 정보를 정의하는 규약(프로토콜0입니다.
이 메타 정보를 통해 페이스북이나 카카오톡 등 다양한 플랫폼에서 URL을 공유할 때 해당 페이지의 미리보기로 표시될 정보를 제공할 수 있고, 사용자는 URL로 접속하기 전에 해당 페이지의 기본 정보를 미리 확인할 수 있습니다.
대부분의 플랫폼 검색 엔진은 공유된 URL의 페이지 전체 로딩을 기다리지 않고 빠르게 메타 정보만 읽어서 해당 페이지를 파악하므로, 오픈그래프나 트위터 카드 같은 메타 정보를 잘 제공해야 검색 엔진 최적화(SEO)에도 도움이 됩니다.
그래서 SPA(Single Page Application) 같은 단일 HTML 제공 사이트는 페이지 구조에 따라 이러한 메타 정보를 위해 별도의 컴퓨팅 서버가 필요할 수 있습니다.

---

---

---

## 질문

Git Master와 Main 브랜치의 차이점을 설명해 주세요.

## 답변

대표적인 VSC(Version Control System)인 Git에서는 기본적으로 주 브랜치로 `master` 브랜치를 사용했지만, Git 2.28 버전부터 주 브랜치를 `main` 브랜치로 변경하였습니다.
'Master'라는 단어는 주종 관계와 같이 인종 차별적인 것으로 인식될 수 있어, 'Main'이라는 단어로 변경되었다고 합니다.
그래서 Git 2.28 미만 버전에서는 `git config --global init.defaultBranch main` 명령어로 주 브랜치를 변경을 구성하거나, 프로젝트 단위로는 `git branch -m master main` 명령어로 주 브랜치를 변경할 수 있습니다.

## 질문

Git flow 전략을 사용하는 이유와 주요 브랜치에 대해 설명해 주세요.

## 답변

Git Flow는 복잡한 프로젝트 개발에서 안전성과 효율성을 향상시키며 버전 관리를 하기 위한 브랜치 관리 전략을 말합니다.
담당자에 따라 이름은 조금씩 다를 수 있지만, 주로 `main`, `dev`, `feature`, `release`, `hotfix`로 역할에 맞게 브랜치를 구분합니다.

`main`은 실제 출시 제품의 브랜치
`dev`는 여러 기능을 병합하는 등의 용도로 안전한 개발을 위해 사용되는 브랜치
`feature`는 `feature/login`, `feature/dashboard` 같이 기능별 이름을 추가해 개발을 진행하는 브랜치 `release`는 출시 버전을 준비해 버저닝하는 브랜치  
`hotfix`는 `hotfix/auth` 같이 사용하며, 긴급 버그 수정을 위해 사용하는 브랜치  
이렇게 각 브랜치를 역할에 맞게 엄격하게 사용해야, 브랜치 간의 병합과 충돌을 최소화해서 프로젝트의 안정성과 효율성을 높일 수 있습니다.

## 질문

Git Merge와 GitHub Pull Requests의 차이점을 설명해 주세요.

## 답변

Git Merge는 단순히 로컬 개발 환경에서 각 브랜치를 병합할 때 사용하는 명령으로, 발생하는 충돌을 직접 해결하기 쉽고 별도의 검토나 승인 없이 빠르게 병합할 수 있습니다.
반면에 GitHub Pull Requests는 원격 저장소에서 다른 개발자와의 협업을 위해 사용하는 기능으로, 병합 전에 코드 리뷰 등의 피드백을 받을 수 있어서 여러 개발자가 변경 사항을 검토하고 토론할 수 있으며, 프로젝트에 따라 관리자 승인이 필요할 수 있기 때문에 더 안전하게 코드를 병합하는 좀 더 구조화된 과정입니다.
그래서 간단한 변경 사항의 브랜치 병합은 로컬에서 Git Merge 명령을 사용하고, 더 복잡한 변경 사항이나 협업을 위한 코드는 되도록 GitHub Pull Requests 기능을 사용해서 병합하는 것이 좋습니다.

## 질문

Markdown 문법 중 코드 블록(Code Block)과 인라인 코드(Inline COde)의 차이점에 대해 설명해 주세요.

## 답변

`마크다운 문법` 에서는 코드 블록은 주로 여러 줄의 코드 영역을 표시할 때 사용하는 기능으로, 백틱(<code>\`</code>) 기호를 연속으로 3개씩 사용해 코드의 시작과 끝을 표시합니다.
그리고 코드 클록은 <code>\`\`\`html</code> 과 같이 작성 코드의 언어를 명시할 수도 있어서 코드의 가독성을 높이고 코드 하이라이팅을 적용할 수도 있습니다.
반면에 인라인 코드는 한 줄의 코드 영역을 표시할 때 사용하는 기능으로, <code>\`background-color\`</code> 처럼 백틱 기호 1개씩 코드의 싲작과 끝에 사용합니다.
그래서 문장 안에서 코드 부분을 강조하는 용도로 사용됩니다.
