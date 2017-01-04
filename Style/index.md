---
layout: page
title: Style
permalink: /Style/
---
This page is intended to serve as guidance on how things are supposed to look and how things are intended to be organized. The purpose of creating and specifying a style is not to satisfy the unrighteous lusts of the project lead; rather, it is to improve consistency and readability. Most of the decisions given here were made after much discussion and experimentation and were chosen to enhance the quality of the code.

Please read the following pages for further information about the style chosen for NJOY21 and its subprojects:

- [Coding Style][1]
- [Directory Hierarchy and Filename Conventions][2]

A good and short read about the importance of following a chosen style is: [ Brown M&Ms: A Quick Way to Determine Code Quality][3].

## Language Standards and Tools

In order to build NJOY21 from source, support for the following language standards is required:

 - [Fortran 2003 ][4]
 - [C++14 ][5]
 - [Python 3.4][6]

These language standards were chosen as they are the current standards with widespread compiler support at the time they were chosen.

Any feature of these language standards is fair game to be assumed available while developing. In addition, to build and compile NJOY21, the following build/configuration tools are required:

 - [CMake 3.2](http://cmake.org) or later

### Packages and Code Dependencies
All code that is used by NJOY21 or any of its packages must be freely available and compatible with the NJOY21 LICENSE. That way we don’t run afoul of the law.

Since we want the build process for NJOY21 to be as simple as possible for the user, all packages and code dependencies must be distributed and built as part of NJOY21. 

For example, [easylogging++][7] is used in nearly all of the NJOY21 packages, but the build process does *not* require the user to download and install easylogging++ separately. Instead, easylogging++ is distributed along with the code for NJOY21.


## Compiling and Compiler Flags

All source should compile without throwing any errors (clearly) or warnings. If warnings are observed, the source should be corrected to avoid the warnings. If it is not possible to resolve the cause of the compiler warnings, then compiler flags may be added to suppress the warning, but this should be a last resort—we want to have standard-compliant code.

Legacy NJOY is an exception—prefer not to change the code; change compiler flags instead.

[1]:	Code
[2]:	Hierarchy
[3]:	http://hiltmon.com/blog/2015/10/14/brown-mms/
[4]:	http://www.j3-fortran.org
[5]:	http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.htm?csnumber=64029
[6]:	https://docs.python.org/3.4/
[7]:	https://github.com/easylogging/easyloggingpp