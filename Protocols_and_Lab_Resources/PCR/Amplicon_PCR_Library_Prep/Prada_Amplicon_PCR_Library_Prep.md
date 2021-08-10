# &quot;2nd PCR&quot; Library Preparation Protocol for Amplicon Libraries (ex. COI, MFU, 16S)

Prada Lab  
Written by Maggie Schedl, references from GSC protocol for amplicon sequencing, Steven Doyle Illumina Amplicon Sequencing Protocol, and Illumina 16S metagenomics Sequencing Library Preparation Protocol.  
Last edited 20210810 Maggie Schedl

**Overall Steps**

1. Normalize Volumes in Plate - this is if your samples are different volumes from the 1st PCR
2. 0.8X Bead Cleanup After 1st Amplification
3. Planning, Set-Up, and Running the &quot;2nd PCR&quot; Index Addition Reaction
4. 0.8X Bead Cleanup After 2nd Amplification
5. 1% Agarose Gel to Check for Amplification
6. Biotium Broad Range DNA Quantification Assay (For less than 36 samples, if more than 36, use the [Biotium Plate Reader Assay](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols/Biotium-BroadRange-DNA-PlateReader.md) Protocol)
7. D5000 TapeStation - Necessary for a few samples when all 2nd PCRs are done
8. Determining uM, Diluting and Combining by Plates (For all Amplicons)
MFU ONLY 9. 1X Bead Cleanup after Pooling
MFU ONLY 10. Double Band Size Selection
MFU ONLY 11. 1X Cleanup after Size Selection
MFU ONLY 12. TapeStation After Size Selection to Confirm Only 1 Band
MFU ONLY 13. Quantify MFU Pool after Size Selection
MFU ONLY 14. Determine uM of MFU Pools and Dilute to 15nM
15. Make the Sample Sheet for Sequencing

#### **Before you begin really prepping your samples, email Janet Atoyan jatoyan@uri.edu in Pharmacy at the Sequencing Center to tell them that you are planning on making Amplicon libraries to be sequenced on the MiSeq. Tell them how many samples, that you will prep them, and that you will pool them.**

## 1. Normalize Volumes in Plate - this is if your samples are different volumes from the 1st PCR. Also note: For all samples: you should have your triplicate reactions combined back into one plate or set of tubes

**Materials:**

- Molecular grade water
- Filter tips
- Amplicons from the original PCRs, **if in triplicate these are combined into 1 well in a plate for each sample**

**Steps \*On Post-PCR bench!\***

- Thaw plate and spin down to collect all liquid at the bottom of the wells
- Look from underneath to find the wells with the largest volume
-  Use a p200 set to your estimated volume and aspirate the liquid in that well. If it is not large enough, adjust the volume and try again. If your guess volume was too large, while you have the liquid in the tip, adjust the volume in the pipette down until you see the liquid line in the tip get to the bottom of the tip. Record that volume as the largest volume that you&#39;ll have to bring all the other wells up to (this has been between 30 and 60ul previously).
- Make a map of the plate in your notebook where you can fill in the estimates of volumes in each well. Ex:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.24.01%20AM.png)
- For the first row, or for a few representative wells, use the pipette to get an accurate estimate of the volume in those wells. For the rest of the plate, go off those known volumes to estimate the rest. For example, if you measure 20ul in the first well, you&#39;ll know that any well that looks like that also has 20ul. This way you don&#39;t need to pipette measure every well. Close estimates are good enough
- Create another plate in your notebook that has in each well the largest volume (ex. 50ul) minus the existing volume. This is how much water to add to each well to get them all to be equal. For wells that already have the largest volume, put an X and don&#39;t add any water to them. Ex:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.24.07%20AM.png)
- Use filter tips to add the amount of molecular grade water up to the largest volume in each well

## 2. 0.8X Bead Cleanup After 1st Amplification

**Materials:**

- Freshly made 80% ethanol
- 10mM Tris HCl conical
- MagBio beads
- Magnetic plate
- New set of strip tubes or plate
- Orbital shaker

**Steps \*On Post-PCR bench!\***

- Take beads out of the refrigerator 30+ minutes before starting the clean up to get the beads to room temperature. Swirl the beads to resuspend the settled beads
- Determine volume of PCR product
- Calculate volume of beads that is 0.8X the volume of the PCR product. All the wells should now be the same volume, use that largest volume from the previous step. (ex: 0.8 * 30ul = volume of beads)
- Add 0.8X volume of MagBio beads to the first sample tube, pipetting slowly because the beads are viscous
  - If you are doing a plate, you can use a trough/basin to hold the beads that are then added with a multichannel. Calculate the amount of beads that are needed: volume * number of samples.
