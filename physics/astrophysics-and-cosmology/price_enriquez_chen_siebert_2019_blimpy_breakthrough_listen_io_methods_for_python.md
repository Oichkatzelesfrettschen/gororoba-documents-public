Source: ChatGPT data export, attachment file_00000000079471fdb956def73f8b2280
PDF sha256: 81ac4b4213661a06edbb29f289389e777f4df20959b58b90427836937061822c
License: https://creativecommons.org/licenses/by/4.0/
Language: eng
Fidelity: machine (failed: characters)

# Transcription of price_enriquez_chen_siebert_2019_blimpy_breakthrough_listen_io_methods_for_python.pdf

Transcription of `price_enriquez_chen_siebert_2019_blimpy_breakthrough_listen_io_methods_for_python.pdf` in this directory, 3 pages; each `## PDF page` heading marks a page of the PDF.

Method: no page was sent to OCR; pages 1-3 from the PDF's own text layer (pdftotext version 26.01.0 with the TeX glyph-name table sha256 964f0780f6b9, one page at a time). No page was compared against its rendered image; OCR errors remain where a scan is unclear, so the PDF is the authority for every quotation.

## PDF page 1

Blimpy: Breakthrough Listen I/O Methods for Python
Danny C. Price+, 1, 2 , J. Emilio Enriquez+, 1, 3 , Yuhong Chen1 , and
Mark Siebert1

DOI: 10.21105/joss.01554
Software
• Review
• Repository
• Archive
Submitted: 28 June 2019
Published: 21 October 2019
License
Authors of papers retain
copyright and release the work
under a Creative Commons
Attribution 4.0 International
License (CC-BY).

+ Equal contribution from both authors 1 Department of Astronomy, University of California
Berkeley, Berkeley CA 94720, United States of America 2 Centre for Astrophysics &
Supercomputing, Swinburne University of Technology, Hawthorn, VIC 3122, Australia 3 Department
of Astrophysics/IMAPP, Radboud University, Nijmegen, Netherlands

Summary
The search for extraterrestrial intelligence (SETI) has historically used radio astronomy data
as the main venue to search for artificial signals of extraterrestrial origin. The Breakthrough
Listen program is the latest large-scale project for the search of technosignatures, and thanks to
modern telescopes and instrumentation, as well as significant amounts of dedicated observing
time, the program has become the largest SETI endeavour in history. This has also resulted in
an unprecedented amount of publicly-available data (Lebofsky et al., 2019). Over 1 PB of data
from the Breakthrough Listen program may be downloaded from seti.berkeley.edu/opendata.
The Blimpy—Breakthrough Listen I/O Methods for Python—package provides Python
2.7+/3.6+ utilities for viewing and interacting with the data formats used within the
Breakthrough Listen program. This includes Sigproc filterbank (.fil) and HDF5 (.h5) files
that contain dynamic spectra (aka ‘waterfalls’), and GUPPI raw (.raw) files that contain
voltage-level data. Python methods for data extraction, calibration, and visualization are
provided. A suite of command-line utilities are also available.
The waterfall data product stores an array of detected power across frequency channel
(i.e. spectra) over time. These files can be several GB in size, with up to billions of channels
and/or hundreds of thousands of time steps. Blimpy provides convenient methods to extract
frequencies and time slices of interest—without loading the full file into memory–which
are presented as Numpy arrays (van der Walt, Colbert, & Varoquaux, 2011). Methods for
manipulating lower-level voltage data products stored in the GUPPI raw format, as generated
by the Green Bank Telescope, are also provided. Blimpy uses the Matplotlib library (Hunter,
2007) to provide plotting of spectra, time series, and dynamic spectra; the Astropy package
for handling of astronomical coordinates (Astropy Collaboration et al., 2013; Price-Whelan et
al., 2018); and, the H5py package to interact with data stored in HDF5 files (Collette, 2013).
The turboSETI package, which conducts doppler acceleration searches for narrowband signals
that would indicate the presence of technologically-capable life beyond Earth, uses Blimpy
for file handling and diagnostic plotting.
Blimpy was designed to be used by radio astronomers, students and anyone else interested in
accessing Breakthrough Listen data, whether searching for SETI signals, spectral lines, pulsars,
fast radio bursts, or other astrophysical phenomena. It has already been used in a number of
scientific publications (Croft et al., 2018; Enriquez et al., 2019, 2018; Enriquez et al., 2017;
Gajjar et al., 2018; Price, Croft, et al., 2019; Price, Enriquez, et al., 2019).

Price et al., (2019). Blimpy: Breakthrough Listen I/O Methods for Python. Journal of Open Source Software, 4(42), 1554. https://doi.org/ 1
10.21105/joss.01554

## PDF page 2

