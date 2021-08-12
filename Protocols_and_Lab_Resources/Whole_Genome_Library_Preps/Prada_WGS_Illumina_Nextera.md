# Low Coverage Whole Genome Sequencing Library Prep Protocol

Protocol is a mix of 1/7th reactions from Nextera XT and recommendations from [Kishony et. al](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0128036)

Prada Lab
Last Update 20210812 Maggie Schedl

**Materials**

- Nextera XT DNA Library Preparation Kit (24 samples) [LINK](https://www.illumina.com/products/by-type/sequencing-kits/library-prep-kits/nextera-xt-dna.html) catalog number: FC-131-1024
- IDT® for Illumina Nextera DNA Unique Dual Indexes Set A (96 Indexes, 96 Samples): [LINK](https://www.illumina.com/products/by-type/sequencing-kits/library-prep-kits/nextera-xt-dna.html) catalog number: 20027213
- DNA-Away [LINK](https://www.fishersci.com/shop/products/dna-away-surface-decontaminant/2123628#?keyword=DNA-away) catalog number: 21-236-28
- MagBio beads
- Filter pipette tips
  - p1000: [LINK](https://www.shoprainin.com/Products/Pipettes-and-Tips/Pipette-Tips/LTS-Pipette-Tips/GreenPak/Pipette-Tips-GP-LTS-1000%C2%B5L-F-768A-8/p/30389272) catalog number: 30389272
  - p200: [LINK](https://www.shoprainin.com/Products/Pipettes-and-Tips/Pipette-Tips/LTS-Pipette-Tips/GreenPak/Pipette-Tips-GP-LTS-200%C2%B5L-F-960A-10/p/30389276) catalog number: 30389276
  - p20: [LINK](https://www.shoprainin.com/Products/Pipettes-and-Tips/Pipette-Tips/LTS-Pipette-Tips/GreenPak/Pipette-Tips-GP-LTS-20%C2%B5L-F-960A-10/p/30389274) catalog number: 30389274
- 96 well plates [LINK](https://geneseesci.com/shop-online/product-details/24-301/olympus-96-well-pcr-plate-semi-skirted)
- Foil seals [LINK](https://www.thermofisher.com/order/catalog/product/AB0626?SID=srch-hj-AB-0626#/AB0626?SID=srch-hj-AB-0626)
- Thermocycler
- Biotium broad range DNA assay kits

#### PRE-STEP: Any time you get in a new kit you should aliquot the reagents into smaller tubes. The suggested volume to aliquot are amounts for 8 preps each. This way you have enough for a small test prep in 1 tube, or you can easily use multiple tubes for more or a plate. This kit has had issues with reagents not working after multiple freeze-thaws, so it is essential to aliquot out when you get a new box if you're not planning on using all of it at once.
- Total volumes in tubes from Illumina
  - TD: 1.24mL
  - NT: 0.66mL
  - ATM: 0.236mL
  - NPM: 0.41mL
- The most limiting reagent is the NPM. The maximum amount of aliquots for 8 samples each you can get out the NPM is 21. 21 x 8 = 168. 168 preps is the maximum you can get out of the 24 kit with 1/7th reaction volumes
- NT is kept at room temp and does not need to be aliquoted
- Make 21 small strip tubes for each: TD, ATM, and NPM
- Thaw TD, ATM, and NPM on ice
- Invert to mix and spin down reagents
- Add 12.78ul of TD to the 21 TD aliquot tubes on ice
- Add 6.65ul ATM to the 21 ATM aliquot tubes on ice
- Add 19.26ul NPM to the 21 NPM aliquot tubes on ice
- Spin down all aliquot tubes and place in a PCR rack with a cover in the -20. Label with the kit name, Prada, and the kit received date



**Steps**

1. Plan index and plate layouts
2. DNA standardization to 0.5ng/ul
3. Tagmentation
4. Amplification and index addition
5. 1X bead cleanup
6. QC: concentration and size check
7. Dilution to 10uM and pooling

**Pre-Steps:**

- Use filter tips for all steps other than qubit and cleanups
- Clean pipettes, work bench, tube racks, and tip boxes with DNA-away before use each day
- Work on the Prada Lab Molecular bench

## PROTOCOL

### 1. Plan Indexing and Plate Layouts

- We have 2 index plates, IDT® for Illumina Nextera DNA Unique Dual Indexes Set A and Set B. These are plates with 96 unique indexes in each. Each well has 1 index set, each well can only be used once (within a project/sequenced once)
- They are numbered UDP0001 to UDP0192
- Because they are already set up in plates, it&#39;s easiest to plan your libraries in plates and use the same layout to allocate indexes to them, ie the sample in row A column 1 should get the index that is in row A column 1 in the index plate
- Index numbers go down columns
- Randomize samples in the plate layout so there are no possible batch effects

### 2. DNA Standardization to 0.5ng/ul (Kisony et. al recommendation)

**Materials**

- Filter tips
- 96 well plate or strip tubes, depending on how many samples
- TE buffer
- Foil plate seals
- Extracted DNA

**Notes**

- Use filter tips for all pipetting
- Work at the Pre-PCR Prada Lab bench

**Steps**

- Quantify DNA from extractions if not done so, use Qubit or plate reader
- Decide the ideal volume for diluting the DNA.
  - This depends on your starting concentration, 0.5ng/ul is very dilute. For example:
  - Samples with greater than 20ng/ul it might be easiest to dilute in 100 or 200ul. It is best to avoid pipetting below 1ul.
  - Samples with less than 20ng/ul concentration could be in 50ul or 20ul
- Calculate the volume of DNA for the dilution for each sample
  - Depending on the volume this could be 5ng, 50ng, 100ng etc
  - If you are diluting in 100ul, you need 50ng to make the concentration 0.5ng/ul
  - If you are diluting in 10ul, you need 5ng to make the concentration 0.5ng/ul and so on
- Calculate the volume of DNA buffer (usually TE buffer or 10mM Tris HCl, depending on the extraction conditions) needed to add to each sample to equal up to the dilution volume
- (For a 96 well plate) You can easily set up a plate map for the dilutions that you can use for pipetting, as well as make a map of the layout of the samples:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-09%20at%206.33.45%20PM.png)
- Set up a dilution plate or strip tubes. If doing a 96 well plate, use the layout you&#39;ve generated above
- Add first the calculated volumes of DNA buffer to each well (usually this is the larger volume)
- Then add the calculated volumes of DNA to each well
- Cover the plate with a foil seal
- Vortex the plate and centrifuge it down in the large centrifuge
- The plate can be kept on ice for use immediately or put in the -20 freezer for use another day

### 3. Tagmentation

**Materials**

- TD (Tagmentation buffer - stored at -20)
- ATM (Amplicon tagment mix - stored at -20)
- NT (Neutralize Tagment Buffer - stored at room temp in the Illumina box on the Prada bench)
- Fresh 96 well plate or strip tubes depending on how many samples you are doing
- Filter tips
- Foil plate seals
- DNA diluted to 0.5ng/ul

**Notes**

- &quot;This step uses the Nextera transposome to tagment gDNA, which is a process that fragments and tags DNA with adapter sequences.&quot;
- 1/7th reaction volumes of Nextera kit
- Use filter tips for all pipetting
- Work at the Pre-PCR Prada Lab bench

**Steps**

- Thaw TD on ice, once thawed, invert 3 times then centrifuge to collect
- Thaw ATM on ice, once thawed, invert 3 times then centrifuge to collect
- Check for precipitates in the NT, if there are any, vortex the tube until everything is in solution, then centrifuge to collect
- Add 1.42ul of TD to each well in a 96 well plate (or however many tubes or wells you are going to use).
  - If doing a 96 well plate, you can use the multichannel and strip tubes.
  - Make 8 strip tubes with 18.5ul of TD in each.
  - Then pipette 1.42ul by column into each well in the plate
- Add 0.7ul of diluted 0.5ng/ul DNA for each sample into their planned well. Again if you already made a dilution plate, this can be done with a multichannel
- Pipette mix after adding the DNA (0.7ul is sufficient because volume is ~2.1ul)
- Add 0.7ul of ATM to each well
  - If doing a 96 well plate, you can use the multichannel and strip tubes
  - Make 8 strip tubes with 9.1ul of ATM in each
  - Then pipette 0.7ul by column into each well in the plate
- Pipette mix after adding the ATM at least 10 times
- Centrifuge at 3000rcf at 20°C for 3 minute (using the large centrifuge). If there are still bubbles present (the low volume causes problems) flick the bottom of the plate to disrupt the bubbles in the wells and centrifuge again for 3 minutes
- Place in the thermocycler in the TAG1 program
  - Lid is set at 100 degrees C
  - 55 degrees C for 10 minutes
  - Hold at 10 degrees C
- Immediately take the plate or tubes out of the thermocycler after 10 minutes, the enzyme is still active
- Add 0.7ul of NT to each well in the plate/tubes
  - If doing a 96 well plate, you can use the multichannel and strip tubes
  - Make 8 strip tubes with 9.1ul of ATM in each
  - Then pipette 0.7ul by column into each well in the plate
- Pipette mix after adding the NT at least 10 times
- Seal plate/tubes
- Centrifuge at 3000rcf at 20°C for 3 minute (using the large centrifuge). If there are still bubbles present (the low volume causes problems) flick the bottom of the plate to disrupt the bubbles in the wells and centrifuge again for 3 minutes
- Incubate the plate at room temperature for 5 minutes (inactivates the tagmentation enzyme)
- After the 5 minutes, place the plate on ice
- Final volume is 3.52ul

### 4. Amplify DNA and Add Indexes

**Materials**

- Filter tips
- Index plates (A or B, depending on what samples you are doing, stored at -20)
- NPM (Nextera PCR Master Mix, stored at -20)
- Thermocycler
- Tagmented samples on ice

**Notes**

- 1/7th reaction volumes of Nextera kit
- Use filter tips for all pipetting
- Work at the Pre-PCR Prada Lab bench

**Steps**

- Thaw NPM on ice, once thawed, vortex and spin down
- Thaw Index plate you are going to use on ice
- Add 1.42ul of each planned index to their corresponding well in the tagmented DNA plate. Use a multichannel. These should be planned so that the indexes are in the same well as the sample they are going into
- Add 2.14ul NPM to each well
  - If doing a 96 well plate, you can use the multichannel and strip tubes
  - Add 27.8ul NPM to 8 strip tubes
  - Use the multichannel to add 2.14ul NPM across rows to each well
  - Pipette mix 10 times in each well after adding the NPM
- Centrifuge at 3000rcf at 20°C for 3 minute (using the large centrifuge). If there are still bubbles present (the low volume causes problems) flick the bottom of the plate to disrupt the bubbles in the wells and centrifuge again for 3 minutes
- Seal plate/tubes
- Place in the thermocycler CP login, WGS folder, PCR 15 program. Runs for ~45 minutes
- Afterwards, place on ice or in the fridge if doing a cleanup that day. If waiting to do a cleanup, put in the -20 freezer

### 5. 1X Cleanup after Index Amplification

**Materials**

- MagBio Beads
- Molecular grade water
- 80% ethanol
- 10mM Tris HCl
- Orbital shaker
- New 96 well plate and seal
- Index amplified sample plate

**Notes**

- Work at the Pre-PCR Prada Lab bench
- We increase the working volume with water before adding beads to make it easier to multichannel and less likely that the beads will over-dry and cause DNA loss
- It is important that the MagBio beads are at room temperature when you use them. Take them out of the 4 degree 30-60 minutes before use
- Make 80% ethanol fresh each day you use it. Use 40mL of 100% ethanol and fill the rest of the 50mL conical with molecular grade water up to 50mL

**Steps**

- Add 13ul of molecular grade water to each sample/well
  - If doing a 96 well plate, you can use the multichannel and strip tubes
  - Add 169ul molecular grade water to 8 strip tubes
  - Use the multichannel to add 13ul water across rows to each well
- Make sure MagBio beads are at room temperature and completely mixed. Swirl the bottle until all the beads at the bottom have come up into solution
- Add 20ul of beads to each well
  - If doing a 96 well plate, you can use the multichannel and strip tubes
  - Make 12 strip tubes with 180ul beads in each
  - Multichannel 20ul beads down columns
- Pipette mix 10-20 times in each well. Pipette slowly and try to avoid bubbles. The beads should be spread homogeneously through the liquid
- Place the plate on the orbital shaker for 15 minutes (use a silicon mat to cover the plate from dust if desired)
- After 15 minutes, place plate on magnet stand and put back on the shaker for 2 minutes (or until the liquid goes clear)
- Take the plate and stand back to the bench
- Multichannel out the liquid into a waste basin. Remove 33ul from each well, pipette down the side of the well that is opposite from the bead pellet. Pipette slowly as to not disturb the beads
- Add 75ul 80% ethanol to each well gently to not disturb the beads (a basin can be made for ethanol)
- Remove 75ul of liquid from each well and into a waste basin. Pipette down the side of the well that is opposite from the bead pellet. Pipette slowly as to not disturb the beads
- Add 75ul 80% ethanol to each well gently to not disturb the beads (second wash)
- Remove 75ul of liquid from each well and into a waste basin. Pipette down the side of the well that is opposite from the bead pellet. Pipette slowly as to not disturb the beads
- Remove any remaining ethanol from each well by using a p20 pipette set to 20ul
- Remove the plate from the magnet rack
- Resuspend the beads by pipetting/dripping 17ul of 10mM Tris HCl directly onto the bead pellet and pipetting up and down on the bead pellet to get it to come off the side of the well and mix completely into solution. There should be minimal to no clumps of beads and the liquid should be homogeneously brown. Pipette carefully to avoid bubbles as much as possible. Tapping the plate down on the bench can help droplets get into the liquid. Also try to move quickly across the plate because there can be DNA loss when the beads over-dry
- Place the plate on the orbital shaker for 5 minutes 200rpm
- After 5 minutes, place the plate on the magnet stand and back on the shaker for 2 minutes
- Remove the plate and the magnet to the lab bench and remove 16ul of clear liquid into a new 96 well plate in the same layout. Avoid pipetting beads, if some beads get sucked up, adjust the volume lower until they are avoided
- Label the new plate
- Keep the plate on ice if QCing immediately, if waiting to QC, cover in a foil seal and freeze at -20

### 6. QC: Quantify and Validate Size

**Materials**

- Biotium Qubit assay kit or Plate Reader assay kit (depending on number of samples)
- D5000 screentape, buffer, and ladder OR D1000 screentape, buffer and ladder
- Qubit tubes

**Notes**

- Work at the Pre-PCR Prada Lab bench
- For less than 36 samples, use the Qubit to quantify the libraries
- For more than 36 samples, use the Plate Reader to quantify the libraries
- If you have 96 samples, 12 of them will not fit on the plate reader plate and will need to be Qubited (one row of the assay plate has standards in it)

**DNA Quant**

- Follow the [Qubit](https://docs.google.com/document/u/0/d/17T3hY-7SahpaQwVxecqTkfk7OkjqxVaKmGaz8eXbdDU/edit) and/or the [Plate Reader protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols/Biotium-BroadRange-DNA-PlateReader.md) for quantifying the DNA
- Record your quantifications in a google sheet for the project
- Note any samples that have &quot;too low to read&quot; or below 3ng/ul DNA, these are not enough for sequencing and probably should be re-done

**TapeStation**

- Choose ~10% of your samples to tapestation, if samples did not have any measurable DNA, do not choose them
- Get the D5000 buffer, D5000 Ladder, and screen tape out of the fridge at least 30 minutes before use to equilibrate them to room temperature
- Use the tapestation specific strip tubes and tube caps to set up 1 or 2 strip tubes to run your samples
- A ladder is always run in the first well of the 1st strip tube, so for example if you want to run 8 samples you will have to use 2 strip tubes to account for the ladder that is in the first tube
- Vortex and spin down the ladder and the buffer
- Add 10ul of D5000 buffer to each tube being used plus the one for the ladder (**if you are using the D1000 reagents, use 3ul buffer here. That is the only difference between the two**)
- Add 1ul of D5000 ladder to the first tube
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

**Size Validate**

- Before turning off the TapeStation, use the analysis software to get an average size of the libraries
- Create a region in the electropherogram that encompases the peak and look in the table below and record the size in bp of the average length of the peak
- Do this for each TS library you&#39;ve ran
- Average all the sizes together to get an estimated average library size for all your libraries (should be around 300-400)

### 7. Dilution to 10uM, Pooling by Plate and Final Tubes for Sequencing

**Dilution to 10uM**

- In your spreadsheet, create a column for concentration in nM
- The calculation is: (concentration in ng/ul / (660 \* average size of fragments)) \* 1000000
- Example calculation for libraries with 400bp size and with 13.5 ng/ul:  **(13.5/(660\*400))\*1000000 = 51.13nM**  
- Most sequencing companies want libraries sent to them at 10-15uM concentration, so each library needs to be diluted to 10uM and combined together
- Only libraries that do not have the same index can be pooled together. The max we have is 192 unique dual indexes (illumina plate A and plate B), so that is the maximum number of libraries you can pool together
- Create a column for dilution. Calculate the amount of library is needed to make 10uM concentration in 15ul. Calculate how many nmoles are needed in 15ul (15\*10= 150) and divide that by the concentration of DNA in nM: **(15\*10)/concentration in nM**
- Then create a column for the amount of water to add up to 15ul

Example:

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-09%20at%206.33.26%20PM.png)

- For a plate of samples it is best to copy and paste this information into a plate layout and print it out for easy viewing while pipetting. Make sure to paste as values first before pasting transposed into the plate layout
- Add the 10mM tris HCl first to every well in the plate, it can be helpful to highlight after you&#39;ve added each sample
- Vortex and spin down your libraries and have them on a ice bucket or plate. Then add the correct amount of library to each corresponding well in the 10nM dilution plate
- Example plates:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-09%20at%206.33.09%20PM.png)
- Cover and vortex and spin down the plate when you are done
- If you are done for the day the dilution plate can be frozen at -20 degrees
- If pooling immediately, set up 12 temporary strip tubes
- Use a multichannel set to 4ul to pool together each column in the 10nM dilution plate: Pipette 4ul of each sample in the first row into the new strip tubes. Then pipette 4ul from each sample in row B also into the new strip tubes. Do this for all the rows in the plate. After you have done every row, the strip tubes should have 32ul in each
- Cover and freeze the dilution plate
- Combine all liquid from the strip tubes into one 1.5mL tube with a p200 pipette set to ~32ul
- The 1.5m tube should have ~384ul (4\*96) in it
- Keep this tube on ice if using immediately, freeze at -20 if not

**Combining Pooled Tubes/Preparing for Sequencing**

- Vortex and spin down the pools (either 1 or 2 tubes, depending on how many samples you library prepped)
- If you are combining the pooled samples from 2 plates, make label a new 1.5mL tube with the final library name
- Combine 25ul of each tube into the new tube
- Vortex and spin down the new tube
- **Even if you are not combining pools of 2 plates, make a new 1.5mL tube with 50ul of the pooled libraries : this way you only send part of what you have for sequencing**
- Wrap the lids in parafilm and place in the -20 freezer until you are ready to send to be sequenced
- Prepare the spreadsheet for sequencing: you will either get one from Carlos, or if sequencing with GenoHub there is a blank spreadsheet [here](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/Whole_Genome_Library_Preps/Files/Blank_Genohub_Sampl_%20Submission_Sheet.xlsx)
- Fill out the sheet with all the information: example sheet below

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-09%20at%206.42.59%20PM.png)
- For the index sequences, see [this file](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/Whole_Genome_Library_Preps/Files/Blank_Genohub_Sampl_%20Submission_Sheet.xlsx)
