# 2016-06-07 - Monthly IACT DL3 telcon

* Tuesday, June 7, 2016 at 11 am CEST
* Duration: 1.5 hour
* Participants: Catherine Boisson, Jürgen Knödlseder, Tarek Hassan, Christoph Deil

## Connection details

If you have questions how to connect, please email [Catherine Boisson]
(http://www.iau.org/administration/membership/individual/7665/)

Connection from a single terminal:
* http://desktop.visio.renater.fr/scopia?ID=724922***2763&autojoin

Otherwise:

* Telephone +33 (0)4 26 68 73 07
* GDS         +33 (0)4 26 68 73 07 727454
* SIP         sip:727454@195.98.238.109 (via e.g. ekiga or linephone with Linux)
* H.323     h323:727454@mgmt.visio.renater.fr
* Conference number    724922 (end by #)
* Password             2763 (end by #)

Conference
Title     2016 June 7 IACT DL3
Begin     07/06/2016 11:00 (GMT +2 Europe/Paris)
Duration     02:00

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

* Organisation: Christoph didn't send reminders, that's why there were so few
  participants. Will send announcements and reminders for next monthly IACT DL3
  telcon to CTA-DATA and OPEN-GAMMA-RAY-ASTRO mailing lists.
* We agree to put back `RA_PNT` and `DEC_PNT` in the `EVENTS` header for now,
  and add a note that DL3 producers and consumers should implement the new
  `POINTING` table, which will likely be the long-term solution for this info.
* Where to put livetime info in DL3?
    * This is a key quantity used by most science analyses
      (flux is roughly excess over livetime)
      so it's important to handle this well in the DL3 data model.
    * Christoph explains how it's computed in HESS: consecutive event time
      difference distribution is fitted with an exponential model and that
      is used to estimate the dead-time fraction `DEADC`.
      Then `LIVETIME = DEADC * ONTIME` where ontime is the observation time.
      So this method needs a certain time interval to compute, the length of
      which depends on the array and trigger rate.
      For HESS, it's stable for our 28 min runs, although I'm not sure if e.g.
      the ParisAnalysis calibration doesn't use shorter time intervals.
      I don't know how other IACTs compute it or how CTA will compute it.
    * For now we'll keep it as a header keyword in ``EVENTS``, but storing
      ``LIVETIME`` as a column in the ``GTI`` table seems like a good solution
      to most (all?) telcon participants.
    * Action item (for Jürgen): inquire in CTA if something is known
      about how livetime computation will be done already.
* FOV coordinates
    * We had a long discussion:
        * Christoph insists on a change to the spec now,
          to have something well-defined for the upcoming HESS data release.
        * Jürgen isn't happy with having both ALTAZ and RADEC aligned FOV coordinates
          in the spec ("too much systems to potentially have to support by tools")
        * Tarek would like to have something more flexible for IRF axes, where
          the current ``BKG_2D`` and ``BKG_3D`` are only different configurations
          of one background model spec.
    * Action items (for Christoph): in the end we agreed on this for now:
        * Define ``BKG_3D`` to be in the ALTAZ aligned FOV system.
        * Keep the simple ``DETX, DETY`` names for those.
        * Make ``DETX, DETY`` optional in the ``EVENTS`` list.
        * Simplify the FOV coordinate general section (don't spec names for RADEC FOV).
* Data type specification
    * The discussion is mostly about 32 and 64 bit floats.
    * In the current spec, ``TIME`` needs to be 64 bit, for the others
      and most (all?) use cases, 32 bit is enough.
    * Christoph prefers to have "float" for most columns with the meaning that
      both 32-bit and 64-bit are valid. The column datatype is in the FITS header
      and FITS tools can process either without extra effort.
      Being flexible here has two advantages: 1. no need to make decisions for every
      single field in the spec now. 2. there can be cases like ``RA / DEC`` where
      for most data 32-bit is sufficient and means smaller file size, but
      64-bit can be useful sometimes e.g. for high-precision checks (I had this
      case this morning). It would be nice if an EVENTS list with 64-bit ``RA/DEC``
      is still a valid file according to the spec.
    * Jürgen and Tarek don't see the need for flexibility here and prefer to have
      everything fixed (to 32 bit, except for TIME which is 64 bit)
    * A more cosmetic controversial issue was on whether to write "float32" and
      "float64" or the FITS ttype codes "1E" and "1D" everywhere in the spec.
    * Christoph prefers "floatXX" (more human-readable and what's displayed by 
      tools like e.g. Astropy Table), Jürgen and Tarek FITS ttype codes
      (because that's what you have to know when writing C/C++ code based on CFITSIO
      and that is also what's displayed by tools like FTOOLS)
    * Action item (for Christoph): agree to be explicit about 32 vs 64 bit and
      put FITS ttype codes for now.
* Units
    * Jürgen thinks units should be fixed (mainly to simplify usage by tools)
    * Christoph and Tarek think that it would be nice to be flexible here
      (e.g. Fermi uses MeV and IACTs use TeV) and take advantage of the fact
      that FITS supports encoding the unit in the FITS header.
    * So no agreement on this point (and the discussion wasn't very long).
    * Action item (for Christoph): for now, we'll stick with units as specified in the spec,
      and add a note in the general section that it's not clear / agreed if
      units will be fixed or flexible.
