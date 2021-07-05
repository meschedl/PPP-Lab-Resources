
# PPP LAB Biotium Broad Range AccueBlue dsDNA Quantification Assay Protocol

[AccuBlue® Broad Range dsDNA Quantitation Kit with DNA Standards](https://biotium.com/product/accublue-broad-range-dsdna-quantitation-kit-with-9-dna-standards/)

This is for using the Synergy HTX Multi Mode Plate Reader to read a 96 well plate for DNA quantification. Notice you will not be able to read a whole plate because of the standard curve, usually you will be able to run 84 samples.

1. Take the buffer and standards out of the fridge at LEAST 30 min before use, it needs to get up to room temp, keep it in a drawer because the components are light sensitive, or keep inside the cardboard box. **It can be useful to aliquot out the amount of buffer you need in a 50mL conical cold, then keep in the drawer and the smaller volume will warm up quicker. Additionally, the dye (clear) can become solidified in the fridge. Make sure it has warmed up and has been mixed up before use, you can shake it to hear if there is a piece of solidified dye bouncing around. Vortex and hold in gloved hand if it's solid.**
2. **Determine what standards are needed**, you may not need all of them. Standards that come with the kit:  
  - 0 ng/ul  
  - 2ng/ul
  - 6.25ng/ul
  - 12.5ng/ul
  - 25ng/ul
  - 50ng/ul  
  - 100ng/ul
  - 150ng/ul
  - 200ng/ul  
  For example, if you are not expecting samples to be over 100ng/ul you can omit those from the standards you use. You have to use the 0ng/ul, and the more standards you use the more accurate your curve. If you have room you can also double or triple up on standards. For example, you could use half the standards and do 2 of each. Plan this depending on your expected amount of DNA. Make sure to include your planned standards in calculations for the working solution and plate layout planning
3. **Prepare working solution** (goes in each well of the plate):  
  - A full plate (96 wells) is: 20mL buffer, 200ul dye, 200ul enhancer in a 50mL conical  
  Vortex and spin down all reagents and add into the conical  
  Then vortex and spin down the conical, use the large centrifuge to spin the conical  
  Cover the conical with foil or keep in a drawer before use because the dye and enhancer are light sensitive
  - If you have a different number of samples you can calculate the amount of working reagent to make:  
  200ul buffer per sample + 2ul dye per sample + 2ul enhancer per sample plus error (also include each standard you’re going to do here as a sample)
5. **Plan** how your samples and standards are going to be laid out in the 96 well plate **before** you pipette anything. Note that if you have a full 96 well plate, you won't be able to read all you samples because of the standards needed. I usually use a whole row for standards and then use the Qubit to quantify the remaining 12 samples
4. Use a **black 96-well microplate.** For each well that is going to be used (the standards plus your samples), pipette 200ul of the working solution. _It is best to use a trough/basin and a p200 multichannel_
6. Adde 10ul of the appropriate standard to its corresponding planned standard well(s)
7. Adde **2ul** of sample to the appropriate well (this is different then the Accublue protocol, they suggest using 10ul, but that is often too large a portion of your sample. However, because the difference in the amount added per sample versus the standards, it makes the standard curve calculation a little strange)
8. Cover the plate with foil (loose foil, not a sticky lid) to block light and incubate on the orbital shaker for 10 minutes at 300rpm (this also helps mix the samples with the solution)
9. Turn on the computer and log in. Then turn on the plate reader and **wait** for it to start up: you know when it is ready because the little hatch has opened for the second time and stays open, this will take 3ish minutes.
10. Opened the Gen5 software and chose the **BiotiumBroadRangeDNA.prt** protocol. **Make sure you are on the "Read Now" section.** If you mess up, close the program and open again.
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/7.png)
11. Click on the plate icon (on the menu bar, blue with an orange open circle on the right) to set the plate layout, this is where you tell the computer which wells are the standards and which wells are the samples. It's not technically necessary, but it helps for copy and paste later.
12. Set the positions of the standards where they are in the plate:  
  Select the standard from the left side dropdown list and click on the well in the virtual plate where it will be (the curser is a pipette!)  
  **It will automatically switch to the next standard in the list after 1 click, so if you are replicating them or skipping one you have to select it specifically**  
  If you don’t use all the options on the program for standards that is fine, click ok if the program gives you an “error”   
  **Note that the standards are set as the number of ng added to each well, aka the 6.25ng/ul standard is set as 62.5 because that is how many ng were added in the 10ul.**
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/2.png)
13. Set your samples where they are in your plate, some times you can drag horizontally to make it go quicker. It is usually saved as the last layout someone used. **Make sure you know what SP1,SP2, SP etc are in how they pertain to your actual sample #s**
13. Any well that has nothing in it do not click anything leave it white/Empty and click ok
14. You have to wait for the bulb to warm up before running it, that takes about 3 minutes
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/8.png)
**If you wait until the machine is ready and then press ok, it will immediately start and bring the tray into the machine. If you press ok before it's ready, you'd have to press the green play button on the upper menu bar to read the plate. However you do it, before you press to read the plate, put the plate on the tray with the A row closest to the machine and remove the foil.**
15. It takes less than a minute to read, and once done click on statistics tab to look at the readings
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/6.png)
16. To copy things to Excel, you first have to open excel on the computer (for some reason if you don’t have the Excel welcome window already open, the Gen5 software won’t let you copy to Excel)
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/4.png)
17. Then go back to the Gen5 software and be on the "Statistics" tab. Next to the dropdown menu, click the little Excel button. The excel open on the computer will flash orange, and it will have copied that table to the excel sheet.
18. Save the Excel sheet to the computer in a folder with your name (do not save to One Drive, that would be Maggie's drive!), and then you can email it to yourself
19. To analyze the data, first you need to make a standard curve with the standards in the first row. However, in the Excel sheet, these are at the bottom and labeled as the standards with their ng/well. Scroll to the bottom of the table and the standards are there. You can copy and paste the "ng/well" and "360/460:360/40,460/40" columns to a new sheet or a Google Sheet to make a graph. 360/460:360/40,460/40 is the absorbance
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-02-17%20at%205.00.51%20PM.png)
20. Then you can make a scatter chart in either Excel or Google Sheets that uses the first column (ng/well) and the second column (absorbance) to make a standard curve. This is basically a line and the slope is used as a calculation for your other samples
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-02-01%20at%203.59.23%20PM.png)
For example, in Google Sheets you can create a chart and customize it by going to series and adding a Trendline. To get the equation, use it as a label. Make sure the line is not forced through 0,0; as you can see 0ng/ul does not have a 0 absorbance
21. Then you can use the equation for the rest of your samples. In the image above, absorbance = 0.342x + 5.68. x is ng per well. You have to switch it around to solve for x, and you have the absorbance values already. That would be (absorbance - 5.68)/0.342 = ng per well. Use a new column in your Google or Excel sheet and put in the equation, referencing the absorbance from the plate reader, to get ng per well for each sample. Then make another column where that value is divided by 2 to get ng/ul, remember you added 2ul of sample to each well
