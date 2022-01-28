WebP ファイルをイメージ ファイルに解凍する
.webp --> .png

dwebp picture.webp -o output.png

https://developers.google.com/speed/webp/docs/dwebp

Decoding tool:
==============

The sample decoding program dwebp will take
a .webp file and decode it to a PNG image file (amongst other formats).
This is simply to demonstrate the use of the API. You can verify the
file test.webp decodes to exactly the same as test_ref.ppm by using:

 dwebp test.webp -ppm -o test.ppm
 diff test.ppm test_ref.ppm

The full list of options is available using -h:

> dwebp -h
Usage: dwebp in_file [options] [-o out_file]

Decodes the WebP image file to PNG format [Default].
Note: Animated WebP files are not supported.

Use following options to convert into alternate image formats:
  -pam ......... save the raw RGBA samples as a color PAM
  -ppm ......... save the raw RGB samples as a color PPM
  -bmp ......... save as uncompressed BMP format
  -tiff ........ save as uncompressed TIFF format
  -pgm ......... save the raw YUV samples as a grayscale PGM
                 file with IMC4 layout
  -yuv ......... save the raw YUV samples in flat layout

 Other options are:
  -version ..... print version number and exit
  -nofancy ..... don't use the fancy YUV420 upscaler
  -nofilter .... disable in-loop filtering
  -nodither .... disable dithering
  -dither <d> .. dithering strength (in 0..100)
  -alpha_dither  use alpha-plane dithering if needed
  -mt .......... use multi-threading
  -crop <x> <y> <w> <h> ... crop output with the given rectangle
  -resize <w> <h> ......... scale the output (*after* any cropping)
  -flip ........ flip the output vertically
  -alpha ....... only save the alpha plane
  -incremental . use incremental decoding (useful for tests)
  -h ........... this help message
  -v ........... verbose (e.g. print encoding/decoding times)
  -quiet ....... quiet mode, don't print anything
  -noasm ....... disable all assembly optimizations