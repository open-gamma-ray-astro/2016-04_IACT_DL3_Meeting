# Meeting

This page contains info about the face-to-face meeting.

## When?

* Face-to-face meeting
    * Start: 11 am on Wednesday, April 6, 2016
    * End: noon on Friday, April 8, 2016
* Pre-meeting planning telcon:
    * Purpose: plan the f2f meeting
    * March 29, 2016 at 6 pm CEST
    * Agenda and notes at [pre-meeting-telcon.md](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/notes/pre-meeting-telcon.md).
* Post-meeting follow-up telcon:
    * Purpose: wrap up and follow-up for the f2f meeting
    * Tuesday, April 26, 2016 at 11 am CEST
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

## Thursday

Start: **9 am**

The rest of Thursday was use for discussions and planning.

## Friday

Start: **9 am**

* Continue discussions from yesterday.
* What's process, goal and timescale for version 1.0 of the spec?
* Identify action items: who does what after the meeting until when?
* Is Github communication and one follow-up telcon enough, or do we want
  dedicated follow-up telcons on sub-topics to increase chances of quick
  progress and convergence on the things discussed here?
* Schedule the date / time for the [post-meeting-telcon.md](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/notes/post-meeting-telcon.md).
* Present summary of this meeting in some CTA telcon soon?

## Participants

(alphabetical order by first name)

1. [Bruno Khelifi](https://github.com/bkhelifi)
1. [Catherine Boisson](https://github.com/cboisson)
1. [Christoph Deil](https://github.com/cdeil)
1. [Daniela Dorner](https://github.com/dadorner)
1. [Gernot Maier](https://github.com/GernotMaier)
1. [Giovanna Pedaletti](https://github.com/gpedalet)
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
