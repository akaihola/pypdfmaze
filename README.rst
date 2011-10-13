=================
 Printable Mazes
=================

This is akaihola's fork of David Bau's `original pymaze.py`_ script, which is
*"a free PDF maze generator that can create mazes of various sizes and
complexity, including pretty diabolical mazes that include 3-d
crossings..."*. `Dave's site`_ also includes a web form for generating maze
PDFs interactively using the code as a CGI script.


Requirements
============

The maze generator requires Python_ and the ReportLab_ library. On Debian-based
systems (e.g. Ubuntu) they must be installed from the command line::

    sudo apt-get install python-reportlab


Command-line arguments
======================

When run on the command line, the script accepts the following options:

  * ``-w <NUM>``: width of the paper (default: width of a letter page)
  * ``-h <NUM>``: height of the paper (default: height of a letter page)
  * ``-m <NUM>``: page margin (default: 36 points)
  * ``-p <PAGESIZE>``: page size (e.g. a4 or letter)
  * ``--cell=<NUM>``: cell size (default: 24)
  * ``--tube=<NUM>``: tube width (default: 0.7)
  * ``--wall=<NUM>``: wall thickness (default: 0.3)
  * ``--curve=<0/1>``: rounded corners (default: 1=yes)
  * ``--cross=<0/1>``: generate multi-level crossings (default: 1=yes)

Dimensions are expressed in *points* (1/72ths of an inch) except for tube width
and wall thickness, which are ratios relative to the cell size.

Example
=======

::

    python pymaze.py -p a4 --cross=0 --cell=48 >maze.pdf

.. _`original pymaze.py`: http://davidbau.com/downloads/pymaze.py
.. _`Dave's site`: http://davidbau.com/archives/2006/10/10/printable_mazes.html
.. _Python: http://python.org/
.. _ReportLab: http://www.reportlab.com/ 
