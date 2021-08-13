# Puritz Pick Size Selection Range for ddRAD Library Prep Protocol

Last Updated 20210315 Maggie Schedl

**Steps**

- Pick and prepare test samples
- 1X Cleanup test samples
- Digest test samples
- TapeStation test samples
- 8X Cleanup after digestion
- Locus count estimation
- Deciding on enzymes and size range

**Background Info**

- Restriction enzymes recognize a certain sequence in a DNA strand, bind to it, and cut the double stranded DNA at that site. They leave a &quot;sticky end&quot; where either the forward or the reverse strand has an overhanging section of a few bases with no pairs (it&#39;s not a clean break)
- We have 4 different restriction enzymes that you can use for ddRAD library prep (\* is where it makes the cut)
  - PstI: cutsite 5&#39; CTGCA\*G 3&#39;
  - MspI: cusite 5&#39; C\*CGG 3&#39;
  - EcoRI: cutsite 5&#39; G\*AATTC 3&#39;
  - SphI: cutsite: 5&#39; GCATG\*C 3&#39;
- These 4 can be paired in 4 ways:
  - PstI and MspI
  - PstI and EcoRI
  - EcoRI and SphI
  - SphI and MspI
- We can only combine them 4 ways because of the way we have adapters that ligate to the cutsites. PstI and SphI both have i5 adapters that anneal to their restriction sites. MspI and EcoRI have i7 adapters that anneal to their restriction sites. For our library prep to work, we need to have both i5 and i7 adapters on each of our fragments
- We will also need to digest each test sample with each enzyme individually
- The reason we have to test different enzymes is because we want to get an ideal amount of fragments of DNA in a sequenceable size range, and this can be pretty different between organisms and genome sizes. ddRADSeq is reduced representation sequencing, where only a small part of the genome is sequenced. For us, we want something between 20,000-30,000 fragments of DNA per sample. Restriction enzymes cut up the DNA randomly into millions of fragments of all sizes, hundreds to thousands of base pairs long. The goal is to find a size range that is not too broad, not too narrow, and between 150-600bp, that would give you ~20,000-30,000 fragments. This is sort of a goldilocks situation, to get something just right. Our size selection capabilities can only go from 150-600bp, so we are limited there. And the machine that does the size selection (BluePippin) should not have a size range less than 50bp, and 100bp is better.

**1. Picking and Preparing Test Samples**

- First you&#39;ll need to determine how much DNA is going to go into each library prep. This way you can pick test samples that will have enough DNA left over after testing to still do the regular library prep
- The input amount for the library prep should be between 200-500ng per sample, and the volume we start with is 50ul (or less). That means all your samples should have a concentration of DNA high enough for at least 200ng in 50ul, which is 4ng/ul or higher. If you have any samples below 10ng/ul, you&#39;ll have to base the amount of starting DNA off them. For example if all your samples are above 10ng/ul except one that&#39;s at 7ng/ul, you&#39;ll have to use 350ng as your starting DNA amount (this is 7ng \* 50ul). You want the starting amount for each sample to be the same to standardize, which is why you have to adjust to the smallest sample. If all your samples are above 10ng/ul concentration, you can use 500ng for each sample
- You&#39;ll want to pick 3 test samples, and each sample will get 8 different digestions (4 individual and 4 pairs). This means you&#39;ll need samples that have at least 9 times the amount of DNA you just chose above, 8 for the tests and the 9th for the real library prep. If you are using 500ng for each library prep, then your test samples will need at least 4.5ug (4500ng) of DNA. If you are eluting your DNA from the extraction in 100ul, and use 10ul for QC, this is a concentration of 50ng/ul or higher (50\*90 = 4500).

**2. Cleanup Test Samples**

- Take out KAPA Pure beads at least 30 minutes before you&#39;re going to use them and swirl them gently to resuspend the beads
- With your three test samples, you will want to take out the volume required for 500ng and aliquot that into 8 tubes per sample. Then in each tube you will add in a volume of water that totals 50ul (see table below)
- Repeat this for all the samples, so you should have sets of 8 tubes
- Then you&#39;ll add 1X (1 times) the volume, or 50ul, of KAPA Pure beads to each tube. When you add the beads, pipette mix at least 10 times until the solution is homogeneously brown

| DNA ng/μl quant | Volume for 500 ng | Volume water to 50ul | 1X KAPA Pure Bead volume | Total volume in well |
| --- | --- | --- | --- | --- |
| 75 | 500/75= 6.66μl | 50-6.66= 43.33μl | 1\*50= 50μl | 100ul |

- After all the tubes have beads, put the strip tubes on the orbital shaker for 15 minutes at 200rpm to shake and allow the DNA to bind to the beads
- In the meantime, make fresh 80% ethanol for the washes. Use 40mL of 100% ethanol and 10mL of nuclease free water to make a 80% mix
- After the 15 minutes, take the tubes off the shaker and put on a magnet rack or plate and place back on the shaker for ~2-3 min to facilitate the beads going to the magnet
- Once the beads are on the magnet and the liquid looks clear, take the magnet rack or plate off the shaker and bring to your bench
- Carefully removed ~95ul of the clear supernatant in each tube by pipetting slowly from the side of the tube opposite the bead pellet
- Discard the supernatant in a waste trough
- If you suck up beads, release the liquid back into the tube, adjust the volume a little smaller, and try again
- Then add 150ul of fresh 80% ethanol to each tube
- Remove 150ul of the ethanol wash from each tube (avoiding the pellet) and discard into the waste trough
- Wash the bead pellet again by adding 150ul of fresh 80% ethanol to each tube
- Remove all the liquid from each tube (avoiding the pellet) and discard into the waste trough
- Use a p20 set to 20ul to get extra liquid at the bottom of the tubes and any droplets on the sides
- Let the beads dry for about 30 seconds
- Add 72ul of nuclease free water to each tube by adding it to the bead pellet. The beads should begin to resuspend into the water. Pipette over and over until there is no longer a pellet on the side of the tube and the liquid is homogeneously brown. Do this for each tube. Try to avoid bubbles or getting droplets on the side of the tubes
- Put the tubes on the orbital shaker for 5 minutes
- Then put the tubes on the magnet plate or rack for 2 minutes until the beads go to the magnet and the supernatant is clear
- Make new strip tubes: these will be your reaction tubes for the test. Each set of 8 will need to be labeled with the tubes saying: MspI, PstI, SphI, EcoRI, P/M, P/E, S/E, S/M. Also name them with the sample ID if it fits or 1, 2, 3 as place holders
- Remove 72ul from the tubes on the magnet rack and put in their corresponding tube in the newly labeled reaction tubes
- You can throw away the tube with the bead pellets after this

**3. Digestion Tests**

- Each sample (3) will get 8 different digestions (see above)
- To make sure each reaction is as similar as possible across the 3 samples, each reaction type is going to have a master mix, this means you&#39;ll make 8 master mixes
- Make master mixes on an ice bucket, and the Cutsmart buffer will have to thaw before use. Vortex and spin down the buffer and spin down the enzymes before pipetting
- It is easiest if you make these in a set of 8 strip tubes
- For the single enzyme digestions, the master mix is:
  - 8ul cutsmart buffer \* 3.1 = 24.8ul Cutsmart buffer
  - 1ul of nuclease free water \* 3.1 = 3.1ul nuclease free water
  - 1ul of enzyme (either PstI, MspI, EcoRI, or SphI) \* 3.1 = 3.1ul enzyme
- For the double enzyme digestions, similarly, the master mix is:
  - 8ul Cutsmart buffer \* 3.1 = 24.8ul Cutsmart buffer
  - 1ul of first enzyme \* 3.1 = 3.1ul enzyme 1
  - 1ul of second enzyme \* 3.1 = 3.1ul enzyme 2
  - \*\*Enzyme pairs are PstI/MspI, PstI/EcoRI, SphI/EcoRI, SphI/MspI
- Vortex and spin down mixes
- Use a multichannel to add 10ul of the master mix to each of your test sample tubes. Using the 8 strip tubes to store the mixes in the same orientation makes this easy. Make sure to change tips between the tubes
- Vortex and spin down the test sample tubes
- Put them in the thermocycler on the JONP login (1234) 12 hour RAD digest program. This goes for 12 hours at 37 degrees C then to a 4 degree hold. Do this overnight. If you&#39;re not going on to the next step right away, put the tubes in the -20 freezer

**4. 1.5X Cleanup after Digestion**

- If your samples are frozen, thaw them and spin them down
- Take out KAPA Pure beads at least 30 minutes before you&#39;re going to use them and swirl them gently to resuspend the beads
- Each tube should have 80ul in it, and this is a 1.5X cleanup meaning the volume of beads to add to each tube is 1.5\*80= 120ul beads. This ends up being the max volume that strip tubes can take. It&#39;s a lot, but this is the bead cleanup that&#39;s in the main protocol so it&#39;s good to get some practice with it on a smaller scale first
- Add 120ul of beads to each tube and pipette mix at least 10 times to mix
- After all the tubes have beads, put the strip tubes on the orbital shaker for 15 minutes at 200rpm to shake and allow the DNA to bind to the beads
- In the meantime, make fresh 80% ethanol for the washes. Use 40mL of 100% ethanol and 10mL of nuclease free water to make a 80% mix
- After the 15 minutes, take the tubes off the shaker and put on a magnet rack or plate and place back on the shaker **This time it might take 10 minutes for the beads to go to the magnet because the volume is so large, be patient**
- Once the beads are on the magnet and the liquid looks clear, take the magnet rack or plate off the shaker and bring to your bench
- Carefully removed 200ul of the clear supernatant in each tube by pipetting slowly from the side of the tube opposite the bead pellet
- Discard the supernatant in a waste trough
- If you suck up beads, release the liquid back into the tube, adjust the volume a little smaller, and try again
- Then add 200ul of fresh 80% ethanol to each tube
- Remove 200ul of the ethanol wash from each tube (avoiding the pellet) and discard into the waste trough
- Wash the bead pellet again by adding 200ul of fresh 80% ethanol to each tube
- Remove all the liquid from each tube (avoiding the pellet) and discard into the waste trough
- Use a p20 set to 20ul to get extra liquid at the bottom of the tubes and any droplets on the sides
- Let the beads dry for about 30 seconds
- Add 33ul of nuclease free water to each tube by adding it to the bead pellet. The beads should begin to resuspend into the water. Pipette over and over until there is no longer a pellet on the side of the tube and the liquid is homogeneously brown. Do this for each tube. Try to avoid bubbles or getting droplets on the side of the tubes. **This time it will be hard to get all the beads to get resuspended in the liquid because there are so many beads and such a small volume of water, do your best to get the beads resuspended in the water. Some brown will stick to the sides of the tubes and possibly even the pipette tip, it is unavoidable**
- Put the tubes on the orbital shaker for 5 minutes
- Then put the tubes on the magnet plate or rack for 2 minutes until the beads go to the magnet and the supernatant is clear
- Make new strip tubes and label the same as before
- Remove 32ul from the tubes on the magnet rack and put in their corresponding tube in the newly labeled reaction tubes
- You can throw away the tube with the bead pellets after this
- If moving on to the tapestation, the tubes can be kept on ice. If finished for the day, freeze the tubes in the -20 freezer

**5. TapeStation Test Samples**

- Each sample gets TapeStationed, so the TapeStation will have to be run twice (it&#39;s not enough to do a plate, and without a plate it only does 15 samples at once
- Take out 2 Genomic DNA screen tapes, the Genomic DNA buffer and Genomic DNA ladder out of the fridge 30 minutes before use
- Set up 4 tapestation strip tubes and 4 strip caps, separate them into sets of 2
- Label the first well in 1 of the strip tubes as L for ladder in each set (there needs to be a ladder each time it&#39;s run, but only 1)
- Then label the first set as the same as the test samples for the first 15 tubes
- Label the second set for all the rest of the tubes (there should be 1 full strip tube plus 2 on the second)
- Vortex and spin down the buffer and ladder
- Add 10ul of the buffer to each of the strip tubes you&#39;re going to use (should be 26 individual tubes in total), leave unused ones empty, do not rip off the strip
- Add 1ul of ladder to each of the ladder tubes
- Add 1ul of the digested sample to their corresponding TS tube
- Cap tubes and put on the IKA vortexer and press start (vortexes automatically for 1 min)
- Turn on the tapestation computer and login
- Then turn on the TapeStation
- Wait for it to stop making noise then click on the TapeStation controller software
- Spin down the strip tubes in a minifuge to collect any droplets
- Open the Tapestation and put the first set of tubes in the tube rack for 8 strip tubes with the ladder in the A1 position
- Remember the orientation of the tubes and uncap the tubes
- Put 1 new screentape in the tape nest with the barcode to the bottom facing the interior of the machine
- The software should recognize the tape
- Use the cursor to select all the tubes in the virtual tube strips on the software then label them with the sample ID and the enzyme(s)
- Close the lid and press start
- It should take ~21 minutes
- Once it&#39;s done, save the report to your folder or the Puritz lab folder on the computer
- Remove the used tape, tube strips, and tips
- Repeat setup for the second set of tubes, remember that there are only 9 samples in this one plus the ladder so label correctly in the software
- Put in a new tape and start again, this one will take less time, ~12 minutes
- Once it&#39;s done, save the report to your folder or the Puritz lab folder on the computer
- All TS tubes, caps, tips, and tapes can be thrown away. The partially used tape should be put back in the fridge and can be used again for up to 2 weeks from that day, so put the date on it and how many wells used (10)
- Digestion tests and enzymes should go back into the freezer

**6. Locus Count Estimation (on TS software)**

- It&#39;s easiest to do this on the TapeStation computer, you have to use the software that&#39;s on there to look at the files from the machine
- Copy [this spreadsheet](https://docs.google.com/spreadsheets/d/11Fy3yDb6HoeuIUUCFWYTcEjpmjtHNMMFDpJx730OE_g/edit?usp=sharing) in your project folder and call it &quot;Locus Count Estimation&quot;
- You&#39;ll be making one of these in separate tabs for each enzyme **pair** for each test sample, a total of 12 (4\*3). Label each tab with the sample name and enzyme pair
- Start with just one sample and 1 enzyme pair
- Add in the genome size estimate into field B3
- Open up the files from the TapeStation runs, go to File Explorer -\&gt; Documents/Agilent/TapeStation Data/ then find the date you did the TapeStation and the files should be in that folder
- These open up in the TapeStation analysis software (don&#39;t use the &quot;report&quot; PDF)
- Find the wells in the TS that have the sample you&#39;re starting with
- Set fields B8 and B9, this is done **once** for each enzyme pair and sample (ie once per tab in the sheet)
  - Choose 1 enzyme of the pair and go to the single digest well using the TapeStation Region viewing window
  - Click on Region Settings. Edit the region to go from 150-60000bp. Check &quot;this file&quot; and click apply
  - In the table below, use &quot;Average Size [bp]&quot; to add into your spreadsheet in field B8
  - Repeat region for the second enzyme in the double digestions (same sample) and put that average size in the B9 field in the spreadsheet
  - You can make note on fields I8 and I9 which enzyme is which if you want to
- Make a table underneath the calculation part in the spreadsheet that has column names &quot;fragment region&quot; &quot;mean fragment size&quot; and &quot;estimated fragments&quot;
- Go to the region viewing window for the double digest of those two enzymes for your sample
- Go to Region Settings and edit the region to be a range between 150 and 600bp, that is not less than 75bp, and not more than 400bp
- Make sure &quot;this file&quot; is checked and click apply
- On the table below the figures, look at average size. Put that number in field B4 in the spreadsheet
- On the table on the software, also look at &quot;% of total&quot;, put that number into a **decimal percent** (ex. if it says 5.6 you want to use 0.056) in field B2 in the spreadsheet
- On your mini table underneath the calculations, put in your fragment size range and the mean fragment size
- For estimated fragments put in the calculation from field B14 (after all the above numbers are put into the calculation)
- Repeat these steps for as many fragment regions as you want for these enzymes/samples, then move on to do the same for the other enzyme pairs and the other samples
- Remember you are aiming for something that comes out around 20,000-30,000 fragments in the estimated fragments section

**7. Deciding on Enzymes and Size Range**

- It might be obvious that there is only 1 size range and enzyme pair that works well/has an ideal amount of fragments
- If the same size range works for multiple enzyme pairs, try picking the pair that had the least variability across the samples
- If different size ranges are just as ideal, pick one that&#39;s larger than 50 bp if you can (ie 100bp wide)
- Also if different size ranges are just as ideal, again try picking the one that had the least variability across the samples
- Have a meeting with Jon about which pair and what range to chose
