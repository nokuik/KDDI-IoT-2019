# KDDI-IoT-2019

## Dataset Description

The KDDI-IoT-2019 dataset is a set of IPFIX records from 25 different IoT devices. 
if you use the dataset, you must agree to the terms of dataset license below.

### Overview

The KDDI-IoT-2019 dataset contains ZIP files for each device in the ipfix directory.
IoT devices are listed in the table below. 
Extracting the GZ file outputs a JSON file that contains IPFIX records. (Some GZ files are split.) 
We generated IPFIX records by YAF[^1] from PCAP files and converted IPFIX binary to JSON file by Super Mediator[^2]. We used the following commands.

1. PCAP to IPFIX binary
    ```
    yaf --in "input file" --out "output file" --flow-stats --mac 
    ```
2. IPFIX binary to IPFIX JSON file
    ```
    super_mediator --in "input file" --out "output file" --output-mode json
    ```

[^1]: YAF: https://tools.netsa.cert.org/yaf/index.html
[^2]: Super Mediator: https://tools.netsa.cert.org/super_mediator/index.html

### Dataset Speficication

#### IoT devices

| Device                                | Category           | Mac Address       | IPFIX Records |
| ------------------------------------- | ------------------ | ----------------- | ------------: |
| Amazon Echo gen2                      | Smart speaker      | 4c:ef:c0:17:e0:42 | 534,289       |
| au network camera                     | Network camera     | ec:3d:fd:39:6f:98 | 175,794       |
| au wireless adapter                   | IoT gateway/hub    | b0:ea:bc:ea:ac:86 | 735,225       |
| Bitfinder Awair Breathe Easy          | Environment sensor | 70:88:6b:10:22:83 | 396,706       |
| CANDY HOUSE Sesami Wi-Fi access point | Door lock          | 38:56:10:00:1d:8c | 259,873       |
| Google Home gen1                      | Smart speaker      | 48:d6:d5:92:96:a2 | 6,142,846     |
| I-O Data QWatch                       | Network camera     | 34:76:c5:7f:91:07 | 2,167,558     |
| iRobot Roomba                         | Robot cleaner      | 40:9f:38:e7:7f:09 | 132,297       |
| JVC Kenwood CU-HB1                    | IoT gateway/hub    | 00:a2:b2:b9:09:87 | 1,323,485     |
| JVC Kenwood HDTV IP camera            | Network camera     | e0:b9:4d:5c:cf:c5 | 144,955       |
| Line Clova Wave                       | Smart speaker      | a8:1e:84:e8:cc:c3 | 311,199       |
| Link Japan eRemote                    | Remote controller  | 34:ea:34:76:ea:68 | 438,959       |
| Mouse computer room hub               | IoT gateway/hub    | aa:1e:84:06:1c:b4 | 16,932        |
| Nature Remo                           | Remote controller  | 60:01:94:54:6b:e8 | 126,048       |
| Panasonic Doorphone                   | Doorphone          | bc:c3:42:dc:24:78 | 1,344,464     |
| Philips Hue Bridge                    | Light              | 00:17:88:47:20:f2 | 438,573       |
| PLANEX camera one shot!               | Network camera     | 00:1b:c7:fa:c3:e6 | 1,471,465     |
| PLANEX SmaCam Outdoor                 | Network camera     | 00:22:cf:fd:c1:08 | 188,230       |
| PLANEX SmaCam PanTilt                 | Network camera     | e0:b9:4d:b9:eb:e9 | 140,445       |
| PowerElectric Wi-Fi plug              | Plug               | ec:f0:0e:55:25:39 | 359,065       |
| Qrio Hub                              | Door lock          | 80:c5:f2:0b:aa:a9 | 166,061       |
| Sony Bravia                           | TV                 | 04:5d:4b:a4:d0:2e | 3,403,273     |
| Sony network camera                   | Network camera     | 70:26:05:73:6e:31 | 144,236       |
| Sony smart speaker                    | Smart speaker      | 6c:5a:b5:56:39:3e | 2,398,172     |
| Xiaomi Mijia LED                      | Light              | 78:11:dc:55:76:4c | 128,968       |

- Mini Smart Lock (Door lock) was connected to CANDY HOUSE Sesami Wi-Fi acccess point.
- Qrio Lock (Door lock) was connected to Qrio Hub.
- Phillips Hue Light was connected to Philips Hue Bridge.

#### Dataset period

6/25/2019 - 10/10/2019 (108 days)



## LICENSE AGREEMENT for DATASETS

The following terms comprise the License Agreement for Datasets (the “License Agreement”) made available by the KDDI Research, Inc. (KDDI Research).

### LICENSE

KDDI Research’s authorization to access the data grants you a limited, non-exclusive, non-transferable, non-assignable, and terminable license to copy, modify, and use the data in accordance with this License Agreement. No license is granted for any other purpose and there are no implied licenses in this License Agreement. Nothing in this License is intended to limit any rights You may have arising from fair use or due to other limitations on KDDI Research’s exclusive rights under copyright law or other applicable laws. You will not disclose the dataset to any other person other than those employed by your institute or organization who are collaborating with you using the dataset. KDDI Research has the authority and reserves the right, in its sole discretion, to discontinue further access and use to anyone who violates this License Agreement.
If you create a publication (including web pages, papers published by a third party, and publicly available presentations) using data from this dataset, you should cite our paper as follows:

- Title: Identification of an IoT Device Model in the Home Domain Using IPFIX Records
- Authors: Norihiro Okui, Masataka Nakahara, Yutaka Miyake, Ayumu Kubota
- Venue:  IEEE Computer Society Signature Conference on Computers, Software and Applications (COMPSAC) 2022

### DISCLAIMER OF WARRANTIES
KDDI Research USES ITS BEST EFFORTS TO PROVIDE DATA IN ACCORDANCE WITH ETHICAL PRINCIPLES AND SCIENTIFIC INTEGRITY. HOWEVER, THE DATA PROVIDED HEREIN IS ON AN “AS IS” BASIS. NEITHER KDDI Research, ITS RESEARCHERS, RESEARCH PARTNERS, LICENSORS, AND DATA PROVIDERS, NOR KDDI Research’s PARENT COMPANY AND ITS OFFICERS, EMPLOYEES, AND AGENTS MAKE ANY WARRANTY, EITHER IMPLIED OR EXPRESS, OF MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE, INCLUDING, BUT NOT LIMITED TO, THE ACCURACY, TIMELINESS, COMPLETENESS, RELIABILITY, OR AVAILABILITY OF KDDI Research DATA, APPLICATIONS, OR SERVICES ACCESSIBLE THROUGH OR MADE AVAILABLE BY KDDI Research.

### LIMITATION OF LIABILITY
TO THE EXTENT ALLOWED BY LAW, IN NO EVENT SHALL KDDI Research AND ITS PARENT COMPANY BE LIABLE TO YOU OR ANY THIRD PARTY FOR ANY INDIRECT, CONSEQUENTIAL, INCIDENTAL, SPECIAL OR PUNITIVE DAMAGES, ARISING FROM YOUR USE OF THE DATA.
