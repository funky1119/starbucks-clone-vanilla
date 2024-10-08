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

&nbsp;

# GIT 명령어

## 기본 명령어

1. git --version (git 버전 확인 방법)
2. git init (현재 프로젝트에서 변경사항 추적(버전 관리)을 시작)
3. git status (git 상태 확인)
4. git add . (모든 파일의 변경사항을 추적하도록 지정)
5. git commit -m "커밋 메시지" (메세지(-m)와 함께 버전을 생성)
6. git push origin master (origin이랑 별칭의 원격 저장소로 버전 내역 전송)
7. git pull (git 원격 저장소에서 업데이트 된 코드 다운로드)
8. git clone [주소](git 원격 저장소에서 코드 복제)
9. git remote add orgint [주소] (origin이랑 별칭으로 원격 저장소를 연결)
10. git reset --hard HEAD~1 (최신 커밋 하나를 취소하고 되돌아가기)
11. git reset --hard ORIG_HEAD (커밋 취소 된 상태에서 다시 복구 시킬 때)
12. git branch -m master main (마스터 브랜치 이름을 main으로 변경)

## 개행 문자(New line) 설정

### macOS

- $git config --global core.autocrlf input

### windows

- $git config --global core.autocrlf true

## 사용자 정보

### 커밋(버전 생성)을 위한 정보 등록

- $git config --global user.name "사용자 이름"
- $git config --global user.email "사용자 이메일"

## 구성 확인

### Q키를 눌러서 종료!

- $git config --global --list

## 새로운 프로젝트 Push

1.  git init
2.  git config --global init.defaultBranch main (마스터 브랜치 이름을 main으로 변경)
3.  git config --global core.autocrlf input
4.  git config --global user.name "사용자 이름"
5.  git config --global user.email "사용자 이메일"
6.  git config --global --list
7.  git add . (모든 파일 추가)
8.  git commit -m "커밋 메시지" (깃 커밋 생성)
9.  git log (깃 커밋 로그 확인)
10. git remote add origin [주소] (깃 원격 저장소 주소 추가)
11. git push origin master (깃 원격 저장소에 업로드)

## Branch 명령어

1. git branch (브랜치 목록 확인)
2. git branch -a (모든 브랜치 목록 확인)
3. git branch [브랜치 이름] (새로운 브랜치 생성)
4. git checkout [브랜치 이름] (브랜치 이동)
5. git merge [브랜치 이름] (브랜치 병합)
6. git branch -d [브랜치 이름] (브랜치 삭제)

## GIT 버전 관리하지 않을 폴더 및 파일 설정

- .gitignore 로 설정

```
  .idea
  .vscode
  .node_modules
  .DS_Store
```
