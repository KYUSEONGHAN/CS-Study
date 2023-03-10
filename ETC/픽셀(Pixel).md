![](https://mblogthumb-phinf.pstatic.net/20121229_81/phominator_13567923989663LNtq_JPEG/rose_flower_screensaver-234027-1240456558.jpg?type=w2)

## 픽셀
- Pixel
- 픽셀이란 컴퓨터 이미지, 디스플레이를 구성하고 있는 최소 단위.
- 모니터를 통해서 보는 모든 문자와 이미지는 실제로는 픽셀이라고 하는 매우 작은 사각형들로 구성되어있다.

## 해상도
- 어떤 이미지나 디스플레이를 구성하는 최소 단위인 픽셀의 총량을 나타내는 말.
- 픽셀의 밀도를 나타내는 용어로도 사용됨.

## 해상도에 따른 이미지 용량 계산
- 이진 영상(binary image)
    - 디지털 이미지 중 가장 간단한 형태를 말한다. 이진 영상은 각 픽셀(pixel)이 1bit로 이루어져 있으며, 각 픽셀은 오직 밝음(1)과 어두움(0) 두 가지만을 표현한다.
- 컬러 영상(color image)
    - 컬러 영상은 3개의 채널로 표현된다. 이때 3개의 채널은 빛의 3원색인 빨강(red), 녹색(green), 파랑(blue)이며, 각 채널은 0~255 사이의 값으로 빨강의 정도, 녹색의 정도, 파랑의 정도를 각각 나타낸다.
    - 컬러 영상에서는 각각의 8bit의 기본 컬러 3개를 조합하여, 256x256x256=16,777,216개의 컬러를 만들어낼 수 있으며 8bit(red, green, blue) 3개를 조합하여 총 24bit를 이용하여 컬러를 표현했으며 이를 트루 컬러(True color)라고 부른다. 24bit(RGB : 8bit / 8bit / 8bit) 는 하나의 픽셀당 표현할 수 있는 bit의 크기이다.
    - 즉, 1px(픽셀)을 표현하기 위해서는 1byte(바이트)가 필요하고, 8bit(비트)를 표현하기 위해서는 1byte(바이트)를 사용하기에 1px(픽셀)은 1byte(바이트)라는 결론이 나온다.
- ex
    - RGB 8bit 모드로 720 x 720 픽셀의 이미지가 있다고 가정
    - 한개의 픽셀은 24bit용량을 가진다.
    - 계산 결과 1픽셀 당 3byte의 용량을 차지한다.

## 참고자료 출처
[https://velog.io/@ichbinmin2/%EB%B9%84%ED%83%84%EA%B8%B0-2.-1%ED%94%BD%EC%85%80%EC%9D%80-%EB%AA%87%EB%B0%94%EC%9D%B4%ED%8A%B8%EC%9D%B8%EA%B0%80%EC%9A%94](https://velog.io/@ichbinmin2/%EB%B9%84%ED%83%84%EA%B8%B0-2.-1%ED%94%BD%EC%85%80%EC%9D%80-%EB%AA%87%EB%B0%94%EC%9D%B4%ED%8A%B8%EC%9D%B8%EA%B0%80%EC%9A%94)