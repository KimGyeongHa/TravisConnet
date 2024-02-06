# Travis Connect

1. bootjar 이용한 docker build > gradle build로 전환
2. dockerfile을 이용하여 compose에 바로사용 > dockerfile을 hub에 build 후 hub container image사용으로 변경
3. travis ci , github action 중 하나 선택하여 사용


# 오류
1. travis ci 이용중 gradle build 시 메모리 부족으로 인한 오류 발생 -> dist: focal (새로운 가상머신 사용하도록 설정하여 더 많은 메모리를 사용할 수 있게함)

2. dockerfile build 중 ../ 으로 상위폴더 접근을 하였으나, docker에서는 ../ 상위폴더 접근을 지원하지않음 > dockerfile 위치변경

3. travis ev name값에 - 사용불가  > _로 대체하여 사용

4. application.yml 설정파일이 보안문제로 git repository에 올라오지 않고 있었다. > private repo를 생성하여 submodule로 사용하여 설정파일 사용하기
