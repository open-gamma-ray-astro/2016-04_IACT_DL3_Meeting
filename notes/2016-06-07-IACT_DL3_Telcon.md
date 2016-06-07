# 2016-06-07 - Monthly IACT DL3 telcon

* Tuesday, June 7, 2016 at 11 am CEST
* Duration: 1 hour
* Participants: 

## Connection details

If you have questions how to connect, please email [Catherine Boisson]
(http://www.iau.org/administration/membership/individual/7665/)

Connection from a single terminal:
* http://desktop.visio.renater.fr/scopia?ID=724922***2763&autojoin


Otherwise:

* Telephone +33 (0)4 26 68 73 07
* GDS     	+33 (0)4 26 68 73 07 727454
* SIP     	sip:727454@195.98.238.109 (via e.g. ekiga or linephone with Linux)
* H.323     h323:727454@mgmt.visio.renater.fr
* Conference number    724922 (end by #)
* Password             2763 (end by #)


Conference
Title 	2016 June 7 IACT DL3
Begin 	07/06/2016 11:00 (GMT +2 Europe/Paris)
Duration 	02:00


## Agenda

### Status updates

* Jürgen gave a "DL3 IACT meeting report" at the Kashiwa CTA meeting (see slides [here](https://www.cta-observatory.org/indico/contributionDisplay.py?contribId=60&sessionId=10&confId=1046))
* Christoph submitted a poster contribution "Open high-level data formats and software for gamma-ray astronomy" for [Gamma 2016](https://www.mpi-hd.mpg.de/hd2016/pages/news.php) (see abstract
[here](https://github.com/open-gamma-ray-astro/open-gamma-ray-astro-gamma2016))
* Pull request by Tarek: [Modified effective area format. EFFAREA_RECO column moved to a new HDU. #43](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/pull/43) after long discussion in [#39](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/35)
  * See http://gamma-astro-data-formats.readthedocs.io/en/latest/irfs/effective_area/index.html#effective-area-vs-reconstructed-energy
  * If ``EFFAREA_RECO`` (the combined ``EFFARA`` and ``EDISP`` response) is given, it should be a separate HDU.
  * Science tools should use the header key ``HDUCLAS2`` keyword to know what kind of response this is ()``EFF_AREA`` vs ``EFF_AREA_RECO``)
* Pull request by Jürgen: [Change EVENTS and add POINTING #39](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/pull/39)
  * Clean up ``EVENTS`` spec
  * Add [POINTING](http://gamma-astro-data-formats.readthedocs.io/en/latest/events/pointing.html) table
  * Merged yesterday, some controversial things delayed to other issues (see "to be discussed" below).
* Misc clean-up by Christoph
* Some work on [high-level specs](http://gamma-astro-data-formats.readthedocs.io/en/latest/results/index.html)
  (not the topic here):
  * Flux point and bin-by-bin likelihood profile specs by Matthew Wood (discussion still ongoing in [issue 45](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/45))
  * Model specification proposal by Jürgen (see [issue 41](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/41))

### To be discussed

* Where to put livetime info in IACT DL3? (see [issue 52](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/52))
* New EVENTS spec
  * See [here](http://gamma-astro-data-formats.readthedocs.io/en/latest/events/index.html) and [here](http://gamma-astro-data-formats.readthedocs.io/en/latest/events/events.html)
  * Christoph proposes to change back two things that were changed in [#39](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/pull/39):
    * Add back `RA_PNT` and `DEC_PNT` header keywords
    * Make FOV coordinate columns ``DETX``, ``DETY`` optional
* FOV coordinate proposal
  * See current description in spec [here](http://gamma-astro-data-formats.readthedocs.io/en/latest/general/coordinates.html#field-of-view)
  * This is a proposal, up for debate today.
  * Use these names for EVENTS columns and BKG_3D IRF axes?
* Data type specification
  * Most of the spec uses "float" which means any float is valid.
    Where 64-bit is required (rarely, mostly for TIME), we write "float64".
  * For the EVENTS spec integer FITS codes like "1J", "1D", "1E"
    were introduced (see [here](http://gamma-astro-data-formats.readthedocs.io/en/latest/events/events.html))
  * Data type specifiers should be uniform throughout the spec.
* Units
  * Are we agreed that units shouldn't be hard-coded and science tools should read
    units from the files (also e.g. for IRFs)?
  * How to specify "physical dimensions" instead of "units" in the spec?
    (see discussion [here](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/45#issuecomment-220962019))?

## Minutes

* tbd
