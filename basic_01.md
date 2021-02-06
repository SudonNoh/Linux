## 명령어

find 검색조건에 맞는 파일을 지정한 위치에서 찾는 것을 말한다.

-name: 파일 이름으로 검색  
-type: 파일 타입은 ~다.  
-user: 로그인 아이디 소유주 대상(root, centos) ex: -user centos  
-perm: 지정한 접근 권한과 일치하는 파일 검색  
-exec: 명령어를 수행하라는 뜻 -exec cp {} \  


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
