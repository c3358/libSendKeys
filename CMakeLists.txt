#
# SendKeys
# Copyright (c) 2011 Kai Uwe Jesussek <kajot@gmx.net>
# 
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
# 
# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.
# 
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
# THE SOFTWARE.
#  
# @file	CMakeLists.txt
# 
# @brief	File for CMake Build System
#

OPTION(BUILD_EXAMPLES "Build examples" OFF)

cmake_minimum_required(VERSION 2.8)
project(sendkeys CXX)

ADD_LIBRARY(sendkeys STATIC SendKeys.cpp SendMouse.cpp)

if(BUILD_EXAMPLES)
	#adds the directory with examples
	add_subdirectory(examples)
endif(BUILD_EXAMPLES)