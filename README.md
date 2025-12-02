[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/c9pJ25nj)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=21909380&assignment_repo_type=AssignmentRepo)
# 최종 테스트: 명언 관리 프로그램 만들기

## 코드 작성시 주의 사항

소스 코드 맨 위에 학번과 이름을 적고, 아너코드 선언문을 직접 입력할 것!
> 나 OOO는 하나님과 사람 앞에서 정직하고 성실하게 코딩 테스트를 수행하겠습니다.

## 문제 설명

유명인의 명언 목록을 관리하고 분석하는 프로그램을 C 언어로 제작하세요.

최대 50개의 명언 정보를 파일(`quotes.txt`)에서 읽어 관리하며, 다음 4가지 핵심 기능을 중점적으로 구현해야 합니다.

### 📌 데이터 구조

명언 정보는 다음과 같은 구조체 타입으로 미리 정해져 있습니다.
```
typedef struct st_quote{ 
	char author[100]; // 유명인 이름 (최대 100글자) 
	char text[255]; // 명언 내용 (최대 255글자) 
	int likes; // 추천수 (숫자) 
	int word_count; // 명언의 단어 수 (숫자, 공백 기준) 
} QUOTE;
```

### 📋 메뉴별 핵심 기능 설명

이 프로그램은 파일(`quotes.txt`)에서 데이터를 읽어 메모리에 로드한 후, 다음 4가지 핵심 기능(**4. Edit, 5. Remove, 6. Recommend, 7. Report**)이 정상적으로 동작하도록 구현해야 합니다.

| 메뉴 | 기능 설명 | 비고 | 
 | ----- | ----- | ----- | 
| **1. List** | 모든 명언 목록을 번호 순서대로 출력합니다. | (완성 코드로 제공됨) | 
| **2. Add** | 새로운 명언 정보(저자, 명언)를 입력받아 목록에 추가합니다. | (완성 코드로 제공됨) | 
| **3. Search** | 키워드를 입력받아 **저자 이름** 또는 **명언 내용**에 해당 키워드가 포함된 명언 정보를 출력합니다. | (완성 코드로 제공됨) | 
| **4. Edit** | 목록 번호를 입력받아 해당 명언의 **저자 이름**과 **명언 내용**을 다시 입력받아 수정하고, **`word_count`를 재계산**합니다. | **\[핵심 구현\]** | 
| **5. Remove** | 목록 번호를 입력받아 해당 명언을 목록에서 제거하고 메모리(동적 할당)를 해제합니다. 제거된 목록 이후의 명언들 이동 필수! | **\[핵심 구현\]** | 
| **6. Recommend** | 목록 번호를 입력받아 해당 명언의 **추천수(`likes`)를 1 증가**시킵니다. | **\[핵심 구현\]** | 
| **7. Report** | 다음과 같은 통계 정보를 출력합니다:<br> &nbsp; - 총 명언 개수 및 **평균 단어 수**<br> &nbsp; - **추천수(`likes`)가 가장 높은 명언 Top 3**의 정보를 출력합니다. | **\[핵심 구현\]** | 
| **8. Save** | 현재 명언 정보를 `quotes.txt` 파일에 저장합니다. | |
| **0. Exit** | 저장 후 프로그램 종료 (메모리 해제 필수) | |

### 📁 `quotes.txt` 구성 형식

파일은 명언 하나당 3줄로 구성됩니다. 
>저자
>
>내용
>
>추천수와 단어 수

## 제출 방법

LMS 공지 참고하세요.
