# 고등학생의 온라인 영어 강의 선택을 도와 주기 위한 강의 추천 웹 앱
Lecture recommendation web app to help hight school students choose online English lectures   
팀 프로젝트

* **역할**   
프론트엔드   
* **목표**   
수 많은 인터넷 영어 강의 중 학생에게 적합한 강의 추천하기   
* **개발 환경**   
React, React-query, Redux-toolkit
   
---   
   
### **목차**
1. 요구사항 분석
2. System Diagram
3. 구현 예시 (일부 UI)
4. 기능 및 구조 ( 간단한 설명 )
   
---   
   
## 1. 요구사항 분석
> * 사용자 요구사항
>   
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/731537df-736b-4a88-9549-8ee4794460db)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/79add7db-693b-4934-83fc-93b51167bc49)
> 
> ---
> 
> * 운영자 요구사항
> 
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/7223377a-00d1-49b2-8988-dc472f20afe0)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/414d6bab-39aa-43d7-8d0c-1bd1ca5afd5c)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/f7b12b9c-5e18-4822-b039-e55ed72c18dc)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/7fbfa9b7-ead9-4488-a043-6f70e218fcfe)
   
---   
    
## 2. System Diagram
> * Data Flow Diagram
>   
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/3b9c3fce-f499-4e34-9a10-7263f0e56a77)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/6e47b912-4bff-4a7a-8a55-f6f80854029a)
> 
> ---
> 
> * 업무기능분해도
>     
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/1dedaa68-ad03-4f58-8785-2fda52cf4b62)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/f8c67329-d2ac-487a-8add-41d5fc82aa3e)
   
---   
    
## 3. 구현 예시 (일부 UI)
> * 사용자 UI
>   
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/099c5c1c-52e2-43f6-aacf-28f4c8df096a)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/2c4e8e16-3961-4920-9406-7874057387ba)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/f0652f88-bda8-488c-8e6e-705d0e2a91ee)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/216fcbd9-7046-4962-a5db-e067c5265753)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/ef279ee0-4f44-4412-81d1-424dc48bcbe3)
> 
> ---
> 
> * 운영자 UI
>   
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/1d0523b3-67cd-43cf-8dd9-d94450f88855)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/95b00da4-0dfd-4f12-b916-6c9692c4657a)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/75b119ea-1ffd-4092-a3bc-466427801e86)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/c1a3ae98-51ad-446a-adf6-0816138b69ed)
> ![image](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/0828068b-b190-4517-bdc0-73eba287f706)
   
---   
    
## 4. 기능 및 구조 ( 간단한 설명 )
* 프로젝트 구조   
> 프로젝트의 전체 구조는 AWS EC2(아마존 클라우드 서버 호스팅 서비스) 위에 Docker를 이용하여 프론트(NodeJS, React), 백엔드(Java, Spring Boot), DB 등의 여러 서버 컨테이너를 올려놓는 구조로 동작합니다. 2개의 도메인으로 분리되어 사용자, 운영자 각각의 웹으로 구성됩니다. 각 웹 앱은 다시 프론트 서버와 백엔드 서버로 분리되며, 프론트엔드는 CSR로만 구현됩니다.
* 추천 기능   
> 이 기능은 사용자의 설정과 테스트 점수, 3단계로 구성된 라벨링으로 강의를 추천하는 방식이었습니다. 이를 위해, 문제에 라벨링을 해야만 했는데 처음에는 대, 중, 소를 기준으로 분류하려했지만, 이 방식으로 문제를 나누게 되면 기준이 모호해지는 문제가 있었습니다. 따라서, 추천 강의를 기초-개념-완성-풀이로 분류하는 방식으로 변경했습니다. 
* 라벨링 검색 요청 빈도 줄이기
> 추천 로직에는 인강마다 라벨링 기반으로 동작하는 부분이 있었는데, 라벨링을 DB에 저장해 관리하면서 라벨링 데이터를 조회하는 input이 라벨을 만드는 모달, 변경에 따른 중복 확인 등 여러 곳에서 사용되고 있었습니다. 프로젝트가 CSR로 동작했기 때문에, 만약 비슷하거나 동일한 라벨을 검색하게 되는 경우 같은 내용으로 데이터를 여러 번 요청하게 되는 등 자원이 낭비되었습니다.   
> 이 문제를 풀기 위해 여러 해결 방안을 살펴보다가 디바운싱과 리액트 쿼리에 대해 알게 되었습니다. 먼저 디바운싱의 적용을 위해, 변경할 문자열을 받아 지연된 시간(400ms)을 기다린 뒤 입력이 없으면 기존 문자열을 변경하는 useDebounce라는 훅을 만들었습니다. 그 후 잦은 호출 방지를 위해 리액트 쿼리의 retryDelay 옵션으로 실패에 따른 재요청 횟수를 1회로 제한하고, 2초에 1번 실행되도록 제한을 설정했습니다.   
> 이를 공통으로 사용될 input 컴포넌트에 적용하였고, 라벨 목록을 조회 input에서의 API 요청이 이전에는 '테스트'라는 문자열을 검색할 경우 6번이었지만 개선 후 1번으로 감소했습니다. 여기에 여러 곳에서 사용되던 컴포넌트를 하나에서 유지, 보수할 수 있게 되었습니다. 또, 리액트 쿼리의 캐싱 덕분에 다른 페이지에서 조회한 데이터를 검색해도 이전에 요청한 것과 동일한 검색어는 응답을 기다리지 않고 바로 노출되어 사용자가 빈 화면을 기다리지 않을 수 있었습니다.   
> 아쉬운 점은 저에게는 400ms으로 입력 속도를 정한 것이 효과를 보았지만, 사용자의 입력 속도에 따라 효과가 미미해질 수 있다는 점과 지연이 길어질수록 요청에 대한 반응도 느려진다는 것이었습니다.   
> ![1](https://github.com/Taeyeon-Lim/Lecture-recommend-web-for-highSchool/assets/54977412/71805e17-b872-4c48-9301-8de892e22ad7)
* 무한 스크롤
> 라벨, 유저, 강좌 등의 목록에서 무한 스크롤 형식을 구현하는 요구 사항이 있었습니다. window.scroll 관련 이벤트를 이용하여 구현할 수도 있었지만, 이 방식이 window 객체를 직접 사용하여 스크롤을 항상 감시해야하기 때문에 성능 저하를 야기한다고 생각했습니다. 다른 방식을 찾던 중 Intersection Observer API를 발견했습니다. 이 wep API는 기존 스크롤링 방식처럼 요소의 크기나 위치를 계산하고 reflow를 수행하지 않으며 스크롤바의 상태에도 주목하지 않습니다. 다만, 요소의 가시성을 이용하여 교차 여부를 관찰한 뒤에 동작을 일으킵니다. 따라서, 매 번 스크롤을 할 때마다 이벤트를 트리거하여 함수를 실행시키지 않습니다. 이를 위해, IntersectionObserver(callback, options) 객체를 생성하여 교차 범위와 관찰 대상의 부모 요소를 지정하도록 root, rootMargin, threshold와 같은 옵션을 설정해야 합니다. 지정한 뒤, target 요소를 구독하면 설정된 교차 범위에 따라 목록을 불러옵니다. 목록 데이터가 전부 비동기 데이터였기 때문에, react-query의 fetchNextPage 함수를 이용하여 코드를 작성했습니다. 요소를 구독한 뒤에는 해당 요소는 꼭 구독 해제하여야 합니다.
> 아쉽게도 일부 브라우저에서 지원을 하지 않을 수 있기 떄문에 polyfill 등을 고려하여야 했습니다.