- Pipette mix ~10 times slowly to mix beads with the sample, avoid making bubbles and getting droplets on the side of the tubes
- Repeat for each sample, changing tips each time
- Put the sample tubes/plate on the orbital shaker (next to the Qubit) in the rack and use the dial to twist the speed to 200rpm
- Let the samples shake for 15 minutes
- Prepare the 80% ethanol if not made already that day (for a few samples use 4mL of 100% ethanol and 1mL of molecular grade water in a 5mL tube. For a plate of samples use 40mL of 100% ethanol and 10mL of molecular grade water in a 50mL conical)
- After the samples have been on the shaker for 15 minutes, place them on the magnetic rack or plate. To facilitate binding you can place the magnetic rack with the samples on the shaker for a minute or two
- Wait until the liquid inside of the tubes goes clear and the beads have migrated to the sides of the tube where the magnet is
- Prepare a trough/basin for waste liquid
- Remove the clear supernatant by carefully placing the pipette on the bottom side of the tube opposite from the beads. Use a pipette set to 5ul **less** than the amount of liquid that is in the tube (this is to avoid sucking up beads). If you suck up any brown liquid that is the beads and you need to expel the liquid back into the tube and wait for it to go clear again. Expel of the clear liquid in the waste trough
- Repeat for each tube always changing tips
- Add 100ul of fresh 80% ethanol to each tube gently, changing tips between samples
- Remove all the liquid in the tubes carefully without disturbing the beads (100ul) and expel the liquid in the waste trough
- Repeat ethanol wash: add 100ul to each tube gently, changing tips between samples
- Remove all the liquid in the tubes carefully without disturbing the beads (100ul) and expel the liquid in the waste trough
- Remove any remaining liquid by using a p20 set to 20ul on each tube to get anything left over
- Take the tubes off the magnet
- Resuspend the beads in 25ul of 10mM Tris HCl pH 8.5 by pipetting up and down many times to get the beads entirely off the sides of the tubes and mixed in the liquid. If using strip tubes closing the caps and gently flicking can help
- Repeat above step for each tube
- If there are droplets on the side of the tubes tap them gently down or do a **very brief** spin down in the minifuge
- Place the tubes back on the orbital shaker for 5 minutes
- Prepare and label new tubes/plate for the samples
- After the 5 minutes on the shaker, place the tubes back on the magnet plate
- When the liquid is clear, remove 24ul of the clear liquid into the new tubes for each sample. Avoid getting any beads
- Samples can be frozen for later
- Waste trough can be left to dry out overnight and then thrown away in regular trash

## 3. Planning, Set-Up, and Running the &quot;2nd PCR&quot; Index Addition Reaction

**Materials**

- KAPA HiFi HotStart Ready Mix
- 5uM N7-- and S5-- Primers
- Molecular grade water
- Strip tubes and 96 well plate
- Thermocycler
- Filter Tips
- Multichannel pipettes for 1-2ul and 2-20ul

**Steps \*on Post-PCR bench! Use Filter Tips for All Pipetting\***

- Plan so each sample has a unique combination of N7-- and S5-- primers (currently we have enough for more than 384 unique combinations (4 plates))
- This can easily be done in plate format. For example, the N7-- primers can be planned across the top of the plate in sets of 12. All columns in the plate get a unique N7-- primer, but each sample within the column gets the same N7-- primer. For example, think of each primer as a color.
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.24.35%20AM.png)
- Each sample needs a unique pair, so this is combined with the S5-- primers, which you can organize in a similar way by rows. All rows in the plate get a unique S5 primer, but each sample within the row gets the same S5-- primer. This way each sample within the plate has a unique **pair** of primers. Again, think of each primer as a color.
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.24.42%20AM.png)

**PCR**

- Use filter tips for these steps
- Do these steps on an ice bucket or cold plate
- Determine _n_ number: number of samples + small % error = _n_ (for example, for a full plate I do n = 102)
- Create amplification master mix on ice:
- 6.25ul of KAPA HiFi HotStart Ready Mix \* _n_ =
- 2.25ul of molecular grade water \* _n = _
- Set up/label new strip tubes or a plate for your samples
- In each tube should go:
- 2ul of cleaned DNA from 1st amplification
- 8.5ul of the amplification master mix
- 1ul of the planned N7 primer (5uM)
- 1ul of the planned S5 primer (5uM)
- **For a few samples** , I like to make a table, Ex:

| Sample | Master Mix | DNA Volume | Primer 1 (N7) | Primer 2 (S5) |
| --- | --- | --- | --- | --- |
| 1 | 8.5 | 2 | 1 N7-- | 1 S5-- |
| 2 | 8.5 | 2 | 1 N7-- | 1 S5-- |
| 3 | 8.5 | 2 | 1 N7-- | 1 S5- |

- **For a plate of samples** , I first want to add the amplification master mix to each well. To do this with the multichannel, I first create 12 strip tubes with equal amounts of master mix in each. For a plate of 96 samples, the amount of master mix made with an n of 102 is 867ul. Divide this by 12 to get 72.25ul. Aliquot 72.25ul of master mix into each of the 12 strip tubes. Spin down the tubes. Use the multichannel to aliquot 8.5ul of master mix into each well in the reaction plate
- Use the multichannel to add 2ul of DNA from your cleaned 1st PCR plate to the reaction plate, keeping the same orientation
- Set up 12 strip tubes for the N7-- primers, in the order of how they will go in the plate so you can use a multichannel to add down the columns of the plate. Add 10ul of the appropriate primer to its well. Spin down tubes. Use the multichannel to add 1ul of the primers to the plate by going down the columns. Each row gets the same set of N7-- primers but each column gets a different primer
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.24.53%20AM.png)
- Set up 8 strip tubes for the S5-- primers, in the order of how they will go in the plate so you can use a multichannel to add across the rows of the plate. Add 14ul of the appropriate primer to its well. Spin down tubes. Use the multichannel to add 1ul of the primers to the plate by going across the rows. Each column gets the same set of S5-- primers but each row gets a different primer.
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.24.58%20AM.png)
- Vortex and spin down all the samples
- Place in the Thermocycler 2nd PCR program under the CP login. The program is:
  - 98 degrees C 3 minutes
  - **98 degrees C 30 seconds**
  - **55 degrees C 30 seconds**
  - **72 degrees C 30 second**
  - 72 degrees C 5 minutes
  - Hold at 4 degrees C
  - _bold fields are cycled through 8 times_
