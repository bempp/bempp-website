---
title: Publications
---

This page lists publications by members of the Bempp team.
If you use Bempp in your research, we would be grateful if you cite the relevant publications.
This list is also available in [BibTeΧ format](assets/bempp.bib).

## Main citations

The following paper is the main citation for the Bempp library. This paper is based on Bempp-cl.
{% include _paper.html
    id="BetckeScroggs2021"
    author="T. Betcke & M. W. Scroggs"
    title="Bempp-cl: A fast Python based just-in-time compiling boundary element library"
    journal="Journal of Open Source Software"
    volume="6"
    number="59"
    year="2021"
    pagestart="2879"
    doi="10.21105/joss.02879"
%}

To see a large number of applications of Bempp, take a look at [the list of papers that cite any of the three main Bempp papers on Google Scholar](https://scholar.google.co.uk/scholar?cites=17530791602214284423,11433496395088984366,149600224103853667,3529577898501410539).

### Older versions of Bempp
The following paper was the main citation for older versions of the Bempp library.
Please note that this paper is based on Bempp 2.0 with an incompatible syntax to the current version.
{% include _paper.html
    id="Smigaj2015"
    author="W. Śmigaj, S. Arridge, T. Betcke, J. Phillips & M. Schweiger"
    title="Solving boundary integral problems with BEM++"
    journal="ACM Transactions on Mathematical Software"
    volume="41"
    number="2"
    year="2015"
    pagestart="6:1"
    pageend="6:40"
    pdf="http://discovery.ucl.ac.uk/1380119/2/a6-smigaj.pdf"
    doi="10.1145/2590830"
%}

### Maxwell's equations
The main citation for using Bempp to solve electromagnetic problems is the following paper.
{% include _paper.html
    id="Scroggs2017"
    author="M. W. Scroggs, T. Betcke, E. Burman, W. Śmigaj & E. van 't Wout"
    title="Software frameworks for integral equations in electromagnetic scattering based on Calderón identities"
    journal="Computers & Mathematics with Applications"
    volume="74"
    number="11"
    year="2017"
    pagestart="2897"
    pageend="2914"
    pdf="https://www.sciencedirect.com/science/article/pii/S0898122117304789/pdfft?isDTMRedir=true&download=true"
    arxiv="1703.10900"
    doi="10.1016/j.camwa.2017.07.049"
%}

## List of publications by year
### 2021
{% include _paper.html
    author="T. Betcke & M. W. Scroggs"
    title="Bempp-cl: A fast Python based just-in-time compiling boundary element library"
    journal="Journal of Open Source Software"
    volume="6"
    number="59"
    year="2021"
    pagestart="2879"
    doi="10.21105/joss.02879"
%}
{% include _paper.html
    author="T. Betcke & M. W. Scroggs"
    title="Designing a high-performance boundary element library with OpenCL and Numba"
    journal="IEEE Computing in Science & Engineering"
    volume="23"
    number="4"
    year="2021"
    pagestart="18"
    pageend="28"
    doi="10.1109/MCSE.2021.3085420"
%}

### 2020
{% include _paper.html
    id="Betcke2020"
    author="T. Betcke, M. W. Scroggs & W. Śmigaj"
    title="Product algebras for Galerkin discretizations of boundary integral operators and their applications"
    journal="ACM Transactions on Mathematical Software"
    volume="46"
    number="1"
    year="2020"
    pagestart="4:1"
    pageend="4:22"
    pdf="https://dl.acm.org/doi/pdf/10.1145/3368618?download=true"
    arxiv="1711.10607"
    doi="10.1145/3368618"
%}

### 2019
{% include _paper.html
    id="Hagemann2019"
    author="F. Hagemann, T. Arens, T. Betcke & F. Hettlich"
    title="Solving inverse electromagnetic scattering problems via domain derivatives"
    journal="Inverse Problems"
    volume="35"
    number="8"
    year="2019"
    pdf="https://discovery.ucl.ac.uk/id/eprint/10075334/6/Betcke_Solving%20inverse%20electromagnetic%20scattering%20problems%20via%20domain%20derivatives_AAM.pdf"
    doi="10.1088/1361-6420/ab10cb"
%}

{% include _paper.html
    id="Betcke2019"
    author="T. Betcke, E. Burman & M. W. Scroggs"
    title="Boundary element methods with weakly imposed boundary conditions"
    journal="SIAM Journal on Scientific Computing"
    volume="41"
    number="3"
    year="2019"
    pagestart="A1357"
    pageend="A1384"
    pdf="https://discovery.ucl.ac.uk/id/eprint/10073557/13/Betcke_Boundary%20Element%20Methods%20with%20Weakly%20Imposed%20Boundary%20Conditions_VoR.pdf"
    arxiv="1807.01109"
    doi="10.1137/18M119625X"
%}

### 2017
{% include _paper.html
    id="Vater2017"
    author="K. Vater, T. Betcke & B. Dilba"
    title="Simple and efficient GPU parallelization of existing H-matrix accelerated BEM code"
    year="2017"
    arxiv="1711.01897"
%}

{% include _paper.html
    author="M. W. Scroggs, T. Betcke, E. Burman, W. Śmigaj & E. van 't Wout"
    title="Software frameworks for integral equations in electromagnetic scattering based on Calderón identities"
    journal="Computers & Mathematics with Applications"
    volume="74"
    number="11"
    year="2017"
    pagestart="2897"
    pageend="2914"
    pdf="https://www.sciencedirect.com/science/article/pii/S0898122117304789/pdfft?isDTMRedir=true&download=true"
    arxiv="1703.10900"
    doi="10.1016/j.camwa.2017.07.049"
%}

{% include _paper.html
    id="Betcke2017"
    author="T. Betcke, E. van 't Wout & P. Gélat"
    title="Computationally efficient boundary element methods for high-frequency Helmholtz problems in unbounded domains"
    bookeditor="D. Lahaye, J. Tang & K. Vuik"
    book="Modern Solvers for Helmholtz Problems"
    bookpublisher="Springer"
    year="2017"
    pdf="https://discovery.ucl.ac.uk/id/eprint/1478241/1/BetckeWoutGelat2016HelmholtzBook.pdf"
    doi="10.1007/978-3-319-28832-1_9"
%}
### 2015
{% include _paper.html
    id="vantWout2015"
    author="E. van 't Wout, P. Gélat, T. Betcke & S. Arridge"
    title="A fast boundary element method for the scattering analysis of high-intensity focused ultrasound"
    journal="Journal of the Acoustical Society of America"
    volume="138"
    number="5"
    year="2015"
    pagestart="2726"
    pageend="2737"
    pdf="http://discovery.ucl.ac.uk/1488806/1/1.4932166.pdf"
    doi="10.1121/1.4932166"
%}

{% include _paper.html
    id="Groth2015"
    author="S. P. Groth, A. J. Baran, T. Betcke, S. Havemann & W. Śmigaj"
    title="The boundary element method for light scattering by ice crystals and its implementation in BEM++"
    journal="Journal of Quantitative Spectroscopy and Radiative Transfer"
    volume="167"
    year="2015"
    pagestart="40"
    pageend="52"
    pdf="https://www.reading.ac.uk/web/files/maths/Preprint_MPS_15_05_Groth.pdf"
    doi="10.1016/j.jqsrt.2015.08.001"
%}

{% include _paper.html
    author="W. Śmigaj, S. Arridge, T. Betcke, J. Phillips & M. Schweiger"
    title="Solving boundary integral problems with BEM++"
    journal="ACM Transactions on Mathematical Software"
    volume="41"
    number="2"
    year="2015"
    pagestart="6:1"
    pageend="6:40"
    pdf="http://discovery.ucl.ac.uk/1380119/2/a6-smigaj.pdf"
    doi="10.1145/2590830"
%}
