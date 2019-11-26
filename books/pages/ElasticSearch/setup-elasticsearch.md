---
description: Elasticsearch install and configuration
---

### 시스템 설정
1. max open files 설정
```bash
# vi /etc/security/limits.conf
ai - nofile 65536 # ai는 실행 유저 아이디
```

2. num of thread 설정
```bash
#vi /etc/security/limits.conf
ai - nproc 4096 #es 권장 4096이상
```

3. max filesize 설정
```bash
#vi /etc/security/limits.conf
ai - fsize unlimited
```

4. address space 설정
```bash
#vi /etc/security/limits.conf
ai - as unlimited
```

5. max locked in memory 설정
```bash
#vi /etc/security/limits.conf
ai - memlock unlimited
```

6. vm 설정
```bash
#vi /etc/sysctl.conf
vm.max_map_count=262144 #설정 확인
# $sysctl vm.max_map_count
# 바로 적용이안되면
sudo sysctl -w vm.max_map_count=262144
sudo sysctl -w vm.swappiness=1
```