- Take samples out of the thermocycler when done and place in the freezer if not bead cleaning that day, or you can add water in the next step then freeze
- Add 7.5ul molecular grade water to each well to increase volume for better cleanup and mix well

## 4. 0.8X Bead Cleanup After 2nd Amplification

**Materials:**

- Freshly made 80% ethanol
- 10mM Tris HCl conical
- MagBio beads
- Magnetic plate
- New set of strip tubes or plate
- Orbital shaker

**Steps \*On Post-PCR bench!\***

- Take beads out of the refrigerator 30+ minutes before starting the clean up to get the beads to room temperature. Swirl the beads to resuspend the settled beads
- There should be a total of 20ul in each well, if you did not add the 7.5ul water after the PCR reaction, add it now to each well
- Add 16ul of MagBio beads to each well (0.8X times the volume) and pipette 10 times to mix gently, changing pipette tips each time
- Put the sample tubes/plate on the orbital shaker in the rack and use the dial to twist the speed to 200rpm
- Let the samples shake for 15 minutes
- Prepare the 80% ethanol if not made already that day (for a few samples use 4mL of 100% ethanol and 1mL of molecular grade water in a 5mL tube. For a plate of samples use 40mL of 100% ethanol and 10mL of molecular grade water in a 50mL conical)
- After the samples have been on the shaker for 15 minutes, place them on the magnetic rack. To facilitate binding you can place the magnetic rack with the samples on the shaker for a minute or two
- Wait until the liquid inside of the tubes goes clear and the beads have migrated to the sides of the tube
- Prepare a trough/basin for waste liquid
- Remove the clear supernatant by carefully placing the pipette on the bottom side of the well away from the beads. Use a pipette set to 5ul **less** than the amount of liquid that is in the tube (ex 31ul). If you suck up any brown liquid that is the beads and you need to expel the liquid back into the tube and wait for it to go clear again. Expel of the liquid in the waste trough
- Repeat for each tube always changing tips
- Add 100ul of fresh 80% ethanol to each tube gently changing tips
- Remove all the liquid in the tubes carefully without disturbing the beads (100ul) and expel the liquid in the waste trough
- Repeat ethanol wash: add 100ul to each tube gently changing tips
- Remove all the liquid in the tubes carefully without disturbing the beads (100ul) and expel the liquid in the waste trough
- Remove any remaining liquid by using a p20 set to 20ul on each tube to get anything left over
- Take the tubes off the magnet
- Resuspend the beads in 30ul of 10mM Tris HCl pH 8.5 by pipetting up and down many times to get the beads entirely off the sides of the tubes and mixed in the liquid
- Repeat above step for each tube or well
- If there are droplets on the side of the tubes tap them gently down or do a **very brief** spin down in the minifuge
- Place the tubes back on the orbital shaker for 5 minutes
- Prepare and label new tubes/plate for the samples
- After the 5 minutes on the shaker, place the tubes back on the magnet plate
- When the liquid is clear, remove 27-29ul of the clear liquid into the new tubes for each sample. Avoid getting any beads in the final tube
- Samples can be frozen for later or quantified/gel then. If quantifying immediately place on and ice bucket
- Waste trough can be left to dry out and then thrown away in regular trash

## 5. 1% Agarose Gel to Check for Amplification

**Materials**

- GelGreen
- Loading dye
- Gel box and power system
- Agarose
- 1kb Plus DNA ladder

**Steps \*on Post-PCR bench!\***

- Depending on the gel, melt the appropriate amount of agarose in 1X TAE
- Follow [this protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols/Agrose-Gel-Protocol.md) for making, running, and imaging the gel. Suggestion is to run the gel for 1.5hrs at 80V

Check for bands! If you didn&#39;t get a band the 2nd PCR did not work. This could either be because the 1st PCR didn&#39;t work, or that you did not add things correctly to the 2nd PCR. If you know the 1st PCR was good, you should try doing the 2nd PCR again.

COI samples should now have a band at ~520bp

MFU samples should now have a band at ~390bp

## 6. Biotium Broad Range DNA Quantification Assay (For less than 36 samples, if more than 36, use the [Biotium Plate Reader Assay](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols/Biotium-BroadRange-DNA-PlateReader.md) Protocol)

**Materials**

