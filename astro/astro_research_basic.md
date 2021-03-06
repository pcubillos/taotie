# Basic Tools for Astrophysical Research

## Data format used in astronomy

* [Flexible Image Transport System (FITS)](https://archive.stsci.edu/fits/)
	- The default standard for the exchange of data in astronomy now
	- The [full document of FITS](https://fits.gsfc.nasa.gov/users_guide/usersguide.pdf) and [the MAST data format guidelines](https://archive.stsci.edu/data_format.html)
	- [CFITSIO](https://heasarc.gsfc.nasa.gov/fitsio/) is a library of C and Fortran subroutines for reading and writing data files in FITS.
	- [__astropy.io.fits__](https://docs.astropy.org/en/stable/io/fits/) can help you deal with FITS files in Python
* [Advanced Scientific Data Format (ASDF)](https://github.com/spacetelescope/asdf)
	- Next generation interchange format for scientific data developed by STScI
	- It follows the new [ASDF Standard](https://asdf-standard.readthedocs.io/en/latest/)
* [__HDF5__ - High-performance data management and storage suite](https://www.hdfgroup.org/solutions/hdf5/)
	- In the age of big data, HDF5 format is also becoming more popular in astronomy. For example, many hydro-simulations use HDF5 to store large and complex data.
	- [__h5py__ is a Pythonic interface to the HDF5 binary data format](https://www.h5py.org/)
	- [__fits2hdf__ is a FITS to HDFITS conversion utility](https://github.com/telegraphic/fits2hdf)
* If you use Python, it is also convenient to use the [__pickle__](https://docs.python.org/3/library/pickle.html) and [__dill__](https://pypi.org/project/dill/) (an even better __pickle__) module for serializing and de-serializing python objects to the majority of the built-in python types.

## World Coordinate Systems (WCS)

* [FITS World Coordinate System (WCS)](https://fits.gsfc.nasa.gov/fits_wcs.html)
	- [__wcslib__](http://www.atnf.csiro.au/people/mcalabre/WCS/wcslib/index.html) is a C library, supplied with a full set of Fortran wrappers, that implements the "World Coordinate System" (WCS) standard in FITS
	- All the tools that deals with FITS format can also deal with WCS information (normally stored in the header). For example, the [__astropy.wcs__](http://docs.astropy.org/en/stable/wcs/)
* [Generalized World Coordinate System](https://gwcs.readthedocs.io/en/latest/)
	- [__gwcs__ - provides tools for managing WCS in a general way](https://github.com/spacetelescope/gwcs)
* [__stwcs__ - WCS based distortion models and coordinate transformation](https://github.com/spacetelescope/stwcs)
* [__tweakwcs__ - Algorithms for matching and aligning catalogs and for tweaking the WCS so as to minimize catalog mismatch errors](https://github.com/spacetelescope/tweakwcs)
	- __tweakwcs__ is a package that provides core algorithms for computing and applying corrections to WCS objects such as to minimize mismatch between image and reference catalogs. Currently only aligning images with FITS WCS and JWST gWCS are supported.

## Astrometry and Positional Astronomy

* [__Skyfield__ - Elegant Astronomy for Python](https://rhodesmill.org/skyfield/)
	- __Skyfield__ computes positions for the stars, planets, and satellites in orbit around the Earth. Its results should agree with the positions generated by the United States Naval Observatory and their Astronomical Almanac to within 0.0005 arcseconds. The [Github version is here](https://github.com/skyfielders/python-skyfield/)
* [__Astrometry.net__ -- automatic recognition of astronomical images](https://github.com/dstndstn/astrometry.net)
	- Made by Dustin Lang. The best astrometric calibration tool on the market.
* [__SOFA__ - Standard of Fundamental Astronomy](http://www.iausofa.org/tandc.html)
	- The International Astronomical Union's SOFA service has the task of establishing and maintaining an accessible and authoritative set of algorithms and procedures that implement standard models used in fundamental astronomy. The library is now in [Fortran and C](http://www.iausofa.org/current.html)
	- [__pysofa2__ - A python module for wrapping the International Astronomical Union's C SOFA libraries](https://gitlab.com/deddy/pysofa2)
* [__ERFA__ - Essential Routines for Fundamental Astronomy](https://github.com/liberfa/erfa)
	- __ERFA__ is a C library containing key algorithms for astronomy, and is based on the [__SOFA__](http://www.iausofa.org/) library published by the International Astronomical Union (IAU).
* [__NOVAS__ - The United States Naval Observatory NOVAS astronomy library](https://github.com/brandon-rhodes/python-novas)
	- __NOVAS__ is an integrated package of functions for computing various commonly needed quantities in positional astronomy. At a lower level, NOVAS also provides astrometric utility transformations, such as those for precession, nutation, aberration, parallax, and gravitational deflection of light. 
	- The computations are accurate to better than one milliarcsecond. 
* [__spherical_geometry__ - A Python package for handling spherical polygons that represent arbitrary regions of the sky](https://github.com/spacetelescope/spherical_geometry)
	- Made by STScI. [Online document is here](https://spacetelescope.github.io/spherical_geometry/spherical_geometry/) 

## Flux standards

* [The Absolute Magnitude of the Sun](http://mips.as.arizona.edu/~cnaw/sun.html)
	- [Link to download the default composite spectrum of the Sun](http://mips.as.arizona.edu/~cnaw/sun_composite.fits)

* [ESO's RA Ordered List of Spectrophotometric Standards](https://www.eso.org/sci/observing/tools/standards/spectra/stanlis.html)
* [NAOJ's Optical Spectrophotometric Standard Stars](https://www.naoj.org/Observing/Instruments/FOCAS/Detail/UsersGuide/Observing/StandardStar/Spec/SpecStandard.html)
* [ESO's Landolt Equatorial Standards](http://www.eso.org/sci/observing/tools/standards/Landolt.html)

## Plan an observation

* [__astroplan__ - Python package to help astronomers plan observations](https://github.com/astropy/astroplan)
* [__iObserve__](http://onekilopars.ec/iobserve/)
	- The free on-line version is [here](https://www.arcsecond.io/iobserve)
* [Object Visibility by ING](http://catserver.ing.iac.es/staralt/)
* [__JSkyCalc__ -- A Convenient, Portable Observing Aid](https://www.dartmouth.edu/~physics/labs/skycalc/flyer.html)
* [Keck telescopes' own planning tool](https://www2.keck.hawaii.edu/software/obsplan/obsplan.php)
* [Astronomical Observatory Sites by Latitude and Longitude](http://www.eso.org/~ndelmott/obs_sites.html)

## Flux unit conversion

* [NICMOS Units Conversion Form](http://www.stsci.edu/hst/nicmos/tools/conversion_form.html)
* [Magnitude/Flux Density Converter: Point Sources](http://ssc.spitzer.caltech.edu/warmmission/propkit/pet/magtojy/)

## Filter Response Curves

* [Response curved collected in sedpy package by Ben Johnson](https://github.com/bd-j/sedpy/tree/master/sedpy/data/filters)
* [__tynt__ - Color filter approximations in Python](https://github.com/bmorris3/tynt)
	- By Brett Morris. __tynt__ is a super lightweight package containing approximate transmittance curves for more than five hundred astronomical filters, weighing in at just under 150 KB. Document can be found [here](https://tynt.readthedocs.io/en/latest/)

## Extinction calculator

* [NED's extinction calculator](https://ned.ipac.caltech.edu/extinction_calculator)
* [3-D Dust Mapping with Pan-STARRS 1](http://argonaut.skymaps.info)
	- [Query service](http://argonaut.skymaps.info/query)

## Coordinate Service

* [RA, DEC Flexible converter](http://www.astrouw.edu.pl/~jskowron/ra-dec/)
* [NED's coordinate calculator](https://ned.ipac.caltech.edu/coordinate_calculator)

## Managing Catalogs

* [__astropy.table__](https://docs.astropy.org/en/stable/table/) is a flexible Python module that can handle a variant types of tables.
* [__TOPCAT__ - Tool for OPerations on Catalogues And Tables](http://www.star.bris.ac.uk/~mbt/topcat/)
	- Really powerful GUI tool to deal with tables. It is written as a Java application.
	- Have great functions for cross-matching catalogs, querying on-line databases, and making publication-grade figures.
	- [__STILTS__ - Starlink Tables Infrastructure Library Tool Set](http://www.star.bris.ac.uk/~mbt/stilts/) provides most of __TOPCAT__'s capabilities in command line.

### Table cross-match

* [__smatch__ - Code to match points on the sphere using the healpix scheme](https://github.com/esheldon/smatch)
	- By Erin Sheldon. Very fast cross-match tool, C-code wrapped in Python.
* [__nway__ - Bayesian cross-matching of astronomical catalogues](https://github.com/JohannesBuchner/nway)
	- Bayesian match probabilities based on astronomical sky coordinates (RA, DEC)
* [__C3__ - Command-line Catalogue Cross-matching Tool](http://dame.dsf.unina.it/c3.html)
* [__xmatch__ - Cross match of catalogs](https://git.ias.u-psud.fr/abeelen/xmatch)
	- By Alexandre Beelen.

## Cosmology Calculator

* [ICRAR's Cosmology Calculator](http://cosmocalc.icrar.org)
	- Based on the [celestial R-code](https://github.com/asgr/celestial)

* [Ned Wright's Cosmology Calculator](http://www.astro.ucla.edu/%7Ewright/CosmoCalc.html)

## Simulate Galaxy Spectrum

* [__SpecGen__ - Mock Galaxy Spectra Generator](http://specgen.icrar.org)

## Sky Projection Maps of Surveys

* [__AstroMap__ - generating sky projection maps for astronomical surveys](http://astromap.icrar.org)


## List of Observatories

* [List of Astronomical Observatories on Wiki](https://en.wikipedia.org/wiki/List_of_astronomical_observatories)

* [Observatories by GoAstronomy](https://www.go-astronomy.com/observatories.htm)
	- Including U.S observatories and observatories worldwide.

## Basic Astronomy Database

* [SIMBAD Astronomical Database - CDS](http://simbad.u-strasbg.fr/simbad/)
    - The __SIMBAD__ astronomical database provides basic data, cross-identifications, bibliography and measurements for astronomical objects outside the solar system.
* [VizieR Catalog Database](http://vizier.u-strasbg.fr/viz-bin/VizieR)
    - __VizieR__ provides the most complete library of published astronomical catalogues -tables and associated data- with verified and enriched data, accessible via multiple interfaces.
* [Aladin Sky Atlas](https://aladin.u-strasbg.fr/aladin.gml#)
    - __Aladin__ is an interactive sky atlas allowing the user to visualize digitized astronomical images or full surveys, superimpose entries from astronomical catalogues or databases, and interactively access related data and information from the Simbad database, the VizieR service and other archives for all known astronomical objects in the field.
* [NASA/IPAC Extragalactic Database](https://ned.ipac.caltech.edu/)
    - __NED__ is a comprehensive database of multiwavelength data for extragalactic objects, providing a systematic, ongoing fusion of information integrated from hundreds of large sky surveys and tens of thousands of research publications.
* [NASA/IPAC Infrared Science Archive](https://irsa.ipac.caltech.edu/frontpage/)
    - __IRSA__ is chartered to curate the science products of NASA's infrared and submillimeter missions, including many large-area and all-sky surveys.
* [MAST - Mikulski Archive for Space Telescopes](http://archive.stsci.edu/)
    - __MAST__ provides a variety of astronomical archives focused on scientific data sets in the optical, ultraviolet, and near-infrared parts of the spectrum.
    - [The MAST Portal](https://mast.stsci.edu/portal/Mashup/Clients/Mast/Portal.html) lets you search multiple collections of astronomical datasets all in one place.