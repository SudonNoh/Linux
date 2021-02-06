## 명령어


### find 명령어
find 검색조건에 맞는 파일을 지정한 위치에서 찾는 것을 말한다.

-name: 파일 이름으로 검색  
-type: 파일 타입은 ~다.  
-user: 로그인 아이디 소유주 대상(root, centos) ex: -user centos  
-perm: 지정한 접근 권한과 일치하는 파일 검색  
-exec: 명령어를 수행하라는 뜻 -exec cp {} \;


```linux
#echo "명령어 옵션 확인"
find -help

#echo "/usr directory에서 ls라는 이름을 가진 파일을 찾기"
find /usr -name ls
find /usr -name service

find . -type f -name 'servic*' -print

#echo "현재 directory에서 파일을 찾는데, 비어있는 모든 이름의 파일을 찾음. 다 찾은 다음 ls -l 을 실행"
find . -type f -name '*' -empty -exec ls -l {} \;

```


### cat 명령어

```linux
# "텍스트 파일 내용 출력"

cat /etc/profile | less #echo "한 line씩 검색도 가능"
cat /etc/profile | more #echo "한 page씩"
```


### grep 명령어

grep 찾고자하는 문자열 검색

```linux
# "grep [옵션][찾을 문자열]"

# "test3 을 포함한 내용을 출력하라"
ls -l | grep test3

# "-i 옵션은 test3 이라는 문자를 대소문자 구분없이 포함한 내용을 출력하라"
ls -l | grep -i test3

# "-v 옵션은 test3 이라는 문자에 대해서 내용을 제외하고 출력하라"
ls -l | grep -v test3

# "test3 이라는 문자를 대소문자 구분없이 문자열을 제외하고 출력하라"
ls -l | grep -iv test3
```

### whereis / which

```linux
whereis java  
# "JAVA의 모든 경로를 출력"

which java
# "JAVA의 실제 실행 위치를 출력"
```
