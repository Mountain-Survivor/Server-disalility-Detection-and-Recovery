# nginx 컨테이너 중단

## 증상
HTTP 응답을 받기 전에 연결을 실패함
curl: (7) Failed to connect

## 원인과 확인 근거
컨테이너가 중단 되었음. docker ps -a에서 web의 Exited (0) 상태 확인

## 복구 방법
docker start web 으로 컨테이너를 다시 시작해서 복구함

## 복구 확인
curl을 통해서 200OK를 확인하고 복구를 확인