Acknowledgements
We thank G. Molenaar and B. Brzycki for their code contributions, along with G. Zhang, G.
Hellbourg, N. Richard, M. Lebofsky, G. Foster, C. Gilbertson, and the wider Breakthrough Listen collaboration. Breakthrough Listen is managed by the Breakthrough Initiatives, sponsored
by the Breakthrough Prize Foundation.

References
Astropy Collaboration, Robitaille, T. P., Tollerud, E. J., Greenfield, P., Droettboom, M., Bray,
E., Aldcroft, T., et al. (2013). Astropy: A community Python package for astronomy, 558,
A33. doi:10.1051/0004-6361/201322068
Collette, A. (2013). Python and hdf5. O’Reilly.
Croft, S., Siemion, A., De Boer, D., Enriquez, J. E., Foster, G., Gajjar, V., Hellbourg, G., et
al. (2018). The Breakthrough Listen Search for Intelligent Life. In American astronomical
society meeting abstracts #231, American astronomical society meeting abstracts (Vol. 231,
p. 231.01).
Enriquez, J. E., Siemion, A., Dana, R., Croft, S., Méndez, A., Xu, A., Deboer, D., et al.
(2019). Breakthrough Listen follow-up of the reported transient signal observed at the Arecibo
Telescope in the direction of Ross 128. International Journal of Astrobiology, 18, 33–35.
doi:10.1017/S1473550417000465
Enriquez, J. E., Siemion, A., Foster, G., Gajjar, V., Hellbourg, G., Hickish, J., Isaacson, H.,
et al. (2017). The Breakthrough Listen Search for Intelligent Life: 1.11.9 GHz Observations
of 692 Nearby Stars. ApJ, 849(2), 104. doi:10.3847/1538-4357/aa8d1b
Enriquez, J. E., Siemion, A., Lazio, T. J. W., Lebofsky, M., MacMahon, D. H. E., Park, R. S.,
Croft, S., et al. (2018). Breakthrough Listen Observations of 1I/�Oumuamua with the GBT.
Research Notes of the American Astronomical Society, 2, 9. doi:10.3847/2515-5172/aaa6c9
Gajjar, V., Siemion, A. P. V., Price, D. C., Law, C. J., Michilli, D., Hessels, J. W. T.,
Chatterjee, S., et al. (2018). Highest Frequency Detection of FRB 121102 at 4-8 GHz Using
the Breakthrough Listen Digital Backend at the Green Bank Telescope, 863, 2. doi:10.3847/
1538-4357/aad005
Hunter, J. D. (2007). Matplotlib: A 2D graphics environment. Computing in Science &
Engineering, 9(3), 90–95. doi:10.1109/MCSE.2007.55
Lebofsky, M., Croft, S., Siemion, A. P. V., Price, D. C., Enriquez, J. E., Isaacson, H., MacMahon, D. H. E., et al. (2019). The Breakthrough Listen Search for Intelligent Life: Public
Data, Formats, Reduction and Archiving. arXiv e-prints, arXiv:1906.07391. Retrieved from
http://arxiv.org/abs/1906.07391
Price, D. C., Croft, S., DeBoer, D., Drew, J., Enriquez, J. E., Foster, G., Gajjar, V., et al.
(2019). Breakthrough Listen Observations of Asteroid (514107) 2015 BZ509 with the Parkes
Radio Telescope. Research Notes of the American Astronomical Society, 3, 19. doi:10.3847/
2515-5172/ab010b
Price, D. C., Enriquez, J. E., Brzycki, B., Croft, S., Czech, D., DeBoer, D., DeMarines,
J., et al. (2019). The Breakthrough Listen Search for Intelligent Life: Observations of
1327 Nearby Stars over 1.10-3.45 GHz. arXiv e-prints, arXiv:1906.07750. Retrieved from
http://arxiv.org/abs/1906.07750

Price et al., (2019). Blimpy: Breakthrough Listen I/O Methods for Python. Journal of Open Source Software, 4(42), 1554. https://doi.org/ 2
10.21105/joss.01554

## PDF page 3

Price-Whelan, A. M., Sipőcz, B. M., Günther, H. M., Lim, P. L., Crawford, S. M., Conseil,
S., Shupe, D. L., et al. (2018). The Astropy Project: Building an Open-science Project and
Status of the v2.0 Core Package, 156, 123. doi:10.3847/1538-3881/aabc4f
van der Walt, S., Colbert, S. C., & Varoquaux, G. (2011). The NumPy Array: A Structure
for Efficient Numerical Computation. Computing in Science and Engineering, 13(2), 22–30.
doi:10.1109/MCSE.2011.37

Price et al., (2019). Blimpy: Breakthrough Listen I/O Methods for Python. Journal of Open Source Software, 4(42), 1554. https://doi.org/ 3
10.21105/joss.01554
