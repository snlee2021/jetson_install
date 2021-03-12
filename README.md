# jetson_install


1. jetson xavier agx : sdkmanager -> 외장형 SSD

 https://m.blog.naver.com/tinz6461/221622578379


2.jetson xavier nx  ->  s-ssd 메모리 사용


3. jetson tx2:sdkmanager   -> 외장형 SSD

https://medium.com/@plantstoen/jetson-sdk-manager%EB%A5%BC-%EC%9D%B4%EC%9A%A9%ED%95%B4-jetson-tx2%EC%97%90-%EA%B0%9C%EB%B0%9C%ED%99%98%EA%B2%BD-%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0-35ac7b5b3994


4.nano  -> ssd 메모리 사용


# swapfile 생성

fallocate -l 8G swapfile # 8G짜리 파일을 만듬
chmod 0600 swapfile
ll swapfile -h # 확인

mkswap swapfile #swapfile 형식 적용
swapon swapfile #swap에 쓰일 수 있도록 켜줌 (swap on)

swapoff -v swapfile # swap off
rm -rf swapfile # 제거
free -m # 확인
