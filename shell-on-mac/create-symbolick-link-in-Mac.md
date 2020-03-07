# 맥에서 심볼릭 링크 만들기

## 심볼릭 링크
리눅스에서 특정 폴더 또는 파일을 링크하는 기능으로 윈도우에서 바로가기와 비숫하다.

### bash 명령어

##### `/path/to/original`에 대한 심볼릭링크 `/path/to/symlink` 를 만든다.
````
ln -s /path/to/original /path/to/symlink 
````
##### 심볼릭링크 `/path/to/symlink` 를 삭제한다.
````
unlink /path/to/symlink
````
##### 상세
- `ln` 링크 생성, `unlink` 링크 삭제
- `-s` 심볼릭 링크  
- `/path/to/original` 원본 파일 또는 폴더  
- `/path/to/symlink` 심볼릭 링크 파일명 또는 폴더명  


### visual studio code 

##### 심볼릭 링크 만들기
```` 
ln -s /Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin/code /usr/local/bin/vscode
````
##### /usr/local/bin 폴더에 만들면 전역에서 심볼릭 링크 이름만으로 접근 가능하다.
```` 
// . 을 적어 주면 vscode 가 현재 폴더를 선택하여 실행된다.
vscode . 
````

### 참조
https://apple.stackexchange.com/questions/115646/how-can-i-create-a-symbolic-link-in-terminal/115647
https://gist.github.com/bangonkali/02ba0dc50aebca627fa68ff3a7325b8e


## 참고

### /usr/local/bin
/usr/local/bin 폴더 역활이 뭔가 싶어 검색했다.  
`man hier` 명령어로 파일시스템 구조에 대한 설명을 볼 수 있다.

- /usr/ contains the majority of user utilities and applications  
    > 사용자의 주요 유틸리티와 어플리케이션 폴더
    - local/ executables, libraries, etc. not included by the basic operating system
        > 기본 운영 시스템에 포함되지 않은, 실행 파일 또는 라이브러리 등
        - /bin 
            > 따로 설명은 없지만 참조 링크를 참고해 보면, 사용자가 설치하는 부가적인 응용 프로그램은 여기에 위치시키면 되는 것 같다.

#### 참조
https://wookiist.tistory.com/10
