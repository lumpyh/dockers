FROM arch_base:base

ENV home /home/developer
ENV esp_dir /home/developer/esp

RUN mkdir $esp_dir

run sudo pacman -S --noconfirm --needed gcc git make ncurses flex bison gperf python-pyserial wget

run cd $home && wget https://dl.espressif.com/dl/xtensa-lx106-elf-gcc8_4_0-esp-2020r3-linux-amd64.tar.gz

run cd $home && tar -xzf $home/xtensa-lx106-elf-gcc8_4_0-esp-2020r3-linux-amd64.tar.gz -C $esp_dir

run echo "export PATH=\"$PATH:$esp_dir/xtensa-lx106-elf/bin\"" >> $home/.profile

run cd $esp_dir && git clone --recursive https://github.com/espressif/ESP8266_RTOS_SDK.git

VOLUME $home/workspace

run chown developer:developer -R /home/developer


