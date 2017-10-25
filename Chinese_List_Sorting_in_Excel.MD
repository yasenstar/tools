# How to Manage the Customized Sorting of Chinese Language List in Microsoft Product (Excel, SQL, etc.)

Microsoft product family relating to spreadsheet treatment, e.g. Excel, SQL DB, (possible including Access), are dealing with data list, so it's important to understand how the sorting rules applying to the data list.

In English language, by default, there're A-Z and Z-A methods, for sorting via comparing from the first character, in case same, then second character, etc.., till the end of the word (or full data phrase in the cell).

Adding double-bytes language, it's becoming complicated, this file intends to document how the sorting applys to Chinese words in the data list.

Using below table as example, be noticed, there's PinYin used by Chinese to indicate the pronounciation of Chinese character.
*From [here in wikipedia](https://en.wikipedia.org/wiki/Pinyin) you can learn information about Chinese PinYin.*

|中文名称（Chinese Name）|拼音名称（Chinese PinYin）|英文名称（English Name）|
|-----------------------|-----------------------:| :--------------------:|
|卡车 |kache |truck |
|客车 |keche |bus |
|工程机械 |gongchengjixie |construction equipment|

(currently it's no specific order)

If we sort by A-Z in English Name column, it's naturally getting as below:

|中文名称（Chinese Name）|拼音名称（Chinese PinYin）|英文名称（English Name）*(A-Z)*|
|-----------------------|-----------------------:| :--------------------:|
|客车 |keche |bus |
|工程机械 |gongchengjixie |construction equipment|
|卡车 |kache |truck |

If we sort by A-Z in Chinese PinYin, the same rule about applies, just that will based on the alphabet order in PinYin

|中文名称（Chinese Name）|拼音名称（Chinese PinYin）*(A-Z)*|英文名称（English Name）|
|-----------------------|-----------------------:| :--------------------:|
|客车 |keche |bus |
|卡车 |kache |truck |
|工程机械 |gongchengjixie |construction equipment|

Now coming to Chinese Name column, **the default rule *(from Microsoft)* for Chinese words sorting is based on their Pinyin's A-Z or Z-A**, with this in mind, if we just choose A-Z, you get same as above Pinyin, let's try Z-A for Chinese Name column, you get below:

|中文名称（Chinese Name）*Z-A*|拼音名称（Chinese PinYin）|英文名称（English Name）|
|-----------------------|-----------------------:| :--------------------:|
|工程机械 |gongchengjixie  **???** |construction equipment|
|卡车 |kache |truck |
|客车 |keche |bus |

*but here I don't understand why g and k's order is not correct!*

Anyway, this is not the understandable sorting result, but the 

![Create Customized Sorting Rule in Excel](/pics/customized_sorting_in_excel.jpg)
