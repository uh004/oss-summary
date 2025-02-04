# 📌fast forward merge, 3-way merge, rebase

## fast-forward 병합
```
$ git merge 브랜치 이름
```
- Merge할 대상이 현재 커밋의 직접적인 뿌리가 되는 경우 fast-forward 병합이 실행
- 병합할 브랜치의 조상이 기준 브래친인 경우 병합의 기본은 fast-forward 병합

## 3-way 병합
```
$ git merge 브랜치 이름 --3 way 병합은 브랜치 경로가 다른 갈래로 뻗어 나가 있을 때 적용
$ git merge --no-ff 브랜치 이름 -- --no-ff 옵션을 사용하면 3-way 병합으로 적용
```
- 두 브랜치의 조상이 같은 경우 새로운 커밋을 사용하여 두 기록을 합침

## 병합 시 주의점
- Merge 명령을 실행하기 전에 작업과 Stage 영역에 작업중인 파일이 없는지 꼭 확인

## rebase
- 두 갈래의 브랜치에서 기존의 베이스를 수정해 병합할 브랜치 마지막 커밋을 새로운 베이스로 수정하는 병합
```
$ git rebase 브랜치 이름
```

- 현재 HEAD가 devp/lst 브랜치를 가리키고 있다.

![화면 캡처 2022-11-21 224919](https://user-images.githubusercontent.com/105197524/203071972-b063a939-9a27-4f42-8619-bd973502ef5e.png)

- git rebase를 통해 main 이후로 devp/lst 브랜치를 재배치

![화면 캡처 2022-11-21 225017](https://user-images.githubusercontent.com/105197524/203072033-62c164e3-389e-49fc-8a6c-2a9ff2ed3533.png)

- 재배치 후 HEAD가 main 브랜치로 가리키고 병합을 한다.

![화면 캡처 2022-11-21 225120](https://user-images.githubusercontent.com/105197524/203072047-e91aa058-5e2b-487b-bdd3-610feee1b54f.png)

- 병합 완료 후 devp/lst 브랜치 삭제

![화면 캡처 2022-11-21 225143](https://user-images.githubusercontent.com/105197524/203072057-87dce123-6c34-4913-950e-55c3172e4f0e.png)
