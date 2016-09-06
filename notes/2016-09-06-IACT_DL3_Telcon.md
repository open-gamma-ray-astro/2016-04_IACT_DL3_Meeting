# 2016-09-06 - Monthly IACT DL3 telcon

* Tuesday, September 6, 2016 at 11 am CEST
* Duration: 1 hour
* Participants: Catherine Boisson, Tarek Hassan, Jaime Rosado,
  José Luis Contreras, Daniela Dorner, Christoph Deil, Mathieu Servillat

## Connection details

If you have questions how to connect, please email [Catherine Boisson]
(http://www.iau.org/administration/membership/individual/7665/)

Connection from a single terminal:

    http://desktop.visio.renater.fr/scopia?ID=728394***1339&autojoin

Otherwise:

    IP 	194.214.202.146
    Telephone +33 (0)4 26 68 73 07
    GDS +33 (0)4 26 68 73 07 728394
    SIP sip:728394@195.98.238.109 (via e.g. ekiga or linephone with Linux)
    H.323 h323:728394@mgmt.visio.renater.fr
    Conference number 728394 (end by #)
    Password 1339 (end by #)

Conference Title 2016 September 6 IACT DL3 Begin 05/09/2016 11:00 (GMT +2 Europe/Paris) Duration 02:00

## Agenda

### Status updates

* There hasn't been much progress since the last telcon July 5, 2015,
  due to the summer break. Let's get started again!
* Poster "Open high-level data formats and software for gamma-ray astronomy"
was presented at the Gamma 2016 conference (see [PDF](https://github.com/open-gamma-ray-astro/open-gamma-ray-astro-gamma2016/blob/master/open-gamma-ray-astro-gamma2016.pdf)).
Proceeding due in October, Christoph will write a draft.
A or other IACTs, updates from science tools, anything else)?

### To be discussed

* [Issue 64: Change OBS_ID keyword from integer to string](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/64)
* A second face-to-face meeting to follow up on the one from April 2016
  in Meudon
  * Christoph or Catherine could host in Heidelberg or Paris.
  * Duration: 3 or 4 or 5 days?
  * Focus just on IACT DL3, or also allow (parallel) session on
    * DL4, DL5 format spec
    * Connection to lower-level info, e.g. MC parameters
    * Multi-messenger use cases or how to support e.g. HAWC with similar formats.
    * CTA data challenge
    * anything else?
  * When?
    * October doesn't work (ctapipe, ADASS, CTA meeting)
    * Before we circulate a Doodle, do you know of any weeks that should
      be avoided in November or December?

## Minutes

* `OBS_ID` as string or integer?
  * Very briefly discussed, but Jürgen not present.
  * There's open questions on the Github issue that should be answered
    before a decision on this is made.
  * Catherine mentioned that this has been discussed elsewhere and that
    she'll post to the Github issue soon.
* Tarek - Update on MAGIC-DL3 activities
  * Several people are getting involved in MAGIC FITS exporters and analysis
* Christoph - Update on HESS activities
  * Almost no progress over the summer.
  * HESS FITS test data release is supposed to be approved at the
    collaboration meeting in the last week of September.
  * We'll try to get the internal checks done before so that this can happen.
* About the next face-to-face meeting:
  * Agreement that the meeting should have somewhat broader scope this time,
    not just IACT DL3.
      * Catherine: DL4 should be a topic
      * Jose-Luis: multi-messenger should be a topic.
      * Tarek: connection to ctapipe should be present
      * Christoph: agree that DL4 should be a topic.
        There's quite a bit of activity on this in the open spec,
        see e.g. [issue 45](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/45)
        for discussions on SED or [this](https://github.com/gammapy/gamma-cat)
        as a recent project started to collect IACT DL4 data.
  * Duration:
    * Christoph prefers full week, so that work gets done.
    * Catherin can't on Mondays, so prefers start on Tuesday.
  * Christoph will circulate Doodle soon with all weeks in November as option
    as well as the two weeks in December before Christmas.
* Next monthly telcon will be October 4, 2016 at 11 am (see [here](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/notes/2016-10-04-IACT_DL3_Telcon.md)).