- Biotium Broad Range Kit (reagent/buffer and 2 standards, in the 4 degree fridge)
- Axygen thin walled 0.2mL tubes
- Qubit 3 fluorometer

**Steps \*On Post-PCR bench! (except when using the Qubit)\***

- Take the kit box out of the 4 degree fridge at least 30 minutes before use so the bottles can get to room temperature
- In a black rack with the small size holes up, place enough Axygen thin walled tubes for each sample being quantified plus 2 more
- Label the 2 extra tubes S1 and S2 for standard 1 and standard 2
- Label the sample tubes appropriately
- Add 190ul of the Biotum buffer reagent to every Axygen tube (sample assay and standard tubes)
- Add 10ul of Standard 1 solution to the S1 tube
- Add 10ul of Standard 2 solution to the S2 tube
- Add 1ul of each sample to their respective tubes
- Vortex and spin down each sample (using minifuge at Qubit station with the tube inserts)
- Select broad range DNA quantification assay on the Qubit
- Select read standards
- Read standard 1 and 2 and record values (S1 is ~350FRU and S2 is ~80,000-90,000 RFU)
- Tell qubit amount of sample in assay tubes (1ul)
- Read each sample tube twice and record values. Use average ng/ul as the DNA amount
- Tubes are safe to throw away in regular trash

## 7. D5000 or D1000 TapeStation - Necessary for a few samples when all 2nd PCR are done, **if you have MFU samples with double band, do this before and after size selection** (see last section)

**Materials**

- D5000 buffer (or D1000)
- D5000 ladder (or D1000)
- D5000 screentape (or D1000)
- Strip tubes and caps specifically for use in the tapestation

**Steps \*On Post-PCR bench!\***

- If you have bands on the gel and qubit values, the 2nd PCR worked! But to check the indexes were added you can run a few samples on the TapeStation to get an exact size estimate
- Choose 3 or 4 samples per plate that have varying concentrations to use
- Get the D5000 buffer, D5000 Ladder, and screen tape out of the fridge at least 30 minutes before use to equilibrate them to room temperature (or D1000 tape and reagents)
- Use the tapestation specific strip tubes and tube caps to set up 1 or 2 strip tubes to run your samples
- A ladder is always run in the first well of the 1st strip tube, so for example if you want to run 8 samples you will have to use 2 strip tubes to account for the ladder that is in the first tube
- Vortex and spin down the ladder and the buffer
- Add 10ul of D5000 buffer to each tube being used plus the one for the ladder (only difference for D1000 is use 3ul D1000 buffer in this step)
- Add 1ul of D5000 ladder to the first tube (or D1000 ladder)
- Add 1ul of DNA library to their respective tube
- Cap tubes
- Use the IKA vortexer (next to the TapeStation), place the tubes in the holder and press start. They will shake for 1 minute
- Spin down the tubes in a minifuge
- Turn on the computer next to the tapestation and login
- Once logged in turn on the tapestation (button on the bottom left front)
- Wait until the light stays solid orange on the tape station
- Double click on the TapeStation Controller icon on the desktop
- Once the program is open and the machine is connected, open the TapeStation by pressing the black button in the middle
- Place the tube strip into the holder with the ladder in the A1 position
- Remove the tube caps gently
- Put the screentape in the tape nest
- Close the lid
- Name the samples in their positions on the software
- Start the program
- After the program, the results will come up
- There should be one peak with an accurate size estimate, and they should be close between all samples with the same primer
- Go to File \&gt; Create Report. Save to the computer and email to yourself
- Exit both programs open
- Remove tubes, used tips, and screentape from the machine
- If the screentape still has wells, if can be used again in the next two weeks, put back into the pouch and write the date and how many wells used. Put in a plastic bag and back into the fridge along with the ladder and buffer
- Close the lid and **turn off the TapeStation**
- **Shut down the computer**

## 8. Determining uM, Diluting and Combining by Plate (For all Amplicons)

**Note: Even if not all the MFU samples have double bands, combine all of the samples in 1 plate together for the size selection. The smaller band will be selected regardless of if there is a larger band or not.**

**Materials**

- New plate
- Molecular grade water
- Foil seals
- PCR strip tubes
- 1.5mL tubes

**Steps \*On Post-PCR bench!\***

