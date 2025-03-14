-----------------------------------------------------------------------
Notes concerning total cross sections in this directory
Written by: Brian Roeder, TAMU, email: broeder@comp.tamu.edu
Updated: 14 May 2008 for menate_R.cc, v1.4
Updated: 6 February 2025 by Andrew Wantz
-----------------------------------------------------------------------
Total Cross Sections in this directory are from the following sources:

1.n+p elastic (Hydrogen1_el.dat)-> From MCNPx or ENDF.VII sources

2.n+12C elastic (Carbon12_el.dat)-> From ENDF.VII (elastic)+DEMONS (to 1 GeV)

3.n+12C->n'gamma(4.4)+12C (Carbon12_nng4_4.dat)

4.n+12C->a+9Be  (Carbon12_na9Be.dat)  updated 2/6/2025 AW
	The source is unclear for the old cross sections for this channel. I updated this so that up to 21.5 MeV, cross sections
	are from Kuvin 2021, while above 21.5 MeV the cross sections are from Wantz 2025. Since there are no bound excited 
	states of 9Be, we don't have to worry about what state of 9Be we populate- it is always the ground state. 

5.n+12C->n'+3a  (Carbon12_nn3a.dat) -> Contains updated data set with total
cross sections from B. Antolkovic et al., Nucl. Phys. A394 (1983), 87. Added
data points to data file plus added point at 90 MeV reported by Del Guerra.
Points after 100 MeV taken from DEMONS (to 1 GeV).
 
6.n+12C->p+12B  (Carbon12_np12B.dat) updated 2/6/2025
	This was modified to match the Wantz 2025 data from 15.7 to 27.5 MeV, and then 2 data points from Majerle 2020.
	This is now a partial cross section, for producing a proton and populating the ground state of 12B, rather than all proton production. 

7.n+12C->np+11B (Carbon12_nnp11B.dat)

8.n+12C->2n+11C (Carbon12_2n11C.dat)

----9. and 10. added by zwk----

9.n+56Fe elastic (Iron56_el.dat)->From ENDF.VII

10.n+56Fe nonelastic (Iron56_nonel.dat)->From ENDF.VII taken as the diffrence between the total and elastic cross sections.  

----11. and 12. added by zwk----

11.n+27Al elastic (Al27_el.dat)->From ENDF.VII

12.n+27Al nonelastic (Al27_nonel.dat)->From ENDF.VII taken as the diffrence between the total and elastic cross sections.  

----13. to 30. added 2/6/2025 by AW. see summary at end
13. n+12C->p1+12B* (Carbon12_np_1_12B.dat)
	This new channel was added, using cross sections from the Wantz 2025 data set.
	This is the cross section for populating the first excited state of 12B, 2+, Ex = 0.953 MeV.

14. n+12C->p2+12B* (Carbon12_np_2_12B.dat)
	This new channel was added. This is the cross section for populating the second excited state of 12B, 2-, Ex = 1.673 MeV.
	Published cross sections have not yet been implemented. Instead, the n,p0 cross section from the Wantz 2025 data is used,
	until more published cross sections are available. Threshold is adjusted to be reasonable.
 
15. n+12C->p3+12B* (Carbon12_np_3_12B.dat)
	This new channel was added. This is the cross section for populating the third excited state of 12B, 1-, Ex = 2.6208 MeV
	and the fourth excited state of 12B, 0+, Ex = 2.723 MeV. Published cross sections have not yet been implemented. Instead,
	the n,p0 cross section from the Wantz 2025 data is used, until more published cross sections are available. Threshold is
	adjusted to be reasonable. 

16. n+12C->d+11B (Carbon12_nd11B.dat)
	This new channel was added, using cross sections from the Wantz 2025 data set. This is the cross section for populating the
	ground state of 11B, 3/2-, Ex = 0 MeV.

17. n+12C->d1+11B* (Carbon12_nd_1_11B.dat)
	This new channel was added. This is the cross section for populating the first excited state of 11B, 1/2-, Ex = 2.1247 MeV.
	Published cross sections have not yet been implemented. Instead, the n,d0 cross section  from the Wantz 2025 data is used,
	until more published cross sections are available. Threshold is adjusted to be reasonable. 

18. n+12C->d2+11B* (Carbon12_nd_2_11B.dat)
	This new channel was added. This is the cross section for populating the second excited state of 11B, 5/2-, Ex = 4.44498 MeV.
	Published cross sections have not yet been implemented. Instead, the n,d0 cross section  from the Wantz 2025 data is used,
	until more published cross sections are available. Threshold is adjusted to be reasonable. 

19. n+12C->d3+11B* (Carbon12_nd_3_11B.dat)
	This new channel was added. This is the cross section for populating the third excited state of 11B, 3/2-, Ex = 5.020 MeV.
	Published cross sections have not yet been implemented. Instead, the n,d0 cross section  from the Wantz 2025 data is used,
	until more published cross sections are available. Threshold is adjusted to be reasonable. 

