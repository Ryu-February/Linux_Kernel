# 🍓 Raspberry Pi 4B Linux Kernel Playground

About

라즈베리파이 4B에서 리눅스 커널을 커스터마이징하고 빌드하는 프로젝트

커널 빌드 및 수정

모듈 추가 및 삭제

디바이스 드라이버 개발

부팅 프로세스 커스터마이징

Requirements

Raspberry Pi 4 Model B (4GB RAM 이상 권장)

microSD 카드 128GB(32GB 이상)

Ubuntu/Debian 기반 개발 PC

Setup

크로스 컴파일러 설치

sudo apt update
sudo apt install gcc-aarch64-linux-gnu

커널 소스 다운로드

git clone --depth=1 https://github.com/raspberrypi/linux.git -b rpi-5.15.y

커널 설정 및 빌드

cd linux
make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- bcm2711_defconfig
make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- -j$(nproc)

빌드 아웃풋 복사 및 적용

Image, modules, dtbs 파일을 Raspberry Pi 부팅 디렉터리에 복사

TODO

디바이스 트리 수정 및 LED 제어

커스텀 드라이버 모듈 작성 및 삽입

부트 로더 커스터마이징

Bare Metal 수준 최적화

🧸 만든 사람

찬영 (Chanyeong)Firmware / Embedded Linux Nerd 🤓
Firmware / Embedded Linux Developer


✨ 하고 싶은 것들

빌드된 이미지(Image, modules, dtbs)를 라즈베리파이에 복사해서 부팅!



