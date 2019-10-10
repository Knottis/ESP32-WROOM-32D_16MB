# ESP32-WROOM-32D 16MB
#### How to take advantage on the 16MB Flash with the Arduino IDE on the ESP32-WROOM-32D 16MB

ESP32-WROOM-32D 16MB Flash Memory Wi-Fi+BT+BLE ESP32 Module Espressif

![alt text](https://github.com/Knottis/ESP32-WROOM-32D_16MB/blob/master/Arduino_IDE_16MB.png "Arduino IDE")

https://www.aliexpress.com/item/33058728181.html?spm=a2g0o.productlist.0.0.491c7dd1rx2THI&algo_pvid=2799c7c0-98af-443c-8d42-1e27a715c0b7&algo_expid=2799c7c0-98af-443c-8d42-1e27a715c0b7-2&btsid=cbf62f6b-63e6-4825-90da-d31621b76eda&ws_ab_test=searchweb0_0,searchweb201602_3,searchweb201603_60

![alt text](https://github.com/Knottis/ESP32-WROOM-32D_16MB/blob/master/ESP32-WROOM-32D-16MB.png "ESP32-WROOM-32D 16MB")

### You need to make some minor changes to the BOARDS.TXT file that you find here in Windows-10.

C:\Users\XXXX\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.4\boards.txt

### 1. Change to these values WHEN USE OF THE ESP32 - 16MB FLACH

esp32.upload.maximum_size=6553600
esp32.upload.maximum_data_size=4521984


### 2. Insert this after the last:   esp32.menu.PartitionScheme


esp32.menu.PartitionScheme.large_spiffs=16MB Flash (4.5MB APP, OTA, 7MB SPIFFS)
esp32.menu.PartitionScheme.large_spiffs.build.partitions=User1_large_spiffs_16MB
esp32.menu.PartitionScheme.large_spiffs.upload.maximum_size=4685824
esp32.menu.PartitionScheme.large_app_user2=16MB Flash (6.5MB APP, OTA, 3.6MB SPIFFS)
esp32.menu.PartitionScheme.large_app_user2.build.partitions=User2_large_app_16MB


### 3. Then copy these two files to this location:

C:\Users\XXXX\AppData\Local\Arduino15\packages\esp32\hardware\esp32\1.0.4\tools\partitions

User1_large_spiffs_16MB.csv

User2_large_app_16MB.csv


# Special thanks to M5Stack Fire support. 
### The original article this is based on can be found here:
HOWTO: M5Stack Fire - use the full 16MB with the Arduino IDE (UPDATED)

http://forum.m5stack.com/topic/364/howto-m5stack-fire-use-the-full-16mb-with-the-arduino-ide-updated
