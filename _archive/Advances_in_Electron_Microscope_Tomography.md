---
title: Advances in Electron Microscope Tomography
layout: page
order: 1
---

### Contents

1. [Progress and Prospects for Electron Microscope Tomography](#progress-and-prospects-for-electron-microscope-tomography)
2. [Tomography Day at UCSD](#tomography-day-at-ucsd)
    * [Topic 1. The radon transform and its cousins](#topic-1-the-radon-transform-and-its-cousins)
    * [Topic 2. The AI problems associated with tomography: tracking and
      segmentation](#topic-2-the-ai-problems-associated-with-tomography-tracking-and-segmentation)
    * [Session 3. Algorithms and architectures](#session-3-algorithms-and-architectures)
    * [Topic 4. Tomography, Optics and Instrumentation](#topic-4-tomography-optics-and-instrumentation)

3. [Recent Developments](#recent-developments)
    * [Multiscale Phenomena](#multiscale-phenomena)

4. [Stochastic Geometry and Multiscale Biology](#stochastic-geometry-and-multiscale-biology)
    * [What is Stochastic Geometry?](#what-is-stochastic-geometry)
    * [Imaging and Stochastic Geometry](#imaging-and-stochastic-geometry)
    * [Stereology](#stereology)

5. [Exascale Computing](#exascale-computing)
6. [Tomography and Pure Mathematics](#tomography-and-pure-mathematics)
7. [Recent Software Developments](#recent-software-developments)
    * [Iterative Methods](#iterative-methods)
    * [Fluorescence and Electron Microscopies](#fluorescence-and-electron-microscopies)
    * [Coordinated Microscopies](#coordinated-microscopies)

8. [Related Links](#related-links)
9. [References of Interest](#references-of-interest)
    * [Electron Microscope Tomography](#electron-microscope-tomography)
    * [Lambda Tomography](#lambda-tomography)
    * [Tracking](#tracking)
    * [Bundle Adjustment](#bundle-adjustment)
    * [Parallel Processing](#parallel-processing)
    * [Mathematical Foundations](#mathematical-foundations)
    * [Regularization Methods](#regularization-methods)
    * [Meetings of Interest to Tomographers](#meetings-of-interest-to-tomographers)
    * [Recent Presentations on EM Tomography](#recent-presentations-on-em-tomography)

10. [Participants](#participants)
11. [Contacts](#contacts)
12. [Special Thanks](#special-thanks)

<P></p>

### Progress and Prospects for Electron Microscope Tomography

In recent years the biological electron microscopy community has adapted
technical improvements in instrumentation, data collection modes and
large format digital image detectors. For example images on the order of
4K X 4K pixels are commonplace, and multiple detectors and montaging
techniques make series of billion-pixel images achievable without
extraordinary effort. As input to tomographic reconstruction this flood
of image data plays an important role in determining the
three-dimensional structure and function of cells and sub-cellular
organelles. Structure may be elucidated across a wide range of spatial
scales, ranging from that of neurons in the brain, for example, down to
the scale of proteins and protein complexes. The scale and volume of
this data, is in itself, a challenge to the transmission, reconstruction
and storage of the processed data. In response to the requirements for
high-quality three-dimensional reconstructions from EM data this branch
of computer tomography is presently under a state of rapid development.
Areas of future progress include instrumentation, data collection,
reconstruction and other image processing techniques. Because of rapid
advances in instrumentation and computer-based reconstruction, the
routine imaging of molecular structure in context appears to be likely
within the next few years.

Electron microscope (EM) tomography presents a number of special
problems. The imagery is low contrast and noisy with limited sampling of
projection directions; sample warping and the curvilinearity of electron
trajectories make classical techniques of x-ray tomography problematic;
and the volume and scale of the data make automated preprocessing and
image segmentation necessary. The need for solution of these problems
has spurred the introduction of new techniques into EM tomography. For
example, the presence of geometric nonlinearities in the basic ray
transform requires that the inversion problem be treated in terms of
Fourier integral operators rather than Fourier transforms. Recently
Bayesian techniques and Markov random field techniques have been applied
to other steps in the tomographic reconstruction process such as feature
extraction, tracking, alignment, and post processing steps. Progress in
all aspects of EM tomography requires deeper mathematical understanding,
and the introduction of new algorithms and techniques from computer
science.

Up to the present, most conferences on EM tomography have concentrated
on the biology. This is also true for more permanent publication such as
books and papers, and is in contrast to related areas such as X-ray
tomography where the technical aspects have a well-developed presence.
Nevertheless, both the instrumentation and computational aspects of EM
tomography have shown rapid progress, and this discipline is developing
a foundation of its own, in both the mathematics and the engineering
disciplines. Therefore, we believe that now is a good time to initiate
the exchange ideas on the mathematical foundations, computer science and
engineering.

Although we will emphasize applications of EM tomography to the
biological sciences, materials science also makes extensive use of this
technology. Electron tomography in the materials sciences is a rapidly
advancing area of scientific endeavor and affords many opportunities for
collaborative activities. ([Electron Tomography for Nanoscale Materials
Science](http://journals.cambridge.org/production/action/cjoGetFulltext?fulltextid=326132 "http://journals.cambridge.org/production/action/cjoGetFulltext?fulltextid=326132"))

A tutorial on EM tomography, including sessions on instrumentation and
the software package TxBR was presented at the [ISBI 2009
Conference](http://www.biomedicalimaging.org/Tutorial_03.asp "http://www.biomedicalimaging.org/Tutorial_03.asp").

### Tomography Day at UCSD

[![Group Photo for Attendees at the Calit2 Quad](/images/tomo/TomographyDay_UCSD.jpg)](/images/tomo/TomographyDay_UCSD.jpg "Group Photo for Attendees at the Calit2 Quad")

#### Topic 1. The radon transform and its cousins

The purpose of this session is to introduce the basics of the [generalized Radon transform]
(/images/tomo/Generalized-radon-transform.pdf "Generalized-radon-transform.pdf")
as it arises in EM tomography and its associated inverse problem.
We will cover applications of [microlocal analysis](/images/tomo/Microlocal-analysis.pdf "/images/tomo/Microlocal-analysis.pdf")
and the Fourier integral operator.

#### Topic 2. The AI problems associated with tomography: tracking and segmentation

The purpose of this session is to give a quick review of feature extraction,
[tracking](/images/tomo/Tracking.pdf "/images/tomo/Tracking.pdf")
and image segmentation. We will then discuss why these techniques are
necessary to the tomographic process, what information we must extract
from the data, and the special problems of dealing with EM data. We will
also cover some new techniques from graph theory and Markov random
fields, as time permits. New results on fiducial free alignment based on
extended structures in the EM images will be presented at the [CSIE 2009
Conference](http://world-research-institutes.org/conferences/CSIE/2009 "http://world-research-institutes.org/conferences/CSIE/2009")
by Sebastien Phan. A preliminary presentation on [alignment on points and one dimensional
structures](/images/tomo//Alignment-on-points.pdf "/images/tomo//Alignment-on-points.pdf")
is available. This method is an extension of [occluded contour
techniques](http://www.visionbib.com/bibliography/shapefrom408.html "http://www.visionbib.com/bibliography/shapefrom408.html").

#### Session 3. Algorithms and architectures

The purpose of this session is to review the current state of EM
tomography packages, future requirements for speed and computational
resources, and new developments in computer hardware such as [graphical processor units]
(/images/tomo/e/e0/Graphical-processor-units.pdf "/images/tomo//Graphical-processor-units.pdf")
which may be applied to the reconstruction and data processing problems.
Matching architectures to algorithms promises to be an active area of
development. GPU boards in workstations can yield substantial [performance
gains](http://fastra.ua.ac.be/en/index.html "http://fastra.ua.ac.be/en/index.html")
in tomographic applications. Results obtained by researchers at NCMIR
will also be presented at the [CSIE 2009
Conference](http://world-research-institutes.org/conferences/CSIE/2009 "http://world-research-institutes.org/conferences/CSIE/2009").
Information relating to new developments in 2011 may be found at the
following link: [presentation on contour alignment, montaging and applications of tropical
semirings](/images/tomo/Presentation-on-contour.pdf "/images/tomo/Presentation-on-contour.pdf").

#### Topic 4. Tomography, Optics and Instrumentation

The purpose of this session is to provide a quick introduction to the
practical side electron microscope tomography followed by a presentation
of [recent advances in tomography techniques and
instrumentation](/images/tomo/Recent-advances.pdf "/images/tomo/Recent-advances.pdf").
Emphasis will be on the methods of acquisition of data covering a wide
range of spatial scales. A tutorial on instrumentation will be presented at the [ISBI 2009
Conference](http://www.biomedicalimaging.org/Tutorial_03.asp "http://www.biomedicalimaging.org/Tutorial_03.asp").

### Recent Developments

#### Multiscale Phenomena

EM images span spatial scales ranging from a fraction of a nanometer to
about 50 micrometers, and typical 3D reconstructions may cover 1 / 10^15 of the volume of a typical optical microscope reconstruction. The
limit of resolution of light microscopy is on the order of a hundred
nanometers, and even though super resolution techniques applied in
pointilliste optical tomographymay give much better resolution, but
rare events and contextual information are missed.

In order to bridge the gap, the spatial range of the electron microscope
has been expanded by various techniques. Large sensor arrays and
wide-field camera assemblies have increased the field dimensions by a
factor of ten over the past decade, with a further 10X expansion
possible and new techniques for serial tomography (z-axis) and montaging
(x and y axes) make possible the assembly of tens of thousands of three
dimensional reconstructions. Even though we are far from closing the
spatial scale gap with a single experimental preparation, the amount of
data generated by this enterprise threatens to overwhelm computational
resources. A single data set for tomographic processing may have as many
as 360 images, each 8K by 8K. Simple backprojection is order N^3 so a
data set of this size requires about 10^13 or more coordinate
evaluations. Because coordinate evaluations involve nonlinear functions
in our case, the number of elementary operations is hundreds of times
more, and bit error rates require double precision. The number of
reconstruction volumes necessary to image an average cell down to the
protein assembly level is of the order 10^4 , so counting exponents, we
are into the exascale range. Data sets for this are well into the
petascale range.

The present state of the art depends on development of new algorithmic
techniques in addition to the scientific instrumentation and computer
hardware which permit the experimenter to obtain the data and run the
reconstructions. We appeal to a particular example which makes this
point. TxBR runs in 4 days instead of 4 years on the particular data set
mentioned above because the evaluation of high degree polynomials on a
regular grid can be reduced to a simple recursion consisting of
additions, and that the number of additions is linear (rather than
exponential) in the degree of the polynomial. This, can be performed on
a workstation with several GPU cards. Furthermore, the recursion can be
made parallel to a very high degree, and the algorithm can be mapped to
the simplified processors comprising, for example, a graphics processor
unit. Programming this on a GPU board reduces the 4 days to less than 4
hours.

### Stochastic Geometry and Multiscale Biology

#### What is Stochastic Geometry?

Stochastic geometry, or geometrical probability, designates probability
problems which incorporate geometrical figures as the 'outcomes' or
'data'. Random positions of a geometrical figure are the center of the
classical theory. Applications range from astronomy to cell biology and
materials science. Additionally the probabilistic foundations are
connected to other branches of pure mathematics. Scientific problems may
have a geometrical content in the data, in sampling, in theoretical
models, or in all three.

Examples of geometrical data in biology include: maps of neurons,
proximity data for interacting macromolecules, particle counts,
configurations of linear structures such as filaments, shapes of
ultrastructural components, or morphological changes as the result of
experimental manipulation or disease, and derived measures such particle
counts, length ,surface area, and volumes.

Even the question of summarizing data may be nontrivial. Many
experimental sampling techniques can be described as geometrical.
Spatial variation of cell types or morphological changes might be
sampled along a linear transect, inside an arbitrary grid square or
within a fixed radius of an arbitrary reference point.

Solid structures of biological tissues are frequently studied by taking
thin sections for microscopic examination. Here the deep problem of
relating solid geometry to plane sections is compounded with questions
of sampling variability, bias, choice of sampling design and inference.
The multidisciplinary science of stereology deals mainly with sectioning
problems and is an important area of application for stochastic
geometry. Finally, idealized models of natural phenomena often invoke
geometrical probability. These tend to be gross simplifications of
complex processes, such as the packing of astrocytes in the central
nervous system or the attachment of antibodies to a virus or the
distribution of fluorescent markers along proteins along filaments, or
embedded in biological membranes.

#### Imaging and Stochastic Geometry

New advanced experiments give access to the molecular level. These
inclued including superresolution fluorescence microscopy, cryoelectron
microscopy (cryo-EM), and EM tomography on multiple tilt series. These
imaging technologies require the development of new computer-based
mathematical and statistical methods of analysis. For example cryo-EM
and large scale averaging with traditional plastic sections has
experienced several successes in recent years but is now facing a number
of problems which can only be solved in collaboration with
mathematicians, statisticians and computer scientists.

Because of the rapid development of imaging technologies extending the
spatial range to molecular scales advanced research world-wide has found
a new focus on fundamental issues. This research is inspired by the need
to develop new stochastic geometry methods with the ultimate purpose of
establishing a mathematical and statistical fundamental to computer
based analysis of advanced bioimaging data. These efforts take place at
the boundaries between mathematics, statistics, computer science and
bioscience.


 **Multiscale Biology.** Biological processes take place on a wide range
of spatial and temporal scales, from the molecular to the whole
organism. Ongoing work in light and electron microscopy has extend the
scale available for imaging to the level of large molecules and
molecular assemblies. In addition to the structural information
available trom electron microscopy, fluorescence microscopy has added
dynamical information as well as information about the location of
specific proteins. Modern staining techniques also can locate the site
of fluorescence within nanometers. We may exploit the opportunities
created by these two imaging technologies in several diverse areas.

**Correlated microscopies.** The first problem is to correlate the
information gained by light and electron microscopy. The immediate task
is to overlay images or sections of 3D reconstructions so that
identifiable structures are in geometric correspondence. This task is
complicated by the range of spatial scales and the nature of the images
at the various spatial scales. We discuss the problems of correlation in
the sections describing work on 3D reconstruction.

**Uncertainty quantification.** Microscopy is Inherently probablistic.
Binding and staining are the result of random processes, and florescence
itself is subject to quantum uncertainty at the molecular level. These
lead to uncertainty in both position and magnitude or relevant physical
events. A second source of error is due to uncertainty in the trajectory
of the interrogating radiation. Paths of electrons through samples and
lenses are subject to local fluctuations in electrical and magnetic
fields, and light paths are affected by varying optical densities across
material interfaces. A third source of error is in the manual marking of
structures for alignment. As microscopy becomes more quantitative, in
terms of measurement of structure and dynamics of biological processes
the need for identification and quantification of sources of uncertainty
becomes more acute.

**Systems biology.** Decades of work on the metabolic processes has
resulted in the construction of network models relating the chemical
interactions and transformations in living cells. There is increasing
evidence that this chemical activity is compartmentalized and that
geometric proximity is a large factor determining whether specific
reactions take place. Accordingly it is necessary to map the metabolic
network to the spatial reconstructions available from light and electron
microscopy. This would entail the introduction of new mathematical
structures into theoretical biology in order to go beyond the database
approaches currently in vogue.

#### Stereology

In this section we discuss the rationale behind stereology applications
in electron microscopy and review our demonstration of stereology
software developed at NCMIR. It should be noted that all microscopy
methods can be regarded as sampling methods, whether or not the process
is guided to capture structures or events of interest. As such, the
development of stereology has been shaped by this circumstance and the
probabilistic theory of sampling.

Stereological tools are standard for accurate (i.e., unbiased) and
precise quantification of any microscopic sample. Research efforts during
the past decades have provided a broad spectrum of tools to estimate a
variety of parameters such as volumes, surfaces, lengths, and numbers.
Current research has focused of extending this to derived geometric
measures, such as mean curvature and other related quantities. These
techniques require sets of parallel sections that can be produced by
either physical or optical sectioning, with optical sectioning being
much more efficient when applicable. At present various EM techniques are
available for stereologic applications. These include transmission and
the so-called block face EM.

Transmission electron microscopy can not fully exploit image data
directly, mainly because of the large depth of field. Electron
tomography yields stacks of slices from electron microscopic sections.
With the development of high resolution techniques for plastic fixed
objects, parallel reconstructed slices of small thickness (2-5 nm axial
resolution) can be produced from EM. These optical slices minimize
problems related to overprojection e?ects, and allow for direct
stereological analysis, e.g., volume estimation with the Cavalieri
principle and number estimation with the optical disector method.

Block face comprises a second class of techniques. While electron
microscopy has been around for eight decades, since its invention in
the 1930s, the technique of Serial Block face Scanning Elecron
Microscopy (SBFSEM) has been made practical (Denk2004) and gained
popularity in the electron microscopy only recently (EM) community
(refs). In this technique an ultramicrotome is inclueded within a
scanning electron microscope (SEM) and is able to remove slices as thin
as 40 nm from a block of tissue embedded in resin and typically stained
with heavy metals during a process of freeze substitution (ref). By
scanning the exposed block face between successive slices, SBFSEM is
relatively easy to use and then able to image large volumes of tissue
without human intervention.

Using modern machines such as the 2 keV FEI Merlin with Gatan 3View
cutting system, this technique can image over a terabyte worth of data
per week when left running unsupervised (ref). Such datasets can span as
much as 32 x 24k pixel and thousands of slices (Fig 1a), with an optical
resolution as low as 2 nm and pixel size as low as 0.5 nm in the XY
dimensions. Depending on pixel size, SBFSEM is able to capture on the
order of hundreds of microns in XY and Z dimensions, and thus enough to
image many cells simultaneously from a specimen of tissue or cultured
cells (Fig 1b).

Such SBFSEM 3D images represent a new precedent in the volume and size
(multiple terabytes/week) in EM, but also represent an even bigger
bottleneck between image acquisition/reconstruction and
segmentation/analysis. Despite advances in automated segmentation
methods, accurate 3D segmentation of complex tissue, such as the primary
cells and neuropil tissue in Fig 1a, requires manual tracing of contour
lines on every slice in order to achieve accurate segmentation and
correct surface topology of every visible compartment. Manual
segmentation in this was is very slow, on the order of seconds per
contour, and approximately three orders of magnitude slower than image
acquisition. Using modern SBFSEM, a single terabyte of complex tissue
can be acquired in approximately three days but would require tens of
thousands of man-hours (decades), for complete manual segmentation of
all cellular and sub-cellular compartments. With such volumes it has
become infeasible for individuals or even groups to fully segment an
entire dataset, and thus the only way to accurately quantify the content
of these datasets is using rapid randomly sampling methods like the
tools offered by stereology.

We have demonstrated the use of stereology on 3D serial block face
scanning electron microscopy (SBFSEM) to acquire highly accurate
quantification information of large tissue samples all the way down to
individual cells. In particular we demonstrate the benefits of applying
stereology to such 3D SBFSEM volumes of tissue, most notably:

(1) a small (5-10 nm for 2 keV) penetration depth, to reduce
over-projection (40-60nm) errors experienced in thin serial sections
imaged with transmission electron microscopes,

(2) the ability to identify questionable structures by checking
adjacent Z-slices, thus decreasing misclassification errors, and

(3) the versatility to project a 3D stereology grids over single cells,
thus allowing quantification of individual cells in situations a
biologist needs more than just a flat average over tissue.

To test results, we manually segmented an entire neural soma and use
point counting stereology of just 1000 points yields a percentage volume
of ±0.3% for each compartment measured, and this decreased error
predictably when more points were added. To perform stereology we
created a "slash stereology plugin" which we have contributed to the
IMOD software package, and could use to count and average of about 3000
points per hour over a 3D grid of any scale within our massive 3D SBFSEM
volume.

### Exascale Computing

Because of the necessity to bridge the gap between electron and light
microscopy, we expect that many more orders of magnitude improvement in
computational capabilities will be required in the coming decades.
Exascale computing, on the other hand, will raise a new set of problems,
associated with component energy requirements (cost per operation and
costs of data transfer) and heat dissipation issues. As energy per
operation is driven down, reliability decreases, which in turn raises
difficult problems in validation of computer models (is the algorithmic
approach faithful to physical reality), and verification of codes (is
the computation reliably correct and replicable)? Leaving aside the
hardware issues, many of these problems will require new mathematical
and algorithmic approaches, including, potentially, a re-evaluation of
the Turing model of computation.

### Tomography and Pure Mathematics

Tomography, or more properly from a mathematician's point of view,
integral geometry is a core area in mathematics. One may find
applications in many areas of mathematics, physics, and engineering.
Inverse transport, for example, is an obvious generalization of
inversion of the Radon transform, and inverse transport is encountered
in many areas of biomedical imaging. Another area of mathematics which
shows up, surprisingly, in areas as diverse as electron microscopy (as
originally noted by Peter Hawkes in the 1990s) and by brain modelers is
topical algebra. In tropical algebra, the mathematical operations of
product and sum are replaced by the simpler operations of sum and
maximum, respectively. Study of this algebra has recently had a major
impact in theoretical mathematics.

### Recent Software Developments

Alignment of the individual images of a tilt series is a critical step
in obtaining high-quality electron microscope reconstructions. We are
continuing research into techniques for producing good alignments, and
utilizing the alignment data in subsequent reconstruction steps. Our
alignment techniques utilize bundle adjustment. Bundle adjustment is the
simultaneous calculation of the position of distinguished markers in the
object space and the transforms of these markers to their positions in
the observed images, along the bundle of particle trajectories along
which the object is projected to each EM image. Bundle adjustment
techniques are general enough to encompass the computation of linear,
projective or nonlinear transforms for backprojection, and can
compensate for curvilinear trajectories through the object, sample
warping, and optical aberration. This research has resulted in an
advanced code "**T**ransform-**B**ased **T**racking, **B**undle
Adjustment and **R**econstruction" (TxBR).

#### Iterative Methods

Until recently main two approaches to 3D reconstruction have been
employed, electron tomography (ET) and single particle analysis. In ET,
the same sample volume is observed multiple times under many different
viewing angles and the set of images is reconstructed via an
implementation of the inverse Radon transform, for example, with the
filtered back-projection scheme. Alternatively, in single particle
analysis, a collection of numerous snapshots of objects of the same 3D
structure having random orientations are extracted from one or more
micrographs and transformed via single-particle tomography to provide 
3D structure of the generic object at molecular or near molecular scale.
While the first approach is prone to reconstruction artifacts and
focuses on wider scale phenomena involving many biological entities, the
latter offers high-resolution details on the molecular structure of
simple small individual objects. The development of TxBR has enabled a
hybrid method between these two approaches. We have found that given
that proper reconstruction methods are employed a plastic embedded
biological specimen can actually be submitted to a rather substantial
electron beam dosage, through multiple angles of exposure, without
compromising the subsequent reconstruction. Thus the number of electron
micrographs of the same area may be significantly increased by more than
an order of magnitude compared to common practice in ET. Projections may
contribute to a better averaging scheme so higher quality
reconstructions can be produced.The reconstruction method should
incorporate corrections to the possible sample distortions and limit any
processing artifacts. Implementing this method requires highly automated
procedures, both for the data acquisition and the image processing.

#### Fluorescence and Electron Microscopies

A third theme related to molecular scale resolution comes from
fluorescence microscopy. Although the spatial discrimination along the
optical axis is an order of magnitude worse than that afforded by
electron tomography, with superresolution techniques spatial
discrimination between active molecules in the perpendicular plane is
comparable to ET techniques. Because of the chemistry, which is
described in other sections of this proposal, fluorescence microscopy
makes functional and dynamical information available, particularly in
living cells. Unfortunately, because of the specificity, only the active
molecular sites are imaged, which at nanometer resolution, gives images
of isolated points of light.  Staining techniques, can, however, prepare
the sample for electron microscope imaging, and with some effort, sites
associated with fluorescence identified, and the surrounding
ultrastructure revealed for subsequent analysis. Nevertheless, some
part of the information available at the light microscope level is
lost. Preservation and utilization of the coordinates of active points
of light would be useful on several levels during the process of
reconstruction and analysis. This is particularly true in cases where
large scale imaging and reconstruction is necessary for the elucidation
of extended spatial structure and the statistical analysis of large
numbers of ultrastructural components.

#### Coordinated Microscopies

As an initial essay in the arena of coordinated light and electron
microscopy (LM and EM) we have identified two key areas where LM
information would be useful. The first area is in the alignment of EM
images for 3D reconstruction, and the assembly of many reconstructions
for montaging and (possibly) assembly of serial sections. Fluorescence
can outline extended structures, and this information can be used to
supplement or replace the usual alignment data afforded by deposited
particles. The second area of application is the natural extension of
these ideas to the post reconstruction analysis. Pointwise outlines
afforded by light microscope data can be of use in segmentation, and the
coordinatization of the active sites has applications in
stereology. One immediate question is whether all of the
ultrastructural components of a given species carry the active sites
identified by LM. The scale of the data processing problem posed by the
analysis of whole or multicellular data at the molecular level is
somewhat daunting. The incorporation of information from LM should
simplify or streamline the data processing task at subsequent steps in
the workflow from LM to EM to reconstruction and finally to the analysis
and assembly of statistical data. Without constraining the volume of
the data in some fashion, many of the data processing problems posed by
spatial systems biology are in the exascale range. Clever application
of the information from LM may reduce the magnitude of the task by
orders of magnitude.

TxBR is available for download from the NCMIR web site. The most recent
version is fully automated for use with samples incorporating gold bead
markers. This software can be used to assemble large volumes through a
combination of serial sectioning amd montaging techniques. Modules for
alignment on internal structure, noise reduction and artifact
suppression are under development, with plans to add these to the
package in 2012. Iterative techniques based on curvilinear
backprojection are also under development at NBCR and NCMIR.

### Related Links

[National Biomedical Computation
Resource](http://www.nbcr.net "http://www.nbcr.net")

[National Center for Microscopy Imaging
Research](http://ncmir.ucsd.edu "http://ncmir.ucsd.edu")

[National Center for Research
Resources](http://www.ncrr.nih.gov "http://www.ncrr.nih.gov")

[NBCR Summer Institute 2008](http://nbcr.ucsd.edu/si2008 "http://nbcr.ucsd.edu/si2008")

[Calit2](http://www.calit2.net "http://www.calit2.net")

[UCSD](http://www.ucsd.edu "http://www.ucsd.edu")

### References of Interest

[The Landscape of Parallel Computing
Research](http://view.eecs.berkeley.edu/wiki/Main_Page "http://view.eecs.berkeley.edu/wiki/Main_Page")

[HPC Wire Interview of two authors of The View from
Berkeley](http://www.hpcwire.com/features/17897779.html "http://www.hpcwire.com/features/17897779.html")

#### Electron Microscope Tomography

[National Center for Microscopy and Imaging
Research](http://ncmir.ucsd.edu/ "http://ncmir.ucsd.edu/")

[Tomography at NCMIR 2009](/images/tomo/Tomography-at-ncmir.pdf "/images/tomo/Tomography-at-ncmir.pdf")

[Problems in Tomography](/images/tomo/Problems-in-tomography.pdf "/images/tomo/Problems-in-tomography.pdf")

[The Boulder Laboratory for 3-D Electron Microscopy of Cells](http://bio3d.colorado.edu/ "http://bio3d.colorado.edu/")

[Electron Tomography](http://books.google.com/books?hl=en&id=LWx6JKQy34AC&dq=joachim+frank+tomography&printsec=frontcover&source=web&ots=RkQO3wqqzQ&sig=B5uf4oYKwarE8ANn3SINvwztUtg&sa=X&oi=book_result&resnum=10&ct=result "http://books.google.com/books?hl=en&id=LWx6JKQy34AC&dq=joachim+frank+tomography&printsec=frontcover&source=web&ots=RkQO3wqqzQ&sig=B5uf4oYKwarE8ANn3SINvwztUtg&sa=X&oi=book_result&resnum=10&ct=result")

[Transform Based
Backprojection](http://www.sciencedirect.com/science?_ob=ArticleURL&_udi=B6WM5-4J90V13-2&_user=4429&_rdoc=1&_fmt=&_orig=search&_sort=d&view=c&_acct=C000059602&_version=1&_urlVersion=0&_userid=4429&md5=4099c9e79d6a55ea7bd89ddfa56bd564 "http://www.sciencedirect.com/science?_ob=ArticleURL&_udi=B6WM5-4J90V13-2&_user=4429&_rdoc=1&_fmt=&_orig=search&_sort=d&view=c&_acct=C000059602&_version=1&_urlVersion=0&_userid=4429&md5=4099c9e79d6a55ea7bd89ddfa56bd564")

[Local Tomography in Electron
Microscopy](http://www.tufts.edu/~equinto/research/etarticle.pdf "http://www.tufts.edu/~equinto/research/etarticle.pdf")

[Inversion of the X-ray transform from limited angle parallel beam
region of interest data with applications to electron
tomography](http://www.tufts.edu/~equinto/research/ICIAM-paper-2007-09-06.pdf "http://www.tufts.edu/~equinto/research/ICIAM-paper-2007-09-06.pdf")

[Xmipp, "X-Window-based Microscopy Image Processing
Package"](http://xmipp.cnb.csic.es/ "http://xmipp.cnb.csic.es/")

#### Lambda Tomography

A. Faridani, D. V. Finch, E. L. Ritman, and K. T. Smith, Local
tomography II, SIAM J. Appl. Math., 57 (1997), pp. 1095-1127.

A. Faridani, E. L. Ritman, and K. T. Smith, Local tomography, SIAM J.
Appl. Math., 52 (1992), pp. 459-484.

#### Tracking

[Markov Random Field Methods]
(http://www.robotics.stanford.edu/~galel/papers/ElidanRaptor.pdf "http://www.robotics.stanford.edu/~galel/papers/ElidanRaptor.pdf")

[Belief Propagation]
(http://www.merl.com/papers/docs/TR2001-22.pdf "http://www.merl.com/papers/docs/TR2001-22.pdf")

[Pattern Recognition and Machine Learning]
(http://research.microsoft.com/~cmbishop/PRML/index.htm "http://research.microsoft.com/~cmbishop/PRML/index.htm")
Figure downloads, chapter 8 text.

#### Bundle Adjustment

[Euclidean Reconstruction from almost Uncalibrated
Cameras](http://citeseer.ist.psu.edu/6305.html "http://citeseer.ist.psu.edu/6305.html")

[Bundle Adjustment-A Modern
Synthesis](http://lear.inrialpes.fr/people/triggs/pubs/Triggs-va99.pdf "http://lear.inrialpes.fr/people/triggs/pubs/Triggs-va99.pdf")

#### Parallel Processing

[Graphics Processor
Units](http://www.nvidia.com/cuda "http://www.nvidia.com/cuda")

[The Telescience
Project](http://telescience.ucsd.edu/docs/tele_ggf14.pdf "http://telescience.ucsd.edu/docs/tele_ggf14.pdf")

#### Mathematical Foundations

G. Beylkin, The Inversion Problem and Applications of the Generalized
Radon Transform. Comm. Pure Appl. Math., 1984, 37, 579-599

J. Bruning and V. W. Guillemin, Mathematics Past and Present, Fourier
Integral Operators, Springer-Verlag, Berlin, 1994.

L Ehrenpreis, "The Universality of the Radon Transform", Clarendon Press, Oxford, 2003.

O. Faugeras and Q.-T. Luong, The Geometry of Multiple Images, MIT Press, Cambridge Mass, 2001.

I. M. Gelfand, S. G. Gindinkin and M. I. Graev, Selected Topics in
Integral Geometry, American Mathematical Society, Providence, Rhode Island, 2003.

V. Guillemin, On Some Results of Gelfand in Integral Geometry, Proc.
Symp. Pure Math., 43, 1985, pp. 149-155.

F. W. Hawkes and E. Kaspar, "Wave Optics", Academic Press, San Diego, 1994.

F. Natterer and F. Wuebbeling, "Mathematical Methods in Image Reconstruction", SIAM, Philadelphia, 2001.

V. P. Palamodov, "Reconstructive Integral Geometry", Birkhäuser, 2004

V. P. Palamodov, "A uniform Reconstruction Formula in Integral
Geometry", Arxiv, November 11, 2011.

E. T. Quinto, "An Introduction to X-ray Tomography and Radon Transforms", Proc. Symp. Pure Math., 67 2006, pp. 1-24.

H. Romer, "Theoretical Optics", Wiley-VCH, Weinheim, 2005.

A. G. Ramm and A. I. Katsevich, "The Radon Transform and Local
Tomography", CRC Press, New York, 1996.

V. A. Sharafutdinov, "Integral Geometry of Tensor Fields", VSP, Utrecht,
The Netherlands, 1994.

G. Uhlman, editor, "Inside Out", MSRI Publications, Cambridge University
Press, 2003.

V. V. Volchkov, "Integral Geometry and Convolution Equations", Kluwer
Academic Publishers, Dordrecht, 2003.

#### Regularization Methods

High noise, low contrast images require special treatment. This is
especially true when EM tomography is used to elucidate structure at the
level of protein complexes. [Regularization
methods](/images/tomo/Regularization-methods.pdf "/images/tomo//Regularization-methods.pdf")
have proven to be especially effective when dealing with ill-posed
problems with additional unknown parameters. Thanks to Ozan Oktem for this material.

#### Meetings of Interest to Tomographers

Mathematical Sciences Research Institute August-December 2010 [Program on Inverse Problems and Applications]
(http://www.msri.org/calendar/programs/ProgramInfo/260/show_program "http://www.msri.org/calendar/programs/ProgramInfo/260/show_program").

Isaac Newton Institute for Mathematical Sciences July-December 2011 [Program on Inverse Problems]
(http://www.newton.ac.uk/programmes/INV/index.html "http://www.newton.ac.uk/programmes/INV/index.html")

7th International Electron Tomography Conference Conference 2014
[Ultrastructural
Biology](http://www.zingconferences.com/index.cfm?page=conference&intConferenceID=96&type=conference "http://www.zingconferences.com/index.cfm?page=conference&intConferenceID=96&type=conference")

#### Recent Presentations on EM Tomography

[Tutorial on Large Field Electron Microscope Tomography, Part I]
(/images/tomo/Tutorial-large-field-part1.pdf "/images/tomo//Tutorial-large-field-part1.pdf"),
presented at IEEE Symposium on Biomedical Imaging, Boston, Massachusetts, June 28, 2009.

[Tutorial on Large Field Electron Microscope Tomography, Part II]
(/images/tomo/Tutorial-large-field-part2.pdf "/images/tomo/Tutorial-large-field-part2.pdf"),
presented at IEEE Symposium on Biomedical Imaging, Boston, Massachusetts, June 28, 2009.

[Large Field and High Resolution Electron Microscope Tomography]
(/images/tomo/Large-field.pdf "/images/tomo/Large-field.pdf"),
presented at Banff workshop 09w5017: Mathematical Methods in Emerging Modalities of Medical Imaging, Oct 25 - Oct 30, 2009.

[Recent Developments in Large Scale Electron Microscope Tomography]
(/images/tomo/Tutorial-large-field-part2.pdf "/images/tomo/Tutorial-large-field-part2.pdf"),
presented at the NBCR Tech Series: Multiscale and Multi-Physics Tools
for Mesoscale Modeling of Heart Diseases using Realistic Geometry, November 18 2010

Sixth International Congress on Electron Tomography 2011 [Cryo-Electron
Tomography](http://www.bscb.org/?url=newsletter/winter2011/m6tomography "http://www.bscb.org/?url=newsletter/winter2011/m6tomography")

### Participants

Abel Lin, NCMIR, University of California, San Diego

Adel Faridani, [Oregon State University](http://oregonstate.edu/~faridana/ "http://oregonstate.edu/~faridana/")

Alexandre Cunha, California Institute of Technology

Andreas Rieder, [Mathematics, Universität
Karlsruhe](http://www.mathematik.uni-karlsruhe.de/ianm3/~rieder/en "http://www.mathematik.uni-karlsruhe.de/ianm3/~rieder/en")

Bill Tivol, California Institute of Technology

Farshid Moussavi, Stanford University

Fernando Amat, [Stanford University](http://www.stanford.edu/~famat/ "http://www.stanford.edu/~famat/")

Hans Rullgard, [Mathematics, Stockholm
University](http://www2.math.su.se/~hansr/index.html.en "http://www2.math.su.se/~hansr/index.html.en")

James Bouwer, NCMIR, University of California, San Diego

Jane Ding, California Institute of Technology

Jian Shi, California Institute of Technology

Laurent Desbat, TIMC-IMAG, Joseph Fourier University of Grenoble

Mariana Tihova, City of Hope

Mark Ellisman, [NCMIR, University of California, San Diego](http://cancer.ucsd.edu/summaries/mellisman.asp "http://cancer.ucsd.edu/summaries/mellisman.asp")

Mart Malle, Computer Science, University of California, Riverside

Masako Terada, NCMIR, University of California, San Diego

Michael Holst, [Mathematics, University of California, San Diego](http://ccom.ucsd.edu/~mholst/ "http://ccom.ucsd.edu/~mholst/")

Neal Young, Computer Science, University of California, Riverside

Peter Arzberger, NBCR, University of California, San Diego

Raj Singh, NCMIR, University of California, San Diego

Rick Giuly, NCMIR, University of California, San Diego

Ryan Hass, Mathematics, Oregon State Univeristy

Sebastien Phan, NCMIR, University of California, San Diego

Stephen Larson, NCMIR, University of California, San Diego

Steve Peltier, NCMIR, University of California, San Diego

Thomas Payne, [Computer Science, University of California, Riverside](http://www.engr.ucr.edu/faculty/cs/tompayne.html "http://www.engr.ucr.edu/faculty/cs/tompayne.html")

Todd Quinto, [Mathematics, Tufts University](http://www.tufts.edu/~equinto/ "http://www.tufts.edu/~equinto/")

Wilfred Li, [NBCR, University of California, San Diego](http://www.sdsc.edu/~wilfred/ "http://www.sdsc.edu/~wilfred/")

Zeyun Yu, [Mathematics, University of California, San Diego](http://ccom.ucsd.edu/~zeyun/ "http://ccom.ucsd.edu/~zeyun/")

### Contacts

Albert Lawrence albert (dot) rick (dot) lawrence {at} gmail {dot} com, Sebastien Phan sph {at} ncmir {dot} ucsd {dot} edu

### Special Thanks

Peter Arzberger and Mark Ellisman for organizational support.

