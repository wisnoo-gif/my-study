#도커를 이용한 웹 서버 배포 및 외부접속(port forwarding) 실습
```
docker pull kchris000/simple-web-python    #이미지 다운로드 
```
```
docker run -d --name my-python-web -p 7070:7070 kchris000/simple-web-python   #컨테이너 이름 설정 및 7070번 포트포워딩(리눅스의 7070번 문으로 들어오면, 컨테이너의 7070번으로 연결하도록) 
```
```
docker logs my-python-web  #상태 확인 
```
```
firewall-cmd --permanent --add-port=7070/tcp  #방화벽 7070번 허용
sudo firewall-cmd --reload                    #방화벽 적용
```
```
curl localhost:7070    #내부 점검(html 코드가 보이면 컨테이너, 포트연결 정상)
```
192.168.56.115:7070 에 접속
