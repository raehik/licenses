# NOTE

This isn't finished, becaue **I'm not certain**. So, here's an abridged guide
to tide me over:

    1. Copy license into root directory (file name `LICENSE`, could change to
       `LICENSE.txt` later)
    2. If required (e.g. if MIT license), change the copyright line to have the
       correct year, your name & your email.
    3. Add a notice in README.md:

           # License

           [program] is released under the [license](link to license online).
           See `LICENSE` for the full text.

That'll do. No notices in the source files themselves just yet.

# Things to look at

https://github.com/ok100/homepage.py/blob/master/homepage.py
https://github.com/WildCard65/SteamBotPP/blob/master/BotManager/main.cpp


# My style guide for applying a license clearly

i.e. How to make it clear that every file is written by X and distributed under
the GPL/MIT/WTFPL/whatever.

I assume you're using Markdown in your README, so it's called `README.md`.
Else, pleb.

All full license texts can be found at `licenses/texts/[license name]/LICENSE`.

## General

    1. Put this notice into your README.md:

        
## General

    1. Put this notice into your README.md:

        ay
        ay ay
        ay

    2. Copy your preferred license to your root directory.
    3. Put this 'boilerplate' notice into each source file:


## MIT

    1. 1


## GPLv3

    1. 1


## WTFPL

    1. 1


# Notes and comments on how others apply licenses

## Where to find the copyright notice

Almost -all- programs have a short clause or paragraph (or even just a
sentence!) explaining which license it is distributed under and where the full
text can be read. This is **always** in the **readme**. `README` in many GNU
projects, `README.md` in spiffy modern pr0 Web 3.0 GitHub projects,
`readme.txt` in dumb Windows programs, you get my point.

The license file is invariably `LICENSE`, `LICENSE.txt` or `COPYING` (in GNU
projects) - though again Windows uses `license.txt`, probably because Microsoft
made the reeeally fuckin' stupid mistake of making the filesystem
case-insensitive.

Both of these files will almost definitely be found in the program's root
directory.


## Notices in source files?

The Free Software Foundation suggests putting a 'boilerplate' notice at the
start of every source file in your GPL-licensed software, to make clear the
absence of warranty. Funnily enough, even in the *Linux kernel* some files are
missing this notice or have an abridged or somehow different version. Entries
from this:

    This work is licensed under the terms of the GNU GPL, version 2. See
    the COPYING file in the top-level directory.

to this:

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License version 2 as
    published by the Free Software Foundation.

even though the suggested is this:

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

So it's clearly not an end-of-the-world scenario, but still, most files at
least reference the GPL, so I think that's important.

Also important: the copyright holder can be anyone. The Linux kernel has
literally *thousands* of contributors, so most files don't share any author
names. These are stored in the source files, by the way.

GitHub on the other hand uses the MIT license pretty much exclusively, and puts
no notices in any of their files (as well as licensing all repos under the
general 'GitHub Inc.' body). Takes all kinds...? I guess they just don't care
as much.


## Copyright (C) &lt;name of author&gt;

These lines at least are useful/important, especially if the project has
multiple authors (so imperative in the Linux kernel):

    <one line to give the program's name and a brief idea of what it does.>
    Copyright (C) <year>  <name of author>


## GPL - warranty notice in interactive program?

No one in their right mind would (and has as of yet, AFAIK) shove a warranty
notice in your face when you start up the program:

    <program>  Copyright (C) <year>  <name of author>
    This program comes with ABSOLUTELY NO WARRANTY; for details type `show w'.
    This is free software, and you are welcome to redistribute it
    under certain conditions; type `show c' for details.

So let's not do that, shall we?


# Example boilerplate notices

An example first bit of a Linux kernel file (drivers/bus/arm-cci.c):

    /*
     * CCI cache coherent interconnect driver
     *
     * Copyright (C) 2013 ARM Ltd.
     * Author: Lorenzo Pieralisi <lorenzo.pieralisi@arm.com>
     *
     * This program is free software; you can redistribute it and/or modify
     * it under the terms of the GNU General Public License version 2 as
     * published by the Free Software Foundation.
     *
     * This program is distributed "as is" WITHOUT ANY WARRANTY of any
     * kind, whether express or implied; without even the implied warranty
     * of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
     * GNU General Public License for more details.
     */

    #include <linux/arm-cci.h>
    ...

Compare to another one in same directory, 'omap_l3_noc.c':

    /*
     * OMAP4XXX L3 Interconnect error handling driver
     *
     * Copyright (C) 2011 Texas Corporation
     * Santosh Shilimkar <santosh.shilimkar@ti.com>
     * Sricharan <r.sricharan@ti.com>
     *
     * This program is free software; you can redistribute it and/or modify
     * it under the terms of the GNU General Public License as published by
     * the Free Software Foundation; either version 2 of the License, or
     * (at your option) any later version.
     *
     * This program is distributed in the hope that it will be useful,
     * but WITHOUT ANY WARRANTY; without even the implied warranty of
     * MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
     * GNU General Public License for more details.
     *
     * You should have received a copy of the GNU General Public License
     * along with this program; if not, write to the Free Software
     * Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA 02111-1307
     * USA
     */
    #include <linux/module.h>
    ...

Another file, 'drivers/bluetooth/bcm203x.c', has:

    * Copyright (C) 2003 Maxim Krasnyansky <maxk@qualcomm.com>
    * Copyright (C) 2003 Marcel Holtmann <marcel@holtmann.org>

So maybe *that's* how I ought do it. So, if Setsura (my shared OR Enterprise
Awards 2014 project) was a corporation, its notice could be:

    #
    # A file which does a thing
    #
    # Copyright (C) 2014 Setsura Corp.
    # Authors: Ben Orchard <thefirstmuffinman@gmail.com>
    #          Charlie Harding <charding@xsanda.com>
    #

    code
    ...

or if it's not an official company thing:

    #
    # A file which does a thing
    #
    # Copyright (C) 2014 Ben Orchard <thefirstmuffinman@gmail.com>
    # Copyright (C) 2014 Charlie Harding <charding@xsanda.com>
    #

    code
    ...

The last comment line could be omitted.
