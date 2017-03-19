
To implement DVFS, we changed the following files:
	power.c power.h sim-outorder.c

and added a new file:
	dvfs_header.h
	
A funtion called dvfs_controller() is added in power.c, in which we implemnt a new dvfs control strategy(not the simple one with 0.2 step) as we discussed in our report.

Replace that three files and add the new file to sim-wattch, then re-compile it:
	make sim-outorder	 


Commands to run benchmark anagram:
	../sim-outorder -dvfs:interval 500 -dvfs:target_power 71.7882 anagram.alpha < anagram.in 2> anagram_result.txt


Commands to run benchmark go:
	../sim-wattch/sim-outorder -dvfs:interval 10000000 -dvfs:target_power 71.7882 go.alpha 50 9 2stone9.in 2> go_result.txt