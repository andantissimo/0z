# 0-zip

converts and/or extracts data in *.pdf, *.rar or *.zip to a noncompressed zip archive.

<table>
<tr>
  <th>Format</th>
  <th>Records</th>
  <th>Order By</th>
</tr>
<tr>
  <td>PDF</td>
  <td>Embedded JPEGs, <s>Texts</s>, <s>Primitives</s></td>
  <td>Occurrence order</td>
</tr>
<tr>
  <td>RAR</td>
  <td rowspan="2">Non-protected entries</td>
  <td rowspan="2">Natural sort order</td>
</tr>
<tr>
  <td>ZIP</td>
</tr>
</table>

## Runtime Dependencies
* [UnRAR](https://www.rarlab.com/rar_add.htm) (Optional)

## Build Instructions

### Windows Development
* Visual Studio 2019+
  * Windows Universal CRT
* VCpkg
  * boost-crc:x64-windows-static
  * boost-interprocess:x64-windows-static
  * boost-locale:x64-windows-static
  * boost-program-options:x64-windows-static

### Build and Installation
1. open `msvc/0-zip.sln`
2. build `Release|x64`
3. copy `msvc/bin/x64/Release/0z.exe` to wherever you want

### Generic Development
* CMake 3.1+
* Clang 6.0+ or GCC 7.0+ or Xcode 10.0+
* Boost 1.66+ (boost-locale, boost-program-options)

### Build and Installation
```sh
$ mkdir build
$ cd build
$ cmake -DCMAKE_BUILD_TYPE=Release ..
$ make
$ sudo make install
```
