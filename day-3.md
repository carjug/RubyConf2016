# Datacenter Fires and Other "Minor" Disasters - Aja Hammerly
* Lessons learned
	* Automate everything
		* people are error prone at 1 in the morning
		* automate rollbacks as well
	* Always have a backup DB
	* Gracefully fallback if any of your external dependencies fail
		* without having to redeploy ideally
	* No silos
		* deployment pairing
		* infrastructure pairing
		* more than 1 person needs to know how to do any given thing
	* Disaster Recovery Plan
	* Cloud
	* If details matter, don't make any assumptions
	* Teams with diverse interests can save the day!
	* Being able to communicate clearly and honestly is hyper-important
	* Group ownership!
		* again: no silos
	* Postmortems
		* Blameless == assume everyone had good intentions