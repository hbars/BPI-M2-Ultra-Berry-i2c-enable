# BPI-M2-Ultra-Berry-i2c-enable

1. Compile.* dts files.
dtc -I dts -O dtb v40-bananapi-m2-berry-i2c-0.dts -o v40-bananapi-m2-berry-i2c-0.dtbo
dtc -I dts -O dtb v40-bananapi-m2-berry-i2c-1.dts -o v40-bananapi-m2-berry-i2c-1.dtbo
dtc -I dts -O dtb v40-bananapi-m2-berry-i2c-2.dts -o v40-bananapi-m2-berry-i2c-2.dtbo

2. Copy
cp *.dtbo /boot/overlay-user

3. Add or edit the line:
user_overlays=v40-bananapi-m2-berry-i2c-1 v40-bananapi-m2-berry-i2c-2
in /boot/armbianEnv.txt

4. Do not enable any i2c ports in armbian-config.

5. Reboot and check with:
i2cdetect -y 2
i2cdetect -y 3

Injoy.