- Your samples need to be pooled equal-molarly for sequencing or for size selection. You want to either pool with each sample at 7uM or 15uM concentration. This depends on how much DNA you get out of the 2nd amplification. If some samples amplified poorly, you&#39;ll either have to try doing the 2nd PCR again, or pool to 7uM concentration. It is best to do 15uM though, so if it is not too many samples to re-do, getting them all to 15uM is best
- The amount of DNA in each sample can also be measured as nM (nano Moles) of DNA per ul. This is a better measurement for preparing for sequencing because it&#39;s a weight (ng).
- Create a column in your spreadsheet with Qubit or Plate Reader values for concentration in nM
- measurement that takes into account how much and how long instead of just being the The calculation is: **(concentration in ng/ul / (660 \* average size of fragments)) \* 1000000**
- For COI the average bp is ~520bp
- **If all of your MFU samples have only 1 band, the average is ~380bp. If you have double band samples and will need to size select, use the average size between the two bands, which is ~410bp**
- Example calculation for COI with 13.5 ng/ul:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.25.11%20AM.png)
- Then you&#39;ll want to make a dilution plate where each sample is at 15nM concentration
- To do this create a column for 15nM in 10ul (I chose 10ul because 4ul is used to pool each sample, and with 10 there is a chance to do it twice if you mess up the pooling)
- To calculate how much DNA you need for 10ul at 15nM concentration, calculate how many nM are needed in 10ul (15\*10 or 150nM) and divide that by the concentration of DNA in nM. The equation is: **(15\*10)/concentration in nM**
- For the example sample, thats (15\*10)/40.1 = 3.7ul
- Then create a column for the amount of water to add up to 10ul
- For a plate of samples it is best to copy and paste this information into a plate layout and print it out for easy viewing while pipetting. Make sure to paste as values first before pasting transposed into the plate layout
- **If you have samples that you re-did and are in strip tubes and not the plate, make sure that you make note of where to get the DNA from and to not use samples in the plate you don&#39;t want**
- Add the water first to every well in the plate, it can be helpful to highlight after you&#39;ve added each sample
- Vortex and spin down your 2nd PCR libraries (cleaned) and have them on a ice bucket or plate. Then add the correct amount of DNA to each well in the 15nM dilution plate
- **It will take about 1 hour to do both the water and DNA for 1 plate**
- Example plates:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.25.18%20AM.png)
- Cover and vortex and spin down the plate when you are done
- If you are done for the day the dilution plate can be frozen at -20 degrees
- If pooling immediately, set up 12 temporary strip tubes
- Use a multichannel set to 4ul to pool together each column in the 15nM dilution plate: Pipette 4ul of each sample in the first row into the new strip tubes. Then pipette 4ul from each sample in row B also into the new strip tubes. Do this for all the rows in the plate. This is ok because all the samples should have unique barcode pairs now. After you have done every row, the strip tubes should have 32ul in each
- Cover and freeze the dilution plate
- Combine all liquid from the strip tubes into one 1.5mL tube with a p200 pipette set to ~32ul
- The 1.5m tube should have ~384ul (4\*96) in it
- Vortex and spin down each plate tube and keep on ice
- **STOP HERE IF YOU HAVE DOUBLE BAND MFU SAMPLES AND PROCEED TO STEP 9, these should be frozen at -20 if not moving on immediately**
- For other amplicons: Make 1 new strip tube or 1.5mL tube per primer (ie for all COI or 16S, etc)
- Add 20ul from each primer plate tube into the new tube per primer. **If you have more than one primer here, keep them separate. Only combine pooled plates from the same primer. Freeze tubes at -20 until bringing to the sequencing place**
- **This final tube (or tubes if you have multiple primers) is ready for sequencing. It should have all your samples in it, each library at at same concentration**
- **If you have multiple primers to sequence at once, keep separate at this stage and give to the sequencing place in separate tubes. Determine over email/in person how the primer sets should be added in the sequencer depending on the different sizes**
- **If you don&#39;t have MFU double band samples, skip down to section 15 for preparing the sample sheet and bring the samples to be sequenced**

## **MFU ONLY** 9. 1X Bead Cleanup after Pooling (if you have multiple plates ready, it is best to pool all plates separately, then cleanup each plate pool at one time together)

**Materials**

- Freshly made 80% ethanol
- MagBio beads
- Magnetic rack for 1.5mL tubes
- New set of strip tubes
- Orbital shaker
- TE buffer conical

**Steps \*On Post-PCR bench!\***

- Take beads out of the refrigerator 30+ minutes before starting the clean up to get the beads to room temperature. Swirl the beads to resuspend the settled beads
- This is a 1X bead cleanup, and each 1.5mL tube per plate should have 384ul
- Add 384ul of beads to each plate tube and pipette mix gently at least 15 times
- Put the sample tubes on the orbital shaker in the rack and use the dial to twist the speed to 200rpm
- Let the samples shake for 15 minutes
- Prepare the 80% ethanol if not made already that day (use 40mL of 100% ethanol and 10mL of molecular grade water in a 50mL conical)
- After the samples have been on the shaker for 15 minutes, place them on the magnetic rack. To facilitate binding you can place the magnetic rack with the samples on the shaker for a minute or two
- Wait until the liquid inside of the tubes goes clear and the beads have migrated to the sides of the tube
- Prepare a trough/basin for waste liquid
- Remove the clear supernatant by carefully placing the pipette on the bottom side of the well away from the beads. Use a pipette set to ~10ul **less** than the amount of liquid that is in the tube: use 750ul. If you suck up any brown liquid that is the beads and you need to expel the liquid back into the tube and wait for it to go clear again. Expel of the liquid in the waste trough
- Repeat for each tube always changing tips
- Add 1mL of fresh 80% ethanol to each tube gently changing tips
- Remove all the liquid in the tubes carefully without disturbing the beads (1mL) and expel the liquid in the waste trough
- Repeat ethanol wash: add 1mL to each tube gently changing tips
- Remove all the liquid in the tubes carefully without disturbing the beads (1mL) and expel the liquid in the waste trough
- Remove any remaining liquid by using a p200 set to 50ul on each tube to get anything left over
- Take the tubes off the magnet
- Let them dry for ~5 minutes, you can use a p20 pipette tip to remove any droplets of ethanol that are visible in the tubes
- **For MFU samples that you need to size select, resuspend beads in each tube in 30ul of TE buffer** by pipetting up and down many times to get the beads entirely off the sides of the tubes and mixed in the liquid
- Repeat above step for each tube or well
- Place the tubes back on the orbital shaker for 5 minutes
- Prepare a set of strip tubes for the samples
- After the 5 minutes on the shaker, place the tubes back on the magnet plate
- When the liquid is clear, remove the  clear liquid into the new tubes for each sample. Avoid getting any beads in the final tube
- Samples can be frozen for later, or quantified immediately
- Waste trough can be left to dry out and then thrown away in regular trash

