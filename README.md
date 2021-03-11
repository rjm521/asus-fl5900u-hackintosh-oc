# asus-fl5900u-hackintosh-oc



## OpenCore Version

- 0.66

## MAC OS Version

- Big Sur 11.2

## For Debug

- For debug mode: please add `-v` to  `boot-args`

## Note

Please use SSDTTime to patch your own SSDT, do not use mine as not all the configuration work the same on your device.

You can only dump SSDT on Windows or Linux

Please downgrade your bios if you're at version 3.1.1. （As my bios version is 3.1.1，and it works）

Please generate your own SMBIOS SN, UUID using MacBookPro14,1 and change your ROM based on your Ethernet Mac Address.



## Laptop Specifications

| Name              | Specifications                                               |
| ----------------- | ------------------------------------------------------------ |
| Processor         | Intel Core i7 - 7500u                                        |
| Memory            | 1x 4 GB DDR4 2133 Mhz + 1x 8 GB DDR4 2133 Mhz                |
| Storage           | SSD 128G + HDD 1T                                            |
| Video             | Integrated Intel HD 620 + NVIDIA 940MX                       |
| Wi-Fi + Bluetooth | Qualcomm Atheros 9565                                    |
| Ethernet          | Realtek RTL8111                                              |
| Audio             | Realtek ALC255                                               |
| Touchpad          | ELAN 1000 I2C Interface                                      |
| Screen Size       | 15,6 Inch                                                    |
| Screen Resolution | 1920 x 1080                                                  |
| Others            | 1x Card Reader, 1x WebCam, 1x VGA Port, 1x HDMI, 1x Combo Audio Jack, 1x USB 2.0, 1x USB 3.0 Type A, 1x USB 3.0 Type C, 1x Optical Drive |

For more details about my laptop, please see `laptop-config-list.txt` file in this repo.



## What Works 


✅ Intel HD 620

✅ All USB Type A ports

✅ USB type C port

✅ Keyboard

✅ Touchpad

✅ Internal screen backlight change

✅ Wi-Fi

✅ UVC HD Webcam

✅ Speaker

✅ Laptop lid

✅ Native power managment

✅ Battery status

✅ ️Sleep

✅ Bluetooth

✅ IServices (IMessage, FaceTime, ICloud) (Make sure you set your own SMbios and generate your own Serial Number using GenSMBIOS)

✅ Onboard Ethernet

⚠️ FN Keys (Volume Control, Sleep works)

⚠️ SD Card (Not Tested)

✅ VGA/HDMI (Audio + Video)

❌ Realtek SD card reader

❌ NVIDIA GeForce 940MX (Optimus - impossible to get working at the moment)



## Notice



If want your `AR9565 Wireles Card` work, you should：

-  Step1: add  `AirPortAtheros40.kext` and `HS80211Family.kext` to your `EFI/OC/Kexts`directory.

- Step2: modify `config.plist` add `AirPortAtheros40.kext` and `HS80211Family.kext` and keep the load order correct.

  

![order.img](/Users/rjm/repo/asus-fl5900u-hackintosh-oc/config-order.png)



## Contact

- 1824793405@qq.com



## Thanks

- This EFI is based on [firmanjamal](https://github.com/firmanjml/Asus-X556UQK-Hackintosh-OC) 's repo. I just modified some stuff and let it worked for my laptop. If your laptop is similar to mine, hopefully it work for you too. 

