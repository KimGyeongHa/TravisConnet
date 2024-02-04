# Travis Connect

1. bootjar 이용한 docker build > gradle build로 전환
2. dockerfile을 이용하여 compose에 바로사용 > dockerfile을 hub에 build 후 hub container image사용으로 변경
3. travis ci , github action 중 하나 선택하여 사용


# 오류
1. travis ci 이용중 gradle build 시 메모리 부족으로 인한 오류 발생 -> dist: focal (새로운 가상머신 사용하도록 설정하여 더 많은 메모리를 사용할 수 있게함)

  Travis ci에서 ubntu 버전을 지정할때 사용하는 코드   
  1. focal: Ubuntu 20.04 LTS (Long Term Support)의 코드명
  2. bionic: Ubuntu 18.04 LTS의 코드명
