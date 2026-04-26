
<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="LOGO/black.png">
  <source media="(prefers-color-scheme: light)" srcset="LOGO/white.png">
  <img alt="SAIL THE PROTOTYPE LOGO" src="URL_TO_BLACK_IMAGE">
</picture>
 </p>

<h3 align="center"><strong>SAIL THE PROTOTYPE Project Repository</strong></h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Open Source](https://img.shields.io/badge/Open%20Source-%E2%9D%A4-brightgreen)

</div>

---


**SAIL The Prototype** is a [DMP](https://en.wikipedia.org/wiki/Digital_media_player), an open-source project that plans to be a startup. This is not a basic digital media player, but also a multi-tool. It has 433MHZ CC1101, [Infrared LED](https://www.lcsc.com/product-detail/C18199783.html), and NFC functions(13.56MHZ). 
The STM32H723 is a powerful MCU for that project, I would say even an overkill. More about the PCBs, there are 3PCBs. Why 3 PCBs? One is the main board, with STM32, ESP32, Display and user input devices, second one is NFC Board I would call. This board contains NFC as you can tell from the name, CC1101(433MHZ only), and magnetic pogo pin connectors.


|*MAIN Board* Top Component Layer                                                                                                                 |*MAIN Board* Bottom Component Layer                                                                                                              |  
|  :---                                                                                                                              |   :---                                                                                                                              |
|<img width="732" height="1012" alt="image" src="https://github.com/user-attachments/assets/6910aecf-bcad-42f6-b1f6-671b1048c61b" /> | <img width="754" height="1000" alt="image" src="https://github.com/user-attachments/assets/9ee13938-8767-4893-b497-99480a05d921" /> |

---


| **Feature**                    | **Details**                                                                                                                                          |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Main MCU**                       | STM32H723 as a main MCU that does all the work                                   |
| **Secondary MCU**                  | ESP32-WROVER-IE(16MB) for BlueTooth headphones and pogo pin connectors(IOs)                                                                                             |
| **2.4" IPS TFT Display**           | 2.4" IPS Display connected via FPC, 8080 16-bit protocol. [BuyDisplay](https://www.buydisplay.com/2-4-inch-ips-240x320-tft-lcd-display-capacitive-touch-screen)                               |
| **Multi-Tool features**            | [NFC Module](https://www.lcsc.com/product-detail/C5267436.html)                |
| **RTC Battery**                    | BS-CR2032-8 battery slot for [RTC functionality](https://www.lcsc.com/product-detail/C9866.html).                        |
|	~~**Metal Body**~~                 | ~~Aluminium front and back plate; 3D-printed middle section~~                                                                                               |
| **Power and file transmitting**    | USB-C Port which allows data-stream and powering. [USB3300](https://www.lcsc.com/product-detail/C108954.html) for fast file transmitting(50MB/S)                                                                                                                                       |
| **Battery Type**             | 2500mAh Li-Ion battery, 103450, [Aliexpress](https://www.aliexpress.com/item/1005008825499071.html?spm=a2g0o.detail.pcDetailTopMoreOtherSeller.1.51ffSwlrSwlrjB&gps-id=pcDetailTopMoreOtherSeller&scm=1007.40050.354490.0&scm_id=1007.40050.354490.0&scm-url=1007.40050.354490.0&pvid=2d759c26-5379-4d10-b826-4eb722d78d08&_t=gps-id%3ApcDetailTopMoreOtherSeller%2Cscm-url%3A1007.40050.354490.0%2Cpvid%3A2d759c26-5379-4d10-b826-4eb722d78d08%2Ctpp_buckets%3A668%232846%238108%231977&pdp_ext_f=%7B%22order%22%3A%22495%22%2C%22eval%22%3A%221%22%2C%22sceneId%22%3A%2230050%22%2C%22fromPage%22%3A%22recommend%22%7D&pdp_npi=6%40dis%21USD%2110.49%216.29%21%21%2171.38%2142.83%21%40211b65de17772217116784494e6405%2112000046836099274%21rec%21UA%216416141679%21XZ%211%210%21n_tag%3A-29919%3Bd%3Abd2102de%3Bm03_new_user%3A-29895&utparam-url=scene%3ApcDetailTopMoreOtherSeller%7Cquery_from%3A%7Cx_object_id%3A1005008825499071%7C_p_origin_prod%3A)                                         |
| **Battery Life**             | ~8 hours idle, 4-5 hours typical usage                                                                                                                 |
| **Battery Voltage Measurement** | ADC Technology, connected to pin PA0 of STM32H7        |
| **Magnet on Back Plate of NFC Board(Pogo pins)**     | [4x 4-Pin Pogo pin connector](https://www.lcsc.com/product-detail/C5126844.html) is a female version. For a breakout board you would need this [magnetic connector](https://www.lcsc.com/product-detail/C5126845.html?s_z=n_q_YZP0048-20048-04025-03&spm=wm.ssy.bg.0.xh&lcsc_vid=RwRWBFMFT1dZU1UCRVJcX11STgVXUVICQwBZVwYFRQAxVlNRQFNcVVRTRlhWUzsOAxUeFF5JWBYZEEoKFBINSQcJGk4eFQsCAgIaSgADAwAHC0slQlBcUVxSQ08GEwkK)  |
| **Audio components**               | [PCM5102APWR](https://www.lcsc.com/product-detail/C107671.html) as a DAC, [TPA6132A2RTER](https://www.lcsc.com/product-detail/C69901.html) as a AMP and a [PJ-327A 5JJ](https://www.lcsc.com/product-detail/C668605.html?s_z=n_q_PJ-327A%25205JJ&spm=wm.ssy.bg.0.xh&lcsc_vid=RgReVVxRRFgLUlFfQlJXAVEAFVhaX1EDT1YIBQVVQlYxVlNRQFNcVVZTRlFdUTsOAxUeFF5JWBYZEEoKFBINSQcJGk4eFQsCAgIaSgADAwAHC0slQVhXV1VIHxUDCw%3D%3D) as a jack 3.5mm connector for headphones.           |  
