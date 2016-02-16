# IACT DL3 meeting in Meudon in April 2016

## Contact

If you have any questions or suggestions, or would like to attend, please
contact [Catherine
Boisson](http://www.iau.org/administration/membership/individual/7665/) and
[Christoph Deil](https://github.com/cdeil).

## When?

* Start: 10 am on Wednesday, April 6, 2016
* End: noon on Friday, April 8, 2016

* Pre-meeting planning telcon: tbd (set up Doodle)
* Post-meeting follow-up telcon: tbd (will be scheduled at the f2f meeting)

## Where?

Observatoire de Meudon

## Introduction

This two-day face-to-face meeting will bring together people
from existing IACTs (imaging atmospheric Cherenkov telescopes) such as H.E.S.S.,
VERITAS, MAGIC, ASTRI, FACT, ... as well as the next-generation Cherenkov telescope
array (CTA) interested in data level 3 (DL3). 

The ["Cherenkov Telescope Array Data Management" proceeding from ICRC 2015](http://adsabs.harvard.edu/abs/2015arXiv150901012L) explains what DL3 is:

> ... high-level observatory products comprised of selected gamma-like events,
instrument response tables, and housekeeping data (DL3). DL3 data will have a
total volume of about 2% of the DL0 data volume and guaranteed access will be
provided in the CTA archive to basic users (e.g. Guest Observers and Archive
Users).

Very roughly DL3 is what most users will download and analyse with science tools,
similar to how Fermi-LAT data is distributed.

Most of the existing IACTs have started efforts to export their event data and
instrument response functions (IRFs) at the DL3 level to FITS formats and
there are some open-source science tools able to analyse it.

But so far no DL3 data model and data format specifications have been produced,
making collaboration difficult!

There are some efforts to write documents within CTA. For the effort on IRFs
see the
["The Instrument Response Function Format for the Cherenkov Telescope Array" proceeding from ICRC 2015](http://adsabs.harvard.edu/abs/2015arXiv150807437W).
In fall 2015 a few people from H.E.S.S. started writing down an open spec of the
formats they use at [gamma-astro-data-formats](http://gamma-astro-data-formats.readthedocs.org/en/latest/). These formats are (mostly, except for recent extensions) supported by Gammapy and Gammalib/ctools and are similar to the ones used by VERITAS.

## Goals

The main goal of this meeting is to work on the DL3 data model and formats.

* Present [gamma-astro-data-formats](http://gamma-astro-data-formats.readthedocs.org/en/latest/) and other preliminary formats in use.
* Gather use cases and see which ones are possible / not possible with the existing formats.
* Extend existing formats or create new ones that cover more (all?) use cases.
* Write down open specs (so that they are visible by all, not just CTA members) that can form the basis for prototyping for the next months
for data producers (mainly existing IACTs and simulated CTA data) and consumers
(mainly science tool codes).

Finding a good data model and format and getting community adoption will be an
ongoing task for the coming years. This meeting is just an attempt to speed up
the process. The goal is not to "produce and decide on final formats".

## Agenda

### Wednesday afternoon

* Presentations: tbd (please let us know if you'd like to present something!)
* Plenary discussion session

## Thursday

* Split out into small working groups on sub-topics?

## Friday morning

* Summary from the sub-groups and discussion.
* Identify action items: who does what after the meeting?

## Participants

* Christoph Deil
* Catherine Boisson
* Tarek Hassan
* (if your name isn't here yet, but you'd like to attend, please let us know!)