## **MFU ONLY** 10. Double Band Size Selection

**Materials**

- p20 pipette tips
- Blue Pippin 100-600bp Cassette and seals
- Electrophoresis buffer and marker V1
- Strip tubes

[Blue Pippin Manual](https://www.sagescience.com/wp-content/uploads/2016/09/BluePippin-Operations-Manual-460013-Rev-D.pdf) for reference

**Steps \*On Post-PCR bench!\***

- Take out the electrophoresis buffer and marker V1 from the fridge at least 30 minutes before you use them
- Label new strip tubes for each pool to be size selected
- Pipette 30ul of each cleaned, combined plate **in TE buffer** (from previous step) into the new tubes (this is basically all the liquid, but is is very important for it to be exactly 30ul)
- Vortex and spin down marker V1
- Add 10ul of marker V1 to each of the new strip tubes with the combined plates
- Vortex and spin down the new strip tubes
- Take materials up to the Blue Pipping bench
  - Electrophoresis buffer
  - p20 tips
  - p20 pipette
  - 2 cassettes (just in case 1 fails tests)
  - Sealing strips (from cassette box)
  - Quick protocol from the cassette box
  - Strip tubes for collection afterwards
  - 2 foil seals (if you are not using all 5 wells of the cassette)
- Plug in the Blue Pippin and turn it on with the switch in the back, wait for the computer to start up
- Go to protocols and select the eDNA MFU protocol
- In the protocol editor make sure you have the correct number of lanes turned on for collection, if you have only 1 plate you only want 1 lane turned on, etc.
- **Make sure to save the protocol if you change it**
- Open the machine and put in the calibration fixture (this is in the drawer below in a fabric pouch). The calibration fixture goes with the black side down on the machine (see the manual for help)
- Close the lid and press calibrate on the software
- Once done, take out the calibration fixture and put it away in the pouch
- Open up a cassette from the foil packaging and look at it: make sure the agarose is solid throughout the cassette, every wel has liquid in it and that there are no wells that have very low levels of buffer (if there are low liquid levels, it&#39;s ok but you will need to fill them)
- If it&#39;s good, place it in the machine with the input wells on the left side
- Hold it in the machine while you take off the plastic seals
- If any of the wells need more electrophoresis buffer, add it in now (see manual for ideal levels)
- Use the p20 set to 20 to take out the liquid in the first collection well, this should be a little over 40ul. You have to use the p20 tips because they are the only ones small enough to fit in the well.
- Once you have removed the liquid, refill that well with 40ul of fresh electrophoresis buffer
- Go one by one through all the collection wells: removing and adding in fresh buffer. **Even if you are not using all lanes, you have to do this or the cassette could fail the continuity test**
- Check to see if the input wells are full, if they need a little more buffer add it in (see manual for recommended level of buffection well and adding in another 40ul of fresh electrophoresis buffer one at a time. If the cassette fails the continuity test 2 more times, discard that cassette and use a new one.
- When it&#39;s passed the continuity test, you can load the samples
- You can either start at the top or bottom of the cassette, just make sure you are using lanes that are turned on. The lanes are labeled 1-5 starting at the bottom, but it is easier to treat 5 as the first laneer)
- Use a strip seal to seal the collection wells vertically down the cassette
- Close the lid and perform the continuity test on the software
  - If the cassette does not pass, remove the strip seal. Repeat the process of removing liquid from each coll
- Remove 40ul of liquid from the input well, being careful not to stab the gel matrix
- Add the 40ul of your planned first sample and marker mixture to the input well almost like you are loading a large gel. 40ul should add up to the top of the hole
- **Make sure you know/have planned what sample/plate is going into what well in the cassette **
- Repeat one at a time for each input well you are going to use removing the liquid and adding in the sample to the wells
- Do a final visual check to make sure all the chambers have a good amount of buffer and that everything looks right
- Close the lid
- Do a check on the software that the protocol is the correct one and the correct number of lanes are on
- Label lanes with the sample/plate names if you want
- Press start
- Separation and elution will take about 1 hour, set a timer for yourself for 70 min or so
- When you go back up to the GSC, you will see that the program on the computer says Idle when it has finished eluting. If not you&#39;ll have to wait for it to finish.
- Make sure the markers were detected in each lane used, look at the window to see something that looks like this
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.25.30%20AM.png)
- You only care about the lanes you used. If one of the lanes you used does not have the 2 markers like this, the size selection likely did not work and you will have to do it over again for that one sample/plate. You will have to go back to where you combine the samples from the 15nM diluted plate
- If it looks like the run went good, you can open the lid and take off the plastic seal over the collection wells
- Use a new strip tube and remove all the liquid (between 30 and 50ul) from the collection well and put into its own tube in the strip tubes. **Make sure you have the right sample/plate names here**
- Repeat removal of the collection liquid for all used wells
- If there are unused lanes in this cassette, refill each collection well with 40ul electrophoresis buffer
- Write an X on lanes that have been used (sharpie)
- Use foil seals to seal up both sides of the cassette so everything stays covered
- If all of the lanes are used, you can safely dispose of the cassette in the trash
- Samples can be frozen at -20 or cleaned up immediately

## **MFU ONLY** 11. 1X Cleanup after Size Selection (DNA is in the electrophoresis buffer after SS and needs to be removed)

**Materials**

- Freshly made 80% ethanol
- 10mM Tris HCl conical
- MagBio beads
- Magnetic rack for strip tubes (green Zymo one)
- New set of strip tubes
- Orbital shaker

**Steps \*On Post-PCR bench!\***

- Take beads out of the refrigerator 30+ minutes before starting the clean up to get the beads to room temperature. Swirl the beads to resuspend the settled beads
- This is a 1X bead cleanup, and each tube out of the Blue Pippin should have ~40ul
- Add 40ul of beads to each tube and pipette mix gently at least 15 times
- Put the sample tubes on the orbital shaker in the rack and use the dial to twist the speed to 200rpm
- Let the samples shake for 15 minutes
- Prepare the 80% ethanol if not made already that day (use 40mL of 100% ethanol and 10mL of molecular grade water in a 50mL conical)
- After the samples have been on the shaker for 15 minutes, place them on the magnetic rack. To facilitate binding you can place the magnetic rack with the samples on the shaker for a minute or two
- Wait until the liquid inside of the tubes goes clear and the beads have migrated to the sides of the tube
- Prepare a trough/basin for waste liquid
- Remove the clear supernatant by carefully placing the pipette on the bottom side of the well away from the beads. Use a pipette set to ~10ul **less** than the amount of liquid that is in the tube: use 70ul. If you suck up any brown liquid that is the beads and you need to expel the liquid back into the tube and wait for it to go clear again. Expel of the liquid in the waste trough
- Repeat for each tube always changing tips
- Add 150ul of fresh 80% ethanol to each tube gently changing tips
- Remove all the liquid in the tubes carefully without disturbing the beads (150ul) and expel the liquid in the waste trough
- Repeat ethanol wash: add 150ul to each tube gently changing tips
- Remove all the liquid in the tubes carefully without disturbing the beads (150ul) and expel the liquid in the waste trough
- Remove any remaining liquid by using a p20 set to 20ul on each tube to get anything left over
- Take the tubes off the magnet
- Use a p20 pipette tip to remove any droplets of ethanol that are visible on the sides of the tubes
- Resuspend the beads in each tube with 30ul of 10mM Tris HClby pipetting up and down many times to get the beads entirely off the sides of the tubes and mixed in the liquid
- Repeat above step for each tube or well
- Place the tubes back on the orbital shaker for 5 minutes
- Prepare a set of strip tubes for the samples
- After the 5 minutes on the shaker, place the tubes back on the magnet plate
- When the liquid is clear, remove the  clear liquid into the new tubes for each sample. Avoid getting any beads in the final tube
- Samples can be frozen for later, or quantified immediately
- Waste trough can be left to dry out and then thrown away in regular trash

## **MFU ONLY** 12. TapeStation After Size Selection to Confirm Only 1 Band

**Materials**

- D5000 buffer (or D1000)
- D5000 ladder (or D1000)
- D5000 screentape (or D1000)
- Strip tubes and caps specifically for use in the tapestation

**Steps \*On Post-PCR bench!\***

- TapeStation all the samples/tubes you have size selected to make sure they are all the same
- Get the D5000 buffer, D5000 Ladder, and screen tape out of the fridge at least 30 minutes before use to equilibrate them to room temperature (or D1000 tape, buffer and reagent)
- Use the tapestation specific strip tubes and tube caps to set up 1 or 2 strip tubes to run your samples
- A ladder is always run in the first well of the 1st strip tube, so for example if you want to run 8 samples you will have to use 2 strip tubes to account for the ladder that is in the first tube
- Vortex and spin down the ladder and the buffer
- Add 10ul of D5000 buffer to each tube being used plus the one for the ladder (only difference with D1000 is that you add **3ul** D1000 buffer to each tube here)
- Add 1ul of D5000 ladder to the first tube (or 1ul D1000 ladder)
- Add 1ul of DNA library to their respective tube
- Cap tubes
- Use the IKA vortexer (next to the TapeStation), place the tubes in the holder and press start. They will shake for 1 minute
- Spin down the tubes in a minifuge
- Turn on the computer next to the tapestation and login
- Once logged in turn on the tapestation (button on the bottom left front)
- Wait until the light stays solid orange on the tape station
- Double click on the TapeStation Controller icon on the desktop
- Once the program is open and the machine is connected, open the TapeStation by pressing the black button in the middle
- Place the tube strip into the holder with the ladder in the A1 position
- Remove the tube caps gently
- Put the screentape in the tape nest
- Close the lid
- Name the samples in their positions on the software
- Start the program
- After the program, the results will come up
- There should be one peak with an accurate size estimate of around 390bp, and they should all be about the same across all samples
- Go to File \&gt; Create Report. Save to the computer and email to yourself
- Exit both programs open
- Remove tubes, used tips, and screentape from the machine
- If the screentape still has wells, if can be used again in the next two weeks, put back into the pouch and write the date and how many wells used. Put in a plastic bag and back into the fridge along with the ladder and buffer
- Close the lid and **turn off the TapeStation**
- **Shut down the computer**

## MFU ONLY 13. Quantify Pools after Bead Clean and SS

**Materials**

- Biotium Broad Range Kit (reagent/buffer and 2 standards, in the 4 degree fridge)
- Axygen thin walled 0.2mL tubes
- Qubit 3 fluorometer

**Steps \*On Post-PCR bench! (except when using the Qubit)\***

- Take the kit box out of the 4 degree fridge at least 30 minutes before use so the bottles can get to room temperature
- In a black rack with the small size holes up, place enough Axygen thin walled tubes for each sample being quantified plus 2 more
- Label the 2 extra tubes S1 and S2 for standard 1 and standard 2
- Label the sample tubes appropriately
- Add 190ul of the Biotum buffer reagent to every Axygen tube (sample assay and standard tubes)
- Add 10ul of Standard 1 solution to the S1 tube
- Add 10ul of Standard 2 solution to the S2 tube
- Add 1ul of each sample to their respective tubes
- Vortex and spin down each sample (using minifuge at Qubit station with the tube inserts)
- Select broad range DNA quantification
-  assay on the Qubit
- Select read standardsRead standard 1 and 2 and record values (S1 is ~350FRU and S2 is ~80,000-90,000 RFU)
- Tell qubit amount of sample in assay tubes (1ul)
- Read each sample tube twice and record values. Use average ng/ul as the DNA amount
- Tubes are safe to throw away in regular trash

## MFU ONLY 14. Determine uM of Pooled Plates, Dilute to 15nM, and Combine Plates into 1 Tube

Materials

- Strip tubes
- Filter tips
- Molecular grade water

**Steps \*On Post-PCR bench!\***

- This is very similar to the earlier time of calculating nM. Use the size of the fragment (380bp for MFU) and the concentration of the combined plate from the qubit to calculate the nM in the combined tube
- Make a column in an excel/google sheet for nM and use the equation (concentration in ng/ul / (660 \* average size of fragments)) \* 1000000
- Make a column for a diluted pool of sample that is at 15nM concentration and 20ul in volume using the equation: (15\*20)/concentration in nM
- Make a column for how much water to add up to 20ul
- See example table

| Plate | ng/ul | size | Concentration in nM | ul for 15nM in 20ul | H20 to 20ul |
| --- | --- | --- | --- | --- | --- |
| p2001 | 29 | 380 | 86.16 | 3.5 | 16.5 |
| p2003 | 25 | 380 | 74.27 | 4.0 | 16.0 |
| p2005 | 22.4 | 380 | 66.55 | 4.5 | 15.5 |
| p2007 | 24.5 | 380 | 72.79 | 4.1 | 15.9 |

- Make 15nM diluted tubes of for each combined plate tube, adding the water first then the DNA
- Add the whole 20ul from each plate tube to 1 new strip tube. If you did only 1 plate there is nothing to combine
- Label the strip tube appropriately for the project: that one or two tubes should be all the libraries you prepped!

## 15. Make the Sample Sheet for Sequencing

- Download the [Blank Amplicon Sample Sheet](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/PCR/Amplicon_PCR_Library_Prep/Files/Blank_Amplicon_Sample_Sheet.xls)
- In the Sample\_ID column, make IDs for each of your samples starting with CP01 and so on. These have to be in this naming convention for the computer to de-index for you.
- In the Sample\_Name column, that is where the names/IDs of the sample for your project go. These will be put on the file names
- In the i7\_Index\_ID column, put the N7XX number
- In the i5\_Index\_ID column, put the S5XX number
- In the index column, put the bases for the N7XX index. These are in thi[s spreadsheet](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/PCR/Amplicon_PCR_Library_Prep/Files/Indexes%20for%202nd%20PCR%20Prada.xlsx)
- In the index2 column, put the bases for the S5XX index. These are in the same spreadsheet
- The Sample\_Well, Sample\_Plate, Sample\_Project, or Description columns you leave blank
- Example spreadsheet:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-29%20at%2010.25.47%20AM.png)
- Email Janet Atoyen jatoyan@uri.edu with the sample spreadsheet and include the size in bp of the amplicon in the email. Say you are dropping off the tubes in the delivery room on X date
- Put the tube(s) with your libraries in a ziploc bag with &quot;Prada amplicon libraries for the MiSeq&quot; on it and bring to the Pharmacy delivery room (187, across from the fake CVS) freezer
