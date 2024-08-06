### Remote 저장소의 URL을 변경하고 싶을 때

```bash
$ git remote set-url origin {변경할 주소}
```

### Remote 저장소의 URL을 확인하고 싶을 때

```bash
$ git remote -v
```

---

### Commit 로그를 파일로 저장하고 싶을 때

모든 내역을 저장

```bash
$ git log > {저장할 파일명}.txt
```

범위를 지정하여 저장

```bash
# 최근 커밋에서 5번째 이전 커밋까지 로그를 저장
$ git log HEAD~5...HEAD > {저장할 파일명}.txt
```
