### How makes ready an application to be Cloud-base or move it to Cloud
Extracting initial state of system for checking 12 main steps which one is not included:
1) **Code Base:** Keep applications on code repository like Git not storage
2) **Dependency**: Make a bundle of dependencies and and libraries
3) **Configuration:** Should be in variable not in codes -> Helps to change them without changing main codes, rebuild and etc.
4) **Backend Services:** ex. Has Connection string to set them and has retry to connect methods
5) **CD/CD:** Full automations for build, release and run by a container not a person
6) **Stateless:** Not being stateful (Dependence on previous state or process) -> Your tokens, sessions and etc on a q or cache
7) **Port-binding:** set application ports like Nginx
8) **Concurrency:** Run multi instances of a process simultaneously -> helps to horizontal scale:
	* *Horizontal scaling (Scale-out):* up multi processes ->. Good for stateless apps
	* *Vertical scaling (Scale-up):* up Ram / Cpu -> Good for stateful
9) **How Kill a process by Kill-Signals:** Die immediately is not good. -> First response to whatever you have it in process then die -> Helps to No down-time
10) Have multiple environment for to help keeping main app safe:
	 * Test
	 * Development
	 * Pre-product or Pre-live
11) **Logs and Metrics:** Helps to realize system problems and failures
12) **Don't Change system by Live-Coding:** except when it is so incident and simple