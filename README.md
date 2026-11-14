# wmt_eink_study
[WIP] My E-ink study

## Ref
* https://github.com/Luoyacheng/legado-E  
from https://www.bilibili.com/video/BV1BP846JE1W/  
* https://github.com/onyx-intl/OnyxAndroidDemo
* https://github.com/karino2/PngNote
* https://github.com/weimingtom/PngNoteMod
* https://github.com/foobnix/LibreraReader
* https://github.com/onyx-intl/boox-opensource
* https://github.com/geometer/FBReader-Android-2
* https://github.com/lurongshuang/FBReader-Mupdf_library

## ESP32
* https://crosspointreader.com/install

* https://freeink.org/

* (IMP?) https://github.com/atomic14/diy-esp32-epub-reader  
(IMP?) https://github.com/abirw/diy-esp32-epub-reader-m5papers3  

* (IMP?) https://github.com/mikaryyn/EPub-M5Stack-Paper-S3  
freetype build:  
https://github.com/turgu1/EPub-InkPlate/issues/2   
https://github.com/turgu1/EPub-InkPlate#freetype-library-compilation-for-esp32  
```
ESP32墨水屏研究。我现在可以用esp-idf 5.5编译m5stack papers3的代码
mikaryyn/EPub-M5Stack-Paper-S3。方法是
（1）pio没有main模块，你需要创建一个main目录，然后复制src下的CMakeList.txt进去修改
（2）你需要在CMakeList.txt中指定所有源代码，包括库（你可以认为pio相当于一个没有components的最小esp-idf项目）
（3）加上缺少的宏定义和头文件目录，参考platformio.ini里面关于papers3的宏
（4）复制sdkconfig.paper_s3到sdkconfig，并且menuconfig设置partitions.csv分区，否则会用默认的分区导致flash不够
（5）一个棘手的地方是编译freetype，我直接搬用了turgu1/EPub-InkPlate里面的freetype组件
```

* (IMP?) https://github.com/MoveCall/crosspoint-onepage     
https://github.com/MoveCall/onepage-reader   
https://github.com/MoveCall/crosspoint-onepage/tree/16477d0c2f0b8f2839b1340098f3fe2c2c434878      
https://oshwhub.com/movecall/project_ucjwpaya  

* https://docs.waveshare.net/ESP32-S3-ePaper-3.97/Firmware-Flashing  
(IMP) https://docs.waveshare.net/ESP32-S3-ePaper-3.97/ESP-IDF/#示例-08_ESP32-S3_e-Paper-3.97    
ESP32-S3_ePaper-3.97-demo.zip   
(IMP) https://github.com/waveshareteam/ESP32-S3-ePaper-3.97      
```
除了自己用AI生成以外，目前已知最容易编译的墨水屏代码是waveshareteam/ESP32-S3-ePaper-3.97，
用esp-idf 5.5可以轻松编译。
然后我现在是研究m5stack papers3的mikaryyn/EPub-M5Stack-Paper-S3，这个就上难度了，
如果要把这个pio（platformio）工程搬到esp-idf中编译，需要改代码，
我试试能不能搞出来，理论上应该是可以的
```

* https://cursedhardware.github.io/awesome-embedded-display/epd.html

* https://www.bilibili.com/video/BV1Zu4y1H7oA/

* https://crossmux.com  
https://github.com/0x1abin/crossmux  
https://post.smzdm.com/p/ak8xoprk/  

* (IMP???) https://github.com/CloudZao/Metalio-E-INK4    
无名科技, Metalio E-INK4 Plus 4.7英寸墨水屏阅读器  
Metalio E-INK4 3.97英寸墨水屏阅读器  
https://metalio.world  
https://github.com/CloudZao/Metalio-E-INK4-Plus
```
ESP32墨水屏研究。上次我说编译不了的那个CloudZao/Metalio-E-INK4，我可以编译出来了，
需要在idf.py build前执行pip install qoi-conv。
无名科技的Metalio E-INK 4 3.97寸墨水屏我先试试买来看能不能跑，
因为不是很贵，属于可以接收的范围 ​​​
```

* https://github.com/Lakphy/eego-a4-template-firmware

* https://github.com/Seeed-Projects/reterminal-sticky-playground-registry

* https://crosslink-reader.top

* https://github.com/Free-Ink/freeink-sdk

* https://freeink.org/

* https://crosspointreader.com/

* https://github.com/crosspoint-reader/Murphy/tree/main

* https://xteink-flasher-cjk.vercel.app  
https://github.com/CrossPoint-CJK/crosspoint-reader-cjk  
