---
layout: default
---

# SVG To CSV Datasource Converter
<!--
SvgToFloorMapDataSourceConverter: C:\Users\MB\source\repos\draaijerpartners\DECManager\SvgToFloorMapDataSourceConverter\publish
-->
&nbsp;

[Download &#x2b73;](../download/SvgToFloorMapDataSourceConverter.exe)

Click 'Download' to download a command-line tool that is capable of parsing a \*.svg file or a folder containing \*.svg files and converting its contents into a datasource for the [FloorMap Visual](../floormap/floormap.md).

&nbsp;

## Instructions

### Usage

Command prompt syntax:

```c#
C:\Path_To_Install_Directory\SvgToFloorMapDataSourceConverter [command] [options]
```

|Commands||
|-|-|
|&emsp;**convert**|*Convert one or more \*.svg files to a FloorMap Visual datasource.*|
|&emsp;**--help, -h, -?**|*Display general help information.*|
|&emsp;**convert --help**|*Display help information for the convert command.*|
|||

|Options||
|-|-|
|&emsp;**--file, -f**|*Full path to the file that must be converted.*|
|&emsp;**--dir, -d**|*Full path to the directory that contains the files to be converted.*|
|&emsp;**--out, -o**|*Full path to the directory in which generated output will be stored.*|
|&emsp;**--url, -u**|*The base url to use when inserting urls.*|
|&emsp;**--embed, -e**|*Determines whether to insert a url placeholder or insert embedded image data in the ImageData field.*|
|||

#### Notes

- The prompt must contain either one **--file** option ór one **--dir** option, not both or multiple **--file** or **--dir** options.
- When using the **--dir** option, nested directories and non-svg files are ignored.
- If the **--out** option is omitted, the directory of the source (specified with **--file** or **--dir**) is used.
- If not embedding images (i.e. the **--embed** option is omitted), the **--url** option is mandatory. The provided url must be a valid url (i.e. must start with either `'http:\\'` or `'https:\\'` and must contain a valid domain extension, like `'.org'` or `'.nl'`)
- The **--embed** option defaults to `false`, so only needs to be used when embedding images

#### Examples

```c#
// convert file 'test.svg'
// create an image url that will result in 'https:\\mydomain.com\floormap\floors\*id*.svg'
// output results to 'C:\Users\xxx\FloorMapVisual\Datasources'

C:\SvgConverter\SvgToFloorMapDataSourceConverter convert --file "C:\Users\xxx\FloorMapVisual\Resources\test.svg" --out "C:\Users\xxx\FloorMapVisual\Datasources" -url "https:\\mydomain.com\floormap\floors"

// convert directory 'C:\Users\xxx\FloorMapVisual\Resources'
// embed images
// output results to same directory ('C:\Users\xxx\FloorMapVisual\Resources')

C:\SvgConverter\SvgToFloorMapDataSourceConverter convert --dir "C:\\Users\\xxx\\FloorMapVisual\Resources" --embed
```

&nbsp;

## Data source lay-out

boohoo

&nbsp;

[Download &#x2b73;](../download/SvgToFloorMapDataSourceConverter.exe)
