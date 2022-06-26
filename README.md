사전에 설정해야할 것들

secrets.DOCKER_USER
secrets.DOCKER_PASSWORD

secrets.EXAMPLE_GITOPS_DEPLOY_TRIGGER

repository: ianmiell/gitops-example-deploy
event-type: gitops-example-app-trigger
client-payload: '{"ref": "${{ github.ref }}", "sha": "${{ github.sha }}"}'

---
  aass
gitops 보일러플레이트

위 예제는 so1s-poc-nemne를 gitops로 변형한 레파지토리

app 내부는 예시용으로 지워도 상관없습니다. (단 app 내부에 Dockerfile이 있어야합니다.)

필요한 기술 스택
* docker
* k8s
* skaffold
* argocd
* github actions

