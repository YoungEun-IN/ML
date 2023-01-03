- NGINX 포드 생성

`kubectl run nginx --image=nginx`

- POD 매니페스트 YAML 파일(-o yaml)을 생성합니다. 만들지 마세요(--드라이런)

`kubectl run nginx --image=nginx --dry-run=client -o yaml`

- 배포 만들기

`kubectl create deployment --image=nginx nginx`

- 배포 YAML 파일(-o yaml)을 생성합니다. 만들지 마세요(--드라이런)

`kubectl create deployment --image=nginx nginx --dry-run=client -o yaml`

- 배포 YAML 파일(-o yaml)을 생성합니다. 복제본 4개(--replicas=4)로 생성하지 마세요(--dry-run).

`kubectl create deployment --image=nginx nginx --dry-run=client -o yaml > nginx-deployment.yaml`

- 파일에 저장하고 필요에 따라 파일을 변경(예: 복제본 추가)한 다음 배포를 생성합니다.

`kubectl create -f nginx-deployment.yaml`

- 또는 k8s 버전 1.19+에서는 --replicas 옵션을 지정하여 4개의 복제본으로 배포를 생성할 수 있습니다.

`kubectl create deployment --image=nginx nginx --replicas=4 --dry-run=client -o yaml > nginx-deployment.yaml`
