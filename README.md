# IACT DL3 meeting in Meudon in April 2016

## Contact

If you have any questions or suggestions, or would like to attend, please
contact [Catherine
Boisson](http://www.iau.org/administration/membership/individual/7665/) and
[Christoph Deil](https://github.com/cdeil).

## When?

* Start: 10 am on Wednesday, April 6, 2016
* End: noon on Friday, April 8, 2016

* Pre-meeting planning telcon: tbd, Doodle will be set up soon.
* Post-meeting follow-up telcon: tbd (will be scheduled at the f2f meeting)

## Where?

Observatoire de Paris, site de Meudon, 
Place J. Janssen, 92190 - Meudon

The meeting will be held in the conference room, downstairs of Builging 9, the "big dom". See the [access map](https://www.obspm.fr/acces-au-site-de-meudon.html?lang=en)

Practical informations:
A list of a few convenient hotels in Paris can be found [here](http://lesia.obspm.fr/List-of-some-convenient-hotels.html)
The selected hotels are close to Gare Montparnasse serving Meudon SNCF train Meudon and Bellevue stations or close to RER C stop (regional line) serving Meudon Val Fleury RER station.

From the train stations in Meudon, the Observatory is about 20 minutes walk uphill, whatever the station.  From the SNCF station "Bellevue" (in Meudon) to the Observatory you may catch the 9:20 am bus, TIM, going up to the Observatory. Your next chance is one hour later... 

Taxi in Meudon
"Central taxis", 24h/24h, 7d/7d  : 0146309012  or  0673385301


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

* Start with summary presentations on DL3 in the various IACTs and codes that produce or consume DL3 data and IRFs.
* Gather use cases and see which ones are possible / not possible with the existing formats.
* Extend existing formats or create new ones that cover more (all?) use cases.
* Write down open specs (so that they are visible by all, not just CTA members, e.g. at [gamma-astro-data-formats](http://gamma-astro-data-formats.readthedocs.org/en/latest/)) that can form the basis for prototyping for the next months for data producers (mainly existing IACTs and simulated CTA data) and consumers (mainly science tool codes).

Finding a good data model and format and getting community adoption will be an
ongoing task for the coming years. This meeting is just an attempt to speed up
the process. The goal is not to "produce and decide on final formats".

## Agenda

### Wednesday afternoon

We'll start the meeting with a series of short presentations, to make sure everyone's aware of the status of existing efforts.

Confirmed:

* Catherine Boisson - Welcome, logistics
* Tarek Hassan - Proposed DL3 IRF format and prototype code (not public yet)
* Christoph Deil - open-gamma-ray-astro [mailing list](https://lists.nasa.gov/mailman/listinfo/open-gamma-ray-astro), [Github org](https://github.com/open-gamma-ray-astro) and [gamma-astro-data-format](http://gamma-astro-data-formats.readthedocs.org/en/latest/) specs.
* Jürgen Knödlseder - DL3 in [Gammalib](http://cta.irap.omp.eu/gammalib/) and  [ctools](http://cta.irap.omp.eu/ctools/)

Ideas:

* Maybe - DL3 in [Gammapy](https://gammapy.readthedocs.org/en/latest/)
* Wanted: status of DL3 data export from HESS, VERITAS, MAGIC, FACT, ASTRI
* Wanted: short presentations of use cases or "I think we should do this for DL3 ..."
* (if you'd like to give a presentation, please let uns know!)

* Plenary discussion session

## Thursday

* Split out into small working groups on sub-topics?

## Friday morning

* Summary from the sub-groups and discussion.
* Identify action items: who does what after the meeting?

## Participants

* [Catherine Boisson](https://github.com/cboisson)
* [Christoph Deil](https://github.com/cdeil)
* Immacolata Donnarumma
* [Jürgen Knödlseder](https://github.com/jknodlseder)
* [Tarek Hassan](https://github.com/TarekHC)
* (if your name isn't here yet, but you'd like to attend, please let us know!)

(alphabetical order by first name)
