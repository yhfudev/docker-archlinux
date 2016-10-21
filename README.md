# docker-archlinux
create a Arch Linux docker image

## Usage

Install dependencies

    sudo pacman -S git expect arch-install-scripts docker

Build baseline Arch Linux docker image

    git clone https://github.com/yhfudev/docker-archlinux.git
    cd docker-archlinux
    ./runme.sh
    MYUSER=${USER}
    MYARCH=$(uname -m)
    sudo docker build -t ${MYUSER}/archlinux-${MYARCH}:latest .

Run and test

    sudo docker run -i -t --rm ${MYUSER}/archlinux-${MYARCH} /bin/bash

