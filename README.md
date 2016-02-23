# gimp-batch-watermark
Batch watermark utility for Gimp 2.x. Add a jpg/gif watermark (PNG not supported) to an entire directory of files.

Install/Prepare to Run
-------

0. Download migee.scm to your GIMP install followed by \share\gimp\2.0\scripts. GIMP is often found under Program Files for Windows users.
0. Prepare to run this script from command line. For Windows users Start -> Run… -> Cmd (hit OK).
0. Type cd followed by your GIMP directory (i.e. cd “C:\Program Files\GIMP 2\bin”)

Parameters
-----
* Watermark Path – Path to a watermark in XCF (GIMP) format. Other formats may work as well.
* Input files – Path to directory, followed by a wildcard search (i.e. *.jpg to target all jpg images to be watermarked).
* Watermark Size – How big your watermark will be in accordance to the image. This is a percent but is entered as a decimal such as .05 (5%).
* Watermark Padding – Each watermark will be padded from the corners of the image by a percentage (of the entire image) you define. This is a percent but is entered as a decimal as well.
* Watermark Layer Mode – leave this as 0 (zero). higher numbers (i.e. 1,2,3…) will enable a different layer mode such as lighten/hard light/etc.
* Position Number – My script allows for the watermark to be aligned in any corner, or the center. Acceptable values are 1,2,3,4,5.
* Output Path – Where the watermarked images will be saved to.

Usage
-----

```
gimp-2.8.exe -b "(migee-add-watermark watermark-path inputfiles watermark-size watermark-padding watermark-layer-mode position output-dir)
```

Example
-----
```
gimp-2.8.exe -b "(migee-add-watermark \"C:\\Users\\Migee\\Desktop\\WatermarkTest\\watermark.xcf\" \"C:\\Users\\Migee\\Desktop\\WatermarkTest\\*.jpg\" .25 .01 15 5 \"C:\\Users\\Migee\\Desktop\\WatermarkTest\")"
```
