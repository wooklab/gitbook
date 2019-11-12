---
description: rebase 하는 방법
---

### Rebase 하는 방법

```bash
# rebase 하는 법
git checkout ${rebase_dest_branch}
git pull origin ${rebase_dest_branch}
git checkout ${rebase_src_branch}
git rebase -i ${rebase_dest_branch}

# 충돌 발생시 충돌 해결 후 계속 진행하기.
git rebase --continue

# local 상에서 rebase가 정상 완료가 강제 푸시
git push --force-with-lease

# 오류 발생시
git rebase --abort
```
