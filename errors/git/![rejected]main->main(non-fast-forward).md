# ![rejected] main -> main (non-fast-forward)

<br>

```
git push -u origin main
To https://github.com/lew0205/TIL.git
 ! [rejected]        main -> main (non-fast-forward)
error: 레퍼런스를 'https://github.com/lew0205/TIL.git'에 푸시하는데 실패했습니다
힌트: 현재 브랜치의 끝이 리모트 브랜치보다 뒤에 있으므로 업데이트가
힌트: 거부되었습니다. 푸시하기 전에 ('git pull ...' 등 명령으로) 리모트
힌트: 변경 사항을 포함하십시오.
힌트: 자세한 정보는 'git push --help'의 "Note about fast-forwards' 부분을
힌트: 참고하십시오.
```
TIL을 푸시하던 중 이런 에러를 만났다.<br>

### 원인
원인은 잘 모르겠다.<br>
다음에 알아보고 수정해야겠다.

### 해결방법
브랜치 명 앞에 +를 붙이면 된다.
```
<수정 전>
git push -u origin main
------------------------
<수정 후>
git push -u origin +main
```
이렇게 수정하면 오류가 발생하지 않고 제대로 푸시되는것을 확인할 수 있다.