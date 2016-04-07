# IACT DL3 meeting in Meudon in April 2016

## Contact

If you have any questions or suggestions, or would like to attend, please
contact [Catherine Boisson](http://www.iau.org/administration/membership/individual/7665/) and
[Christoph Deil](https://github.com/cdeil).

## When?

* Face-to-face meeting
    * Start: 11 am on Wednesday, April 6, 2016
    * End: noon on Friday, April 8, 2016
* Pre-meeting planning telcon:
    * Purpose: plan the f2f meeting
    * March 29, 2016 at 6 pm CEST
    * Agenda and notes at [pre-meeting-telcon.md](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/notes/pre-meeting-telcon.md).
* Post-meeting follow-up telcon:
    * Purpose: short reports on action items and activities after the meeting; keep people in contact.
    * Date / time: tbd (will be scheduled at the f2f meeting)
    * Agenda and notes at [post-meeting-telcon.md](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/notes/post-meeting-telcon.md).

## Where?

Observatoire de Paris, site de Meudon, 
Place J. Janssen, 92190 - Meudon

The meeting will be held in the conference room, downstairs of Builging 9, the "big dom". See the [access map](https://www.obspm.fr/acces-au-site-de-meudon.html?lang=en)

Practical informations:
A list of a few convenient hotels in Paris can be found [here](http://lesia.obspm.fr/List-of-some-convenient-hotels.html)
The selected hotels are close to Gare Montparnasse serving Meudon SNCF train Meudon and Bellevue stations or close to RER C stop (regional line) serving Meudon Val Fleury RER station.

There are also a few options to book a room in Meudon within walking distance via [airbnb](https://www.airbnb.com/s/Meudon--France).

From the train stations in Meudon, the Observatory is about 20 minutes walk uphill, whatever the station.  From the SNCF station "Bellevue" (in Meudon) to the Observatory you may catch the 9:20 am bus, TIM, going up to the Observatory. Your next chance is one hour later... 

Taxi in Meudon
"Central taxis", 24h/24h, 7d/7d  : 0146309012  or  0673385301

## No remote participation

There will be no possibility of remote participation for this meeting.

Apologies if you would have liked to join the discussion but can't come!

We have the experience that audio or video remote participation is usually distracting and slowing down the face-to-face discussion.

Note that all presentation slides will be openly available in this repository and we also plan to write minutes for the discussion sessions, to provide a good basis for future online collaboration or meetings on the topic.

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

The main goal of this meeting is to work on the DL3 data model and data formats.

* Start with summary presentations on DL3 in the various IACTs and codes that produce or consume DL3 data and IRFs.
* Gather use cases and see which ones are possible / not possible with the existing formats.
* Extend existing formats or create new ones that cover more (all?) use cases.
* Write down open specs (so that they are visible by all, not just CTA members, e.g. at [gamma-astro-data-formats](http://gamma-astro-data-formats.readthedocs.org/en/latest/)) that can form the basis for prototyping for the next months for data producers (mainly existing IACTs and simulated CTA data) and consumers (mainly science tool codes).

Finding a good data model and format and getting community adoption will be an
ongoing task for the coming years. This meeting is just an attempt to speed up
the process. The goal is not to "produce and decide on final formats".

## Agenda

### Wednesday

Start: **11 am**

* Catherine Boisson - Welcome, logistics
* Flash introductions. Everyone please say within ~ 1 minute who you are,
  what you're working on and what you'd like to work on and achieve at this meeting.

Overview presentations:

* Jürgen Knödlseder - [DL3 for high-energy telescopes - experience from space missions](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/2016-04-06-DL3-experience-jknodlseder.pptx.pdf)
* Catherine Boisson - [IACT data to end users](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/2016-04_IACT_DL3_Meeting_Boisson.pdf)
* Mathieu Servillat - [VO data diffusion for IACTs](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/servillat_VOdiff.pdf)
* Christoph Deil - [Open data model and format specifications for gamma-ray astronomy](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/2016-04_IACT_DL3_Meeting_GammaAstroDataFormats.pdf)
* Tarek Hassan - [Proposed DL3 IRF format and prototype code](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/IRF_format_progress_Tarek_Hassan@Meudon.pdf) ([flexIRF](https://github.com/cta-observatory/flexIRF))
* Gernot Maier - [CTA Monte Carlo Pipeline - A very short overview](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/CTA-20160406-DL3MeetingMCPipeline.pdf)

Experience and status reports from existing IACTs:

* Gernot Maier - [DL3 in VERITAS](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/VTS-20160406-DL3.pdf)
* Giovanna Pedaletti - DL3 in MAGIC
* Daniela Dorner - DL3 in FACT
* Kai Brügge - [FACT data and formats](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/fact-dataformats-and-discussion.pdf)
* Saverio Lombardi - DL3 IRF concept and implementation status in the framework of the ASTRI MINI-ARRAY pipeline
* Christoph Deil - [DL3 in HESS](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/2016-04_IACT_DL3_Meeting_HESS.pdf)

## Thursday

Start: **9 am**

Experience and status from existing open-source codes consuming DL3 data:

* Jürgen Knödlseder - DL3 in [Gammalib](http://cta.irap.omp.eu/gammalib/) and  [ctools](http://cta.irap.omp.eu/ctools/)
* Christoph Deil - DL3 in [Gammapy](https://gammapy.readthedocs.org/en/latest/)

General thoughts on DL3:

* Jaime Rosado and José Luis Contreras - [DL3 data model beyond the IACT community?](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/presentations/Rosado_IACT_DL3_Meudon_April_2016.pdf)
* Jürgen Knödlseder - Thoughts on DL3 for IACTs

This concludes the presentations, the rest of the f2f meeting is very informal.

* Open plenary discussion (1 hour?) to discuss the goals for this meeting
  and the coming months / years.
* Plan parallel work in sub-groups for the afternoon and Friday morning
  * Identify topics for working groups
  * How much time to allocate for each?
  * Everyone puts their name to what they are most interested in.
  * We put a schedule that tries to mininize conflicts of interest.

**12:30 - 2 pm** - Lunch break

**2 pm - 6 pm** - Parallel work in sub-groups

Sub-groups:

* Christoph - FOV coordinates (discussion, followed by spec writing)
* Christoph - Define method of EVENT-IRF association via GTI_ID and EVENT_TYPE
* Tarek? - IRFs

## Friday

Start: **9 am**

**9 am - 11 am**: Parallel work in sub-groups.

Sub-groups:

* Christoph - Open spec organisation (discussion)
  * include DL2?
  * how to organise sub-sections?
  * how to do versioning?
* ...

**11 am - 12:30 pm**: plenary summmary session

* Brief summary reports from sub-groups.
* Identify action items: who does what after the meeting until when?
* Schedule the date / time for the [post-meeting-telcon.md](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/notes/post-meeting-telcon.md).

**12:30** - Lunch

## Participants

(alphabetical order by first name)

1. Antonio Stammera
1. [Bruno Khelifi](https://github.com/bkhelifi)
1. [Catherine Boisson](https://github.com/cboisson)
1. [Christoph Deil](https://github.com/cdeil)
1. [Daniela Dorner](https://github.com/dadorner)
1. [Gernot Maier](https://github.com/GernotMaier)
1. Giovanna Pedaletti
1. [Jaime Rosado](https://github.com/JaimeRosado)
1. José Luis Contreras
1. [Julien Lefaucheur](https://github.com/jjlk)
1. [Jürgen Knödlseder](https://github.com/jknodlseder)
1. [Kai Brügge](https://github.com/mackaiver)
1. [Mathieu Servillat](https://github.com/mservillat)
1. [Régis Terrier](https://github.com/registerrier)
1. Roland Walter
1. Saverio Lombardi
1. [Tarek Hassan](https://github.com/TarekHC)

## How to contribute to this repository?

The main work product from this meeting will be presentation slides presented on Wednesday, as well as notes and documents written collaboratively during the meeting.

We are using this Github repository to gather presentations and notes for this
meeting: https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting

Please help us gather notes, especially summaries of the parallel sessions, and
identified action items for the coming months (for us, and for people that
couldn't come to the meeting).

To contribute, please make a Github account (it only takes a minute and is free)
and make pull requests, adding files to the following folders:

* [notes](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/notes) - Add notes as Markdown ``.md`` files. Use the [notes/template.md](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/notes/template.md) file as a starting point if you like.
* If you want to do collaborative note taking, a Google doc with URL shared via
email or Twitter is a good option (and copy & paste the content over to this repo after).
* [presentations](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/presentations) - Add your presentation in PDF format if you want to present slides.
Or just write down what you want to present in a Markdown file if you prefer.

If you have any questions, ask [Christoph Deil](https://github.com/cdeil) or
other participants that are familiar with Markdown and Github. If you don't want
to use Github, just email files or notes to me and I'll add them to the repo.
