# Xiangyin Chinese Dialect Dataset

## Data

The voice data of Xiangyin Chinese Dialect Dataset comes from the voice uploaded by users of [XiangYin.Mobi](https://xiangyin.mobi). At this stage, it is released under the [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/) agreement (not for commercial use, derivatives must also use the same agreement, please keep all information and GitHub page links for reprinting). If you have commercial needs, please contact webmaster@xiangyin.mobi.

The v1 data contains the voice of reading sentences uploaded by users from 2015 to September 2024 (with some filtering), which has been processed by VAD to reduce silence time, totaling about 81 hours and 7719 speakers. It includes the number of votes, but does not include user mutual verification data, and is released in ogg format. The sampling rate depends on the user device, usually 16kHz or 44.1kHz.

Please contact us by email to obtain data and briefly explain the purpose. If you have any questions or suggestions, please raise an issue or send an email for discussion.

Reference link:

```
@misc{xiangyin24,
author = {Xing Chen},
title = {The XiangYin Chinese Dialect Dataset},
howpublished = {\url{https://github.com/cxcxcxcx/xiangyin_dataset}},
year = 2024
}
```

Data verification:

```
$ sha256sum xiangyin_dataset_v1_20240928.tar
749ff4f8d3f2f6d2b34031c213a457f1d3429530ea7d0659d7c6e7aa7af4a12b xiangyin_dataset_v1_20240928.tar
```

## Data format
### Metadata.CSV

| Column name | Data type | Description |
|---|---|---|
| id | integer | unique identifier of the voice sample |
| sound_length | floating point number | duration of the voice sample (seconds) |
| votes | integer | number of votes the voice sample received |
| full_url | string | full URL of the voice sample on the Xiangyin web version (https://web.xiangyin.mobi) |
| date | date | month the voice sample was uploaded |
| same_text | string | user input: description of whether the voice sample matches the text |
| uploader_id | integer | user ID of the uploader |
| uploader.gender | string | user input: gender of the uploader |
| uploader.birth_year | floating point number | user input: year of birth of the uploader (accurate to 10 years) |
| dialect.province | string | user input: province of the voice sample |
| dialect.city | string | user input: city of the voice sample |
| dialect.name | string | short name of the combination of province and city |
| dialect.location_json.lat | floating point number | User input: latitude of the place where the voice sample was collected (accuracy 0.1 degree) |
| dialect.location_json.lng | floating point number | User input: longitude of the place where the voice sample was collected (accuracy 0.1 degree) |
| dialect.is_living | Boolean value | User input: whether the uploader lived in the place when uploading |
| dialect.is_hometown | Boolean value | User input: whether the uploader grew up in the place |
| sentence.source.type | string | type of sentence source (e.g. daily language, poetry) |
| sentence.source.name | string | specific name of the sentence source (e.g. "Humble House Inscription") |
| sentence.text | string | text content corresponding to the voice sample |
| sentence.id | floating point number | sentence ID |

## Data Overview

Number of voices divided by provincial administrative regions

| Provincial administrative regions | Number of voices | Number of users |
|---|---|---|
| Guangdong | 3001 | 746 |
| Jiangsu | 1948 | 542 |
| Hunan | 1823 | 530 |
| Henan | 1676 | 543 |
| Zhejiang | 1612 | 441 |
| Hubei | 1488 | 377 |
| Sichuan | 1450 | 523 |
| Fujian | 1398 | 359 |
| Shandong | 1372 | 468 |
| Jiangxi | 1324 | 351 |
| Anhui | 1130 | 350 |
| Hebei | 939 | 278 |
| Shaanxi | 933 | 296 |
| Shanxi  | 727 | 231 |
| Chongqing | 660 | 218 |
| Guangxi | 640 | 213 |
| Guizhou  | 519 | 141 |
| Liaoning  | 497 | 174 |
| Yunnan  | 463 | 134 |
| Shanghai | 439 | 116 |
| Beijing | 408 | 124 |
| Gansu  | 360 | 129 |
| Heilongjiang  | 347 | 138 |
| Jilin  | 280 | 93 |
| Taiwan | 272 | 21 |
| Inner Mongolia  | 230 | 73 |
| Tianjin | 224 | 72 |
| Taiwan  | 177 | 30 |
| Hong Kong | 153 | 45 |
| Hainan  | 145 | 52 |
| Xinjiang  | 132 | 47 |
| Ningxia  | 71 | 31 |
| Qinghai  | 50 | 23 |
| Tibet | 10 | 7 |

#### Gender

| Gender | Number of voices | Number of users |
|---|---|---|
| Male | 16608 | 4416 |
| Female | 8034 | 2579 |

#### Year of birth

| Year of birth | Number of voices | Number of users |
|---|---|---|
| 1990.0 | 12426 | 3372 |
| 2000.0 | 8675 | 2554 |
| 1980.0 | 3672 | 943 |
| 1970.0 | 719 | 230 |
| 2010.0 | 668 | 210 | 
| 1910.0 | 225 | 91 |
| 1960.0 | 195 | 76 | 
| 1940.0 | 114 | 60 | 
| 1950.0 | 114 | 61 |
| 1930.0 | 111 | 42 | 
| 2020.0 | 92 | 27 | | 1920.0 | 72 | 35 |
