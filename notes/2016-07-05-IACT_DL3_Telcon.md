# 2016-07-05 - Monthly IACT DL3 telcon

* Tuesday, July 5, 2016 at 11 am CEST
* Duration: 1 hour
* Participants: 

## Connection details

If you have questions how to connect, please email [Catherine Boisson]
(http://www.iau.org/administration/membership/individual/7665/)

Connection from a single terminal:
* http://desktop.visio.renater.fr/scopia?ID=724011***3757&autojoin

Otherwise:

* Telephone +33 (0)4 26 68 73 07
* GDS     	+33 (0)4 26 68 73 07 727454
* SIP     	sip:727454@195.98.238.109 (via e.g. ekiga or linephone with Linux)
* H.323     h323:727454@mgmt.visio.renater.fr
* Conference number    724011 (end by #)
* Password             3757   (end by #)


Conference
Title 	2016 July 5 IACT DL3
Begin 	05/07/2016 11:00 (GMT +2 Europe/Paris)
Duration 	02:00

## Agenda

### Status updates

* Christoph gave a presentation on "Open data and tools for gamma-ray astronomy"
  ([PDF](http://www.g-vo.org/edp-forum-2016/slides/deil-opengamma.pdf))
  * Feedback: for sustainability fo the open gamma-ray astronomy spec effort,
    consider forming a VO interest or working group.
    * This was discussed over lunch with Catherine Boisson, Mathieu Servillat and
      Christoph Deil and it wasn't clear to us if forming such an official group
      would help with organisation and sustainability.
    * No plan to pursue this for now.
  * Feedback: consider using [IVOA DataLink](http://www.ivoa.net/documents/DataLink/)
    for IACT DL3 data links (e.g. link EVENTS to IRFs).
    * "This document describes the linking of data discovery metadata to access
       to the data itself, further detailed metadata, related resources,
       and to services that perform operations on the data."
    * Let's discuss today if this is an option worth looking into more
      (more info below).
* Spec updates
  * Very little progress in the past month.
  * https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/pulls?q=is%3Apr+is%3Aclosed
  * Everyone: if you want to make some addition or change, please try to
    make a pull requests, i.e. concrete proposal, instead of "just" an issue.
* Christoph: I haven't gotten around to making the
[Gamma 2016 conference poster for open-gamma-ray-astro](https://github.com/open-gamma-ray-astro/open-gamma-ray-astro-gamma2016).
I'll try to do it tonight or tomorrow latest and then circulate for feedback.
* Update on MAGIC DL3 activities
* Next monthly IACT DL3 telcons:
  * Tuesday, August 2, 2016 at 11 am CEST
    * Who is available? Should we skip that one or do it?
  * Tuesday, September 6, 2016 at 11 am CEST

### To be discussed

* Open pull requests and issues:
  * [PR 40: Add script to generate event template file, add also template file.](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/pull/40)
  * [PR 61: Add light curve spec (a first draft)](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/pull/61)
    * See discussion on how to handle different quantities / units for that application.
    * This is DL4, but still, the main question is how different quantities
      (differential flux, integral flux, energy flux) should be supported and
      whether units should be flexible or fixed.
    * Options for different quantities:
      A. one column "flux" and header key declaring which quantity it is
      B. three columns, requirement is that one out of three is present.
  * [Issue 63: Consistent column names within IRFs](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/63)
  * Any progress / anything actionable on the question how to deal with livetime
    in DL3 that we already discussed in the last telcon?
    * [Issue 52: Where to put livetime info in IACT DL3?](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/52)
    * [Issue 62: How to handle energy dependent deadtime/livetime?](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/62)
* IACT DL3 data link via an XML file?
  * An XML VOTable file.
  * Could maybe replace what we do now to link HDUs
    ([data store in the spec ](http://gamma-astro-data-formats.readthedocs.io/en/latest/data_storage/))
    which was controversial at the f2f meeting and is probably not the final solution.
  * ctools are using the "observation definition" XML files that connect events / IRFs.
    How is this the same or different from VO DATALINK?
    Should we adopt it?
  * An alternative could be to use the FITS grouping convention, where the linking
    info is in an extra table HDU.
* How IRF arrays should be filled / used for invalid parameter ranges (e.g. low energy).
  * Spec doesn't say at the moment, we have some threshold keywords.
  * In HESS we sometimes fill zeros, sometimes `NaN` values.
  * This is important, science tools need to know what cuts to apply.
    See e.g. https://github.com/gammapy/gammapy/issues/589

## Minutes

* tbd
