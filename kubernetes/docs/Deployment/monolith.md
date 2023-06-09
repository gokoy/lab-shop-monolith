
#### Object: monolith
#### Type: Deployment

### Cluster에 monolith Deployment를 생성하려면 아래의 명령어를 실행하세요.

```
$ kubectl create -f https://minio.msaez.io/labs-msaez.io/yamlStorage/undefined/gokoy50%40gmail.com/Deployment/monolith.yaml?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=minio%2F20230609%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230609T021127Z&X-Amz-Expires=60&X-Amz-SignedHeaders=host&X-Amz-Signature=17b645b7e73f77d9b88983c52ba60217988692855000dc5e272abc586e53a2f9
```
- Yaml 파일에 명시된 스펙으로 monolith Deployment를 생성합니다.

```
$ kubectl apply -f https://minio.msaez.io/labs-msaez.io/yamlStorage/undefined/gokoy50%40gmail.com/Deployment/monolith.yaml?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=minio%2F20230609%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20230609T021127Z&X-Amz-Expires=60&X-Amz-SignedHeaders=host&X-Amz-Signature=17b645b7e73f77d9b88983c52ba60217988692855000dc5e272abc586e53a2f9
```
- Create가 된 상태라면 monolith Deployment의 수정이 이루어지고, Create가 된 상태가 아니라면 monolith Deployment를 Create 해주는 명령어입니다.  
#

### monolith Deployment가 정상적으로 생성되었는지 확인하시려면 아래의 명령어를 실행하세요.

```
$ kubectl get Deployment

NAME            READY   UP-TO-DATE   AVAILABLE   AGE
monolith           3/3     3            3           5m43s

```
- monolith Deployment와 Pod, Replicaset이 모두 확인이 된다면 정상적으로 생성된 것입니다.
#

### 생성된 monolith Deployment의 상세 실행 정보를 확인하시려면 아래의 명령어를 입력하세요.

```
$ kubectl describe Deployment monolith
```
- monolith Deployment의 상태를 확인하여 문제가 있는지 확인합니다. 
#

### Kubernetes Cluster network 외부에서 service에 access할 때, 해당 명령어로 외부 IP traffic을 허용할 수 있습니다.

```
$ kubectl port-forward Deployment/monolith 8080:8080
```
#

### monolith Deployment를 삭제하려면 아래의 명령어를 실행하세요.

```
$ kubectl delete Deployment monolith
```
#

