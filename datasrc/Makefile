#
#   Copyright 2005-2007 by Mark Weyer
#   Maintenance modifications 2010,2011 by the cuyo developers
#
#   This program is free software; you can redistribute it and/or modify
#   it under the terms of the GNU General Public License as published by
#   the Free Software Foundation; either version 2 of the License, or
#   (at your option) any later version.
#
#   This program is distributed in the hope that it will be useful,
#   but WITHOUT ANY WARRANTY; without even the implied warranty of
#   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#   GNU General Public License for more details.
#
#   You should have received a copy of the GNU General Public License
#   along with this program; if not, write to the Free Software
#   Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307  USA
#

#
# Usage
# =====
#
# If you don't want to know too much:
#
# make all
# make install
#
# A more thorough description follows.
#
#
#
# Interface:
# ==========
#
# make all
#   Create all levels that have sources
#
# make <levelname>
#   Create an individual level that has sources.
#
# make install
#   Copy all levels that were created to their destination.
#
# make tidy
#   Delete all intermediate files and all files ending in ~.
#
# make clean
#   Delete all files that were regularly created.
#
#
# Requirements:
# =============
#
# You will need m4, make, and ocaml (including the native-code compilers).
#


DATA_DIR = ../data

INSTALL_DIR = $(DATA_DIR)




cvsfiles_local:
	echo "Makefile.common" >> cvsfiles
	echo "make.ml" >> cvsfiles
	echo "make.mli" >> cvsfiles
	echo "README" >> cvsfiles

distfiles_local: makefile.opt
	./makefile.opt dist `cd $(DATA_DIR) && ./used_levels.sh` >> distfiles
	echo "Makefile.common" >> distfiles
	echo "make.ml" >> distfiles
	echo "make.mli" >> distfiles

cleanfiles_local:
	$(NOOP)



include Makefile.common



# The following targets are listed here to prevent them being handed to
# makefile.opt although we do not have real rules for them:

Makefile.common:
	$(NOOP)