20. n+12C->d4+11B* (Carbon12_nd_4_11B.dat)
	This new channel was added. This is the cross section for populating the fourth excited state of 11B, 7/2-, Ex = 6.741 MeV
	and the fifth excited state of 11B, 1/2+, Ex = 6.791 MeV. Published cross sections have not yet been implemented. Instead,
	the n,d0 cross section  from the Wantz 2025 data is used, until more published cross sections are available. Threshold is 
	adjusted to be reasonable. 

21. n+12C->d5+11B* (Carbon12_nd_5_11B.dat)
	This new channel was added. This is the cross section for populating the sixth excited state of 11B, 5/2+, Ex = 7.285 MeV.
	Published cross sections have not yet been implemented. Instead, the n,d0 cross section from the Wantz 2025 data is used,
	until more published cross sections are available. Threshold is adjusted to be reasonable. 

22. n+12C->d6+11B* (Carbon12_nd_6_11B.dat)
	This new channel was added. This is the cross section for populating the seventh excited state of 11B, 3/2+, Ex = 7.977 MeV.
	Published cross sections have not yet been implemented. Instead, the n,d0 cross section from the Wantz 2025 data is used,
	until more published cross sections are available. Threshold is adjusted to be reasonable. 

23. n+12C->d7+11B* (Carbon12_nd_7_11B.dat)
	This new channel was added. This is the cross section for populating the eighth excited state of 11B, (3/2-), Ex = 8.560 MeV.
	Published cross sections have not yet been implemented. Instead, the n,d0 cross section from the Wantz 2025 data is used,
	until more published cross sections are available. Threshold is adjusted to be reasonable. 

24. n+12C->t+10B (Carbon12_nt10B.dat)
	This new channel was added. Since published cross sections of this channel are not yet available, this uses the average of 
	the n,d0 and n,p1 cross sections from the Wantz 2025 data set. This is the cross section for populating the ground state of
	10B, 3+, Ex = 0 MeV. Threshold is adjusted to be reasonable. 

25. n+12C->t1+10B (Carbon12_nt_1_10B.dat)
	This new channel was added. Since published cross sections of this channel are not yet available, this uses the average of 
	the n,d0 and n,p1 cross sections from the Wantz 2025 data set. This is the cross section for populating the first excited 
	state of 10B, 1+, Ex = 0.718 MeV. Threshold is adjusted to be reasonable. 

26. n+12C->t2+10B (Carbon12_nt_2_10B.dat)
	This new channel was added. Since published cross sections of this channel are not yet available, this uses the average of 
	the n,d0 and n,p1 cross sections from the Wantz 2025 data set. This is the cross section for populating the second excited 
	state of 10B, 0+, Ex = 1.740 MeV. Threshold is adjusted to be reasonable. 

27. n+12C->t3+10B (Carbon12_nt_3_10B.dat)
	This new channel was added. Since published cross sections of this channel are not yet available, this uses the average of 
	the n,d0 and n,p1 cross sections from the Wantz 2025 data set. This is the cross section for populating the third excited 
	state of 10B, 1+, Ex = 2.154 MeV. Threshold is adjusted to be reasonable. 

28. n+12C->t4+10B (Carbon12_nt_4_10B.dat)
	This new channel was added. Since published cross sections of this channel are not yet available, this uses the average of 
	the n,d0 and n,p1 cross sections from the Wantz 2025 data set. This is the cross section for populating the fourth excited 
	state of 10B, 2+, Ex = 3.587 MeV. Threshold is adjusted to be reasonable. 

29. n+12C->t5+10B (Carbon12_nt_5_10B.dat)
	This new channel was added. Since published cross sections of this channel are not yet available, this uses the average of 
	the n,d0 and n,p1 cross sections from the Wantz 2025 data set. This is the cross section for populating the fifth excited 
	state of 10B, 3+, Ex = 4.774 MeV. Threshold is adjusted to be reasonable. 

30. n+12C->t6+10B (Carbon12_nt_6_10B.dat)
	This new channel was added. Since published cross sections of this channel are not yet available, this uses the average of 
	the n,d0 and n,p1 cross sections from the Wantz 2025 data set. This is the cross section for populating the sixth, seventh,
	and eighth excited states of 10B, (2-, Ex = 5.110 MeV; 2+, Ex = 5.163; 1+, Ex = 5.182). Threshold is adjusted to be reasonable. 

In summary, the 12C(n,alpha)9Be cross section was updated with new data, the 12C(n,p)12B cross section was modified to be the partial
cross section for populating the 12B ground state. New reaction channels were created, for excited states of 10B, 11B, and 12B, as well 
as the ground states of 10B and 11B. 

Of the new/updated channels, only the 12C(n,alpha)9Be, 12C(n,p0)12B, 12C(n,p1)12B, and 12C(n,d0)11B have real cross section data. All 
the other channels have placeholder cross sections so that the machinery works, but do not reflect reality yet. Some of these may be 
updated as further analysis is performed. The cross sections for all the new channels with placeholder cross sections are too large-
if trying to match with data, they should be reduced. 

More channels may need to be added depending on what is observed in experiment, and some of the above channels may be modified or 
removed as further analysis is performed. 
