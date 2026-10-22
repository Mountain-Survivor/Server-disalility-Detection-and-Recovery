# nginx Down

## 장애 발생
'docker compose stop web'

## 지표
up{job="nginx"}의 값은 exporter가 살아있으므로 1로 뜬다. nginx_up은 nginx가 멈췄으므로 0으로 뜬다.

## 알림
'nginx_up == 0'
30s
0이 된 것이 감지되면 pending 상태가 되며, 그것이 30초 이상 지속되면 firing 상태가 된다.

## 복구
'docker compose start web'
실행 후 alert는 inactive 상태로 돌아왔다.
