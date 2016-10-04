# 2016-10-04 - Monthly IACT DL3 telcon

* Tuesday, October 4, 2016 at 11 am CEST
* Duration: 40 min
* Participants: Catherine Boisson, Tarek Hassan, Christoph Deil

## Connection details

If you have questions how to connect, please email  [Catherine Boisson](http://www.iau.org/administration/membership/individual/7665/)

Connection from a single terminal:

[http://desktop.visio.renater.fr/scopia?ID=721024***1925&autojoin](http://desktop.visio.renater.fr/scopia?ID=721024***1925&autojoin)

Otherwise:

* Telephone or RNIS 	+33 (0)4 26 68 73 07
* GDS 	+33 (0)4 26 68 73 07 721024
* SIP 	sip:721024@195.98.238.109
* H.323 	h323:721024@mgmt.visio.renater.fr
* Conference number 	721024 (end by #)
* Password 	1925 (end by #)

Conference Title 2016 Sept. 4 IACT DL3 Begin 04/09/2016 11:00 (GMT +2 Europe/Paris) Duration 02:00

## Minutes

* We briefly discussed the suggestion to [Rephrase "data level 3" to "low-level science data products"?](https://github.com/open-gamma-ray-astro/open-gamma-ray-astro-gamma2016/issues/6) for the "Open high-level data formats and software for gamma-ray astronomy" Gamma 2016 proceeding draft [PDF](https://github.com/open-gamma-ray-astro/open-gamma-ray-astro-gamma2016/blob/master/proceeding/open-gamma-ray-astro-gamma2016.pdf). Christoph will implement the suggestion from Catherine and Tarek given there.
* Change safe energy header keywords. See [issue 66](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/66).
Agreement that it's probably a good change and that we should make it soon. Catherine and Tarek will have a closer look and then leave a comment there.
* Change energy dispersion storage format. See [issue 67 ](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/67). Issue was filed after the telcon, but we already discussed this during the telcon. It wasn't clear to us if the proposed change really is an advantage or if we couldn't just extend the y-axis range with the current format. Tarek said he might have time to investigate this for CTA in the future, otherwise no short-term or concrete action items.
* Updates to SED Fomat. See [PR 65](https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/pull/65). Briefly discussed, nothing specific to note here. Please review and comment. If there's not much feedback we'll merge soon.
* For Gammapy, we wrote an IPython notebook (work in progress) about [IACT DL3 data with Gammapy](http://nbviewer.jupyter.org/github/gammapy/gammapy-extra/blob/master/notebooks/data_iact.ipynb). We'll do some more cleanup and add docs and then release Gammapy 0.5 in October.
* The next telcon will be November 8th, 2016 at 11 am. (see connection details and agenda [here](https://github.com/open-gamma-ray-astro/2016-04_IACT_DL3_Meeting/blob/master/notes/2016-11-09-IACT_DL3_Telcon.md)).
* We're starting to plan the "Open gamma-ray data and software - Fall 2016 meeting" face-to-face meeting. Christoph will start an email thread on that later this week.
