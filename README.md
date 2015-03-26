# pdf-to-jpg

This is a small shell script to read a PDF document and convert each page into a JPG file.

The quality and size (in pixels) of the resulting JPGs can be manually adjusted.


# Requirements

This script wraps the work performed by `pdftoppm` and `convert`, both required to get this job done:

 - pdftoppm

 Part of the package [poppler-utils](http://poppler.freedesktop.org/), required to extract PDF pages to .PPM files.
 
 *Copyright 1996-2014 Glyph & Cog, LLC*
 
 Installing on CentOS: `# yum install poppler-utils`
 
 Installing on Ubuntu: `$ sudo apt-get install poppler-utils`

 - convert
 
 Part of the package [ImageMagick®](http://www.imagemagick.org/index.php), required to convert .PPM files in .JPG files.
 
 *Copyright (C) 1999-2006 ImageMagick Studio LLC*

 Installing on CentOS: `# yum install ImageMagick ImageMagick-devel`
 
 Installing on Ubuntu: `$ sudo apt-get install imagemagick`


# Usage

just call the script in a manner most suited to you while providing the required parameters:

```
# sh ./pdf-to-jpg 1 /full/path/to/the/file.pdf username
```


# Features

Currently does the *job hired to do*, no features provided.


# Limitations

A bit limited, for now, it sticks to reading a PDF document and extracting each page to JPEGs that will be stored inside a directory.


# Security

This script accounts for common mistakes with values received, while there's room for improvement, it currently:

 - Checks if parameter #1 exists and is a natural number;
 - Checks if parameter #2 exists and points to a valid filepath;
 - Checks if parameter #3 exists and represents a valid system username.

There's also an extra verification that skips the entiry process if the target directory already exists to prevent collisions.


# Support

Being a bash script, any OS that can handle bash should be able to run this script.

Currently tested on:

 - [CentOS release 5.11](http://wiki.centos.org/Manuals/ReleaseNotes/CentOS5.11) (Final)
 
 ImageMagick version 6.2.8 05/07/12 Q16
 
 pdftoppm version 3.04


# Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style.

*Suggestions are always welcome.*

# License

Free-for-all, but mind licenses from required packages.
