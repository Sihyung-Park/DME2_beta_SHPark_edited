# 
#  Copyright (C) 2005-2008 Cold Spring Harbor Laboratory
#  Authors: Andrew D. Smith, Pavel Sumazin and Michael Q. Zhang
# 
#  This file is part of CREAD.
# 
#  CREAD is free software; you can redistribute it and/or modify
#  it under the terms of the GNU General Public License as published by
#  the Free Software Foundation; either version 2 of the License, or
#  (at your option) any later version.
# 
#  CREAD is distributed in the hope that it will be useful,
#  but WITHOUT ANY WARRANTY; without even the implied warranty of
#  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#  GNU General Public License for more details.
# 
#  You should have received a copy of the GNU General Public License
#  along with CREAD; if not, write to the Free Software
#  Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA
#

HEADERS = $(shell ls *.hpp)
SOURCES = $(shell ls *.cpp)

OBJS = $(subst .cpp,.o,$(filter-out $(addsuffix .cpp,$(PROGS)),$(SOURCES)))

STATIC_LIB = libcread.a
DYNAMIC_LIB = libcread.so

LIBS = -lpopt
LIBDIR = lib
INCLUDEDIR = include
GSL_LIBS = -lgsl -lgslcblas
CXX = g++
CFLAGS = -Wall -fPIC
OPTFLAGS = -O2
DEBUGFLAGS = -g

#ifndef CREAD
#$(error Variable CREAD is not defined)
#endif

ifdef DEBUG
CFLAGS += $(DEBUGFLAGS)
endif

ifdef OPT
CFLAGS += $(OPTFLAGS)
endif

all: $(OBJS)

%.o: %.cpp %.hpp
	$(CXX) $(CFLAGS) -c -o $@ $<

%.o: %.cpp
	$(CXX) $(CFLAGS) -c -o $@ $<

clean:
	@-rm -f $(PROGS) *.o *.so *.a

.PHONY: clean
