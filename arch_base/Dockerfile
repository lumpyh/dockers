FROM archlinux:latest

RUN pacman -Syu --noconfirm

RUN pacman -S --noconfirm neovim git sudo

RUN useradd -s /bin/bash -U -m developer

CMD [ "/bin/bash" ]

