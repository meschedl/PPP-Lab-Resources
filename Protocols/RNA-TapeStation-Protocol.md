---
layout: post
title: PPP Lab RNA Tape Station Protocol
category: [ Protocol ]
tags: [ RNA ]
---

## Agilent [Tape Station 4200](https://www.agilent.com/en/promotions/agilent-4200-tapestation-system?gclid=EAIaIQobChMI_tykoMrw4AIVFI7ICh2S3AZFEAAYASAAEgIqEPD_BwE&gclsrc=aw.ds)

### Setup

1. Take RNA Tape and buffer out of fridge 30 minutes beforehand to allow it to equilibrate to room temperature. Tapes should be labeled with how many spots are left, you will always need 1 spot for a ladder. You can also look at the tape and see how many channels have a hole in the top, that means they are used
2. Take ice bucket out of the -20 and put in the RNA ladder (kept in -20) and your RNA sample aliquot tubes (kept in -80)

### Steps

4. Take out appropriate number of Tape Station strip tubes and tube caps (separate boxes per lab)
5. Vortex and spin down buffer, ladder, and samples
6. Add 5µl RNA buffer each to the number of tubes needed + 1. The first tube is always the ladder
7. Add 1µl RNA ladder to the first tube
8. Add 1µl of each sample to each sample tube

Ex:
![Tubes Ex]({{ site.baseurl}}/images/RNA-Tape-Ex.png "Tubes Ex")
9. Put on tube caps and vortex for 1 minute in IKA vortexer
10. Spin down tubes
11. Turn on Thermocyler. Login to JONP (1234). Put tube strip(s) in Thermocyler and balance for the lid. Run program **rna denature** (6 minutes)
12. Spin down tubes
13. Turn on the TS laptop
14. Login to the computer (username Admin, password 3000hanover)
15. Once logged in, turn on the TapeStation (keep the lid closed), wait for it to warm up and make a final click sound and the light will be solid yellow
13. Open TapeStation Controller program and wait for it to connect
14. Open the lid and place the tape in the tape nest. The barcode (looks like a QR code) should be on the bottom facing the back of the machine (where the green light is flashing)
15. Place the strip tubes in the holder with the ladder in the A1 position
16. Take off the tube caps by gently peeling them **from the side**, if you splash up liquid you have to spin them down again
17. Take the tip rack for you lab (on windowsill) and place it in the tip area in the machine, with the empty tips on the left side
18. Close the lid
19. In the software, select the wells in the graphic for your ladder and samples. They will come up on the right side of the screen
20. In the area on the right side, name each well with your sample number/ID
21. Check again that everything is labeled and put in place properly: this machine is a robot and is very delicate, everything **must** be placed properly
22. Press start in the right bottom corner and confirm that the strip caps and tips are taken care of
23. Wait until the program is finished (see progress bar) and the analysis software should come up with your data

### After

24. The TapeStation Analysis software should open by itself within a minute. If it does not (this sometimes happens if the last user does not shut down the computer), close the TapeStation Controller software and it should pop up after a minute or so. If it still does not come up, go into File Explorer/Documents/Agilent/TapeStationData and find the folder for the date. In there should be the analysis file for your data, if you click on it, it will open in the analysis software (this file is not readable on your on personal computer)
25. What comes up first looks like a gel image, click on Electropherogram to be able to look at each samples individually. The trace shows you basically what the gel would look like if you sliced vertically through a gel, and the area under the curve is the brightness of the gel or the amount of the RNA. The x-axis is the size of the RNA and the y-axis is the intensity/how much RNA is at that size
26. Look for the RIN score to determine quality of the RNA, there should be either 2 (most organisms) or 1 (mollusks) clear peaks. Gradations between the two and below the last one indicate degradation of the RNA
27. These are two high quality RNA TapeStations, the first is a coral, and the second is an oyster (only 1 peak)  

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-06-16%20at%201.20.19%20PM.png)  

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-06-15%20at%204.26.07%20PM.png)

28. To save the file, go to File > Create Report. Save the pdf to your folder or your lab folder. You can then email the pdf to yourself
29. When finished, close the Analysis and Controller software
30. **Turn off the TapeStation from the button on the machine**
31. **Shut down the computer**
32. Throw away the used strip tubes and pipette tips from inside the machine
33. Cap and put the tip rack back on the windowsill
34. If the screentape still has spots left on it, put it back in the foil pouch and write down how many spots were used. Write the date opened if not on there
35. Tapes and buffer go back into the fridge, the ladder goes back into the freezer
