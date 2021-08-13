# ddRAD Library Prep Protocol Puritz Lab

Expanded from ddRAD/EpiRAD joint protocol from Puritz/Putnam lab,
modified from Jay Diamond&#39;s notebook: [http://onsnetwork.org/jdimond/2016/08/](http://onsnetwork.org/jdimond/2016/08/)  
And [this protocol ](https://docs.google.com/document/d/1T2B89UGMEoGwuLcm7Ru2biW9UM1TfACEntAWV-eF8yo/edit)  
And [original ddRAD protocol](http://journals.plos.org/plosone/article/file?type=supplementary&amp;id=info:doi/10.1371/journal.pone.0037135.s001) for reference  
**This is written to match the bead-in protocol from Jon**  
Last modified 20210813 by Maggie Schedl

**Steps**

1. DNA extraction and quantification (see outside protocols)
2. Choosing size range and enzyme pair (see outside protocol)
3. Sample layout and multiplexing planning
4. Test digestions
5. DNA standardization and initial cleanup
6. Restriction enzyme digestion
7. 1.5X cleanup after digestion
8. Plate reader quantification (see outside protocol)
9. Ligation calculation and adapter annealing and diluting
10. Adapter ligation
11. Ligation efficiency test
12. Pool samples and 1.5X clean up twice
13. BluePippin Size Selection
14. PCR and index addition
15. 1X Cleanup after PCR
16. Final validation with Qubit and TapeStation (see outside protocols)

# 1. DNA Extraction and Quantification

- DNA extracted from samples using a Zymo Kit and eluted in 100ul of 10mM Tris-HCl
- [Example protocol for DNA extraction](https://meschedl.github.io/MES_Puritz_Lab_Notebook/2020-08-14/HSC-DNA-Protocol)
- Optimal DNA quantity is between 200-500 ng, this means concentration should be higher than 10ng/ul, however over 5ng/ul can work
- Optimal DNA quality high molecular weight \&gt; 10kb
- Quantification can be done with the [qubit protocol](https://meschedl.github.io/MESPutnam_Open_Lab_Notebook/Qubit-Protocol/) or with the plate reader and the [AccueBlue assay](https://biotium.com/wp-content/uploads/2017/11/PI-31007.pdf)
- To visualize DNA quality run a 1.5% agarose gel with a 1kb ladder, or run the genomic DNA TapeStation

## 2. Choosing Size Range and Enzyme Pair

- Use [this protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/ddRAD_Library_Prep/Puritz_Pick_ddRAD_Size_Selection.md) for picking the size range and enzyme pair to use
- If there is an already known optimum enzyme pair and size range for your species this step can be skipped

## 3. Sample Layout and Multiplex Planning

Please read this fully before starting, this is not a protocol, this is guidelines to follow. How you want something laid out in a plate that is visually easy and pipettable for you is probably unique.

- Determine how many samples can be sequenced on 1 lane (this will tell you how many need to be multiplexed to be individually traceable and if you have to split up your samples). Below is an example
  - Based on the planned sequencing platform, find out how many read-pairs are generated for 1 lane (example, 300-350 million)
  - Use estimation for how many fragments each sample will have, this is from choosing the enzyme pair and size range (example, 30,000)
  - Determine the amount of coverage you want per fragment (example, 30X)
  - Potentially, 25% of reads might be lost to poor sequencing and PCR duplicates
  - Equation: # read-pairs / # fragments / coverage \* 0.75 = number of samples
  - Example: 350,000,000/30,000/30\*.75 = 291 samples on 1 lane of sequencing
- Know the limits of your multiplexing capabilities, this partially depends on the enzyme pairs chosen. These are how many barcoded adapters we have for each pair
  - PstI and MspI: 12 adapters for PstI (i5) and 4 adapters for MspI (i7)
  - PstI and EcoRI: 12 adapters for PstI (i5) and 4 adapters for EcoRI (i7)
  - SphI and EcoRI: 3 adapters for SphI (i5) and 4 adapters for EcoRI(i7)
  - SphI and MspI: 3 adapters for SphI (i5) and 4 adapters for MspI (i7)
- There are also index barcodes on the PCR primers, we have 11 pairs (they stay paired), this means the maximum capabilities for each enzyme pair are calculated by this equation:  # i5 \* #  i7 \* 11 = unique multiplexed samples
  - PstI and MspI: 12\*4\*11 = 528
  - PstI and EcoRI: 12\*4\*11 = 528
  - SphI and EcoRI: 3\*4\*11 = 132
  - SphI and MspI: 3\*4\*11 = 132
- Samples are pooled (combined) after adapter ligation before size selection. The maximum amount of samples that can be pooled together is calculated by multiplying the number of i5 and i7 barcodes (the samples will only have those at this point)
  - PstI and MspI: 12\*4 = 48
  - PstI and EcoRI: 12\*4 = 48
  - SphI and EcoRI: 3\*4 = 12
  - SphI and MspI: 3\*4 = 12
- Another thing to note is that the cassettes for size selection have 5 lanes on it. It is best to run the Blue Pippin for size selection as few times as possible. If you are able to restrict your planning to five pools, that can be a good choice. But it&#39;s not necessary, you can use the Blue Pippin more than once.
- If you are going to be using less than 8 PCR primer pairs (being used for sequencing together on one lane), you will have to make sure the pairs you decided on are colorimetrically compatible (if you are using more than 8, there should be enough diversity to not need to check). Most everything we sequence now is on "two channel" chemistry. That means that the sequencer only reads in two colors: red and green. T and G nucleotides read as green, A and C nucleotides read as red. The index barcodes are on every sample and get read during sequencing at the same time. The sequencer cannot read the flow cell if all the same color comes up at one time (if there are only A/C or T/G). See the Color Balance section of this [Illumina info sheet](https://support.illumina.com/content/dam/illumina-support/documents/documentation/chemistry_documentation/experiment-design/index-adapters-pooling-guide-1000000041074-05.pdf). Our indexes are the TruSeq CD Indexes (Dual Indexing) on pg 14 of this document, however we cannot use their pooling guide. We pair our indexes and use them only once, not combinatorially. This mitigates any [index hopping](https://www.illumina.com/techniques/sequencing/ngs-library-prep/multiplexing/index-hopping.html) that could happen in patterned flow cells. But this means you can't use their guide, you'll have to pick the indexes yourself by color coding the bp and trying to make it an even split between green and red at each bp position. Example index check:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.07.52%20AM.png)
- All index and barcode sequences can be found in the [Puritz labs oligo list](https://docs.google.com/spreadsheets/d/1K0JaTR9PWUAhTSiKEU6sEJeHmLmcyGW0Vrs57O5GRPs/edit?usp=sharing)
- Visual representation of a completed library:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.07.59%20AM.png)
- Determining how to multiplex is also determining how to lay out your samples. It is best to do the library prep in plates, with one or two pools in each plate. When making the layouts for your library prep:
  - Randomize all your samples
  - Choose 1 or 2 samples with a lot of DNA, these will be technical replicates that will be in each pool
- First start with deciding how many pools you will have, then you can try to evenly split your samples into each pool (the maximum number of samples in a pool is 48). You&#39;ll want to try to balance having more pools (easier to multiplex the index barcodes), and more samples in each pool (better balance for the adapter barcodes, and less times running the Blue Pippin)
- Add in your technical replicate (or two) into each pool (not more than 48)
- Plan placement of the samples into a plate format in a way that is ideally the same layout for each pool, and also corresponds to what adapter barcodes they will get. This means that it is easiest to add i5 adapters by column, because there are 12 columns and 12 unique i5 adapters. Similarly there are 8 rows, and 4 unique i7 adapters. Following this layout, a pool can only have samples that are placed in 4 rows. **Also make sure that there is 1 well open in each pool for the ligation test sample (used in step 11**). That well will be left blank until step 10. You will likely not have the exact right amount of samples to fill the plate completely and use all barcodes. Look at these 3 examples of ddRAD plate layouts done with this protocol:
- Partial plates, pool sizes around 22 samples each

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.08.06%20AM.png)

- Partial plates, pools sizes at 37 samples each, also the layout with the full multiplexing plan

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.08.13%20AM.png)

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.08.17%20AM.png)

- Plates with 47 samples in each pool (maximum with room for the ligation test)

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.08.30%20AM.png)

- Additionally you will need to make a spreadsheet/table of each sample and what barcodes and indexes they will be getting, like this

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.08.35%20AM.png)


## 4. DNA Dilution and Initial Cleanup

- After quantification, determine DNA quantity in each of the samples. You should have already done this in the chooseing enzyme step if this is a new library prep. If not, follow below
- The input amount for the library prep should be between 200-500ng per sample, and the volume we start with is 50ul (or less). That means all your samples should have a concentration of DNA high enough for at least 200ng in 50ul, which is 4ng/ul or higher. If you have any samples below 10ng/ul, you&#39;ll have to base the amount of starting DNA off them. For example if all your samples are above 10ng/ul except one that&#39;s at 7ng/ul, you&#39;ll have to use 350ng as your starting DNA amount (this is 7ng \* 50ul). You want the starting amount for each sample to be the same to standardize, which is why you have to adjust to the smallest sample. If all your samples are above 10ng/ul concentration, you can use 500ng for each sample
- Calculate volume of each sample needed for 500ng (or how many ng you have decided on) and transfer that to a (new) 96 well plate, in the order you have planned above
- Calculate volume of 10mM Tris HCl needed to add up to 50ul for each sample well
- Example calculations:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.08.43%20AM.png)
- For doing plate, it&#39;s good practice to print out a plate map, a DNA volume map, and a water volume map: Example:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.08.48%20AM.png)
- Arrange your samples on a black rack (has 96 spots) in the same layout as you have planned. Do this for 1 plate at a time. You can highlight off the sample layout as you place the sample DNA tube into the correct spot
- Thaw the samples and keep them on the large ice bucket while you&#39;re working
- Set up a plate, write out the date, the plate name, and any other info. Put the plate on a cooling rack (purple, in the bottom of the -20)
- Add the 10mM Tris HCl to each well, it can be tedious so you can highlight off when you&#39;ve finished adding each one. Sometimes it can be helpful to use a silicon mat to block off the rest of the plate so you only look at 1 row at a time
- Before using each sample vortex and spin down the tube
- Add the planned volume of DNA to each well in the plate. Again it can be useful to use the silicon mat to keep track of rows
- Once the plate is finished, you&#39;ll want to cover it with a foil seal, label it, vortex it (you can use a regular vortexer) and spin it down using the large centrifuge in the corner
- Store the plate on ice if using later or put in the freezer if using another day
- You can decide whether to make the dilution plates for your whole project at once or to do plate by plate

## 5. 1X cleanup

- Make a fresh 50mL conical of 80% ethanol. Use 40mL 100% ethanol and 10mL of nuclease free water
- The volume of KAPA pure beads needed for a 1X cleanup is 50ul. With a multichannel add 50ul of beads to each well in the plate with sample. You can pipette out the right amount + some error into a trough for the beads (ex for 96 samples that&#39;s 4,800ul, which can be increased to 4,900ul for a little extra)
- Add beads slowly to avoid bubbles and pipette up and down at least ten times to mix the beads with the DNA. It should be homogeneously brown when mixed
- Change tips between every use
- After adding beads, put the plate on the orbital shaker (next to the Qubit) at 200rpm for 15 minutes
- After 15 minutes, put the plate on the white magnet rack and return it to the shaker for another ~3 minutes
- The solution should be clear in each well with a small brown pellet on the side with the magnet
- Remove the plate from the shaker and bring it back to the bench
- Use the multichannel to remove 90ul of the clear supernatant from each tube: Slide the pipette tips down the side of the tube opposite the magnet as to not disturb the beads. Try to keep heights of the tips even across the channels. Pipette up slowly to avoid bead suction. Discard of liquid in a trough/basin
- Make a basin with 80% ethanol
- Add 200ul 80% ethanol to each well in the plate, keeping it on the magnet. Pipette onto the side of the wells opposite of the beads to avoid disturbing them
- Remove the supernatant wash (200ul) and discard into the waste basin. Avoid pipetting on the side with the beads
- Add 200ul 80% ethanol to each well in the plate, keeping it on the magnet/Pipette onto the side of the wells opposite of the beads to avoid disturbing them
- Remove all the supernatant wash (200ul) and discard into the waste basin. Avoid pipetting on the side with the beads
- Make sure all liquid is out of each well by going back in with the multichannel for the p20 pipette set to 20ul and suck up any extra liquid at the bottom of each well
- Let samples air dry ~2 minutes (ethanol should evaporate but the beads should not crack)
- Make a basin with 10mM Tris HCl, enough for each sample (70ul each)
- Add 70ul of 10mM Tris HCl, adding directly to the bead pellet this time by dripping slowly onto the beads. Pipette up and down by dripping onto the beads to resuspend the beads in every well. This may be hard with the multichannel, continue pipetting for them all. This is it, the beads are staying in from this point
- Once all are added, you can cover the plate in a labeled foil seal (if you are done for the day or if you need to centrifuge)
- Tap down any droplets, or if lots of bubbles, a very brief centrifuge in the large centrifuge is ok
- If you are going onto the next step in the same day, leave the plate out. If you are done for the day, cover the plate in a foil seal and store in the **4 degree fridge** (the beads cannot be frozen)

## 6. Digestion USE FILTER TIPS FOR ALL PIPETTING

- The next step is to digest the DNA with the two enzymes, this is done with the beads in, so they can be re-used at a later step
- If your plate was in the fridge, take it out and spin it down to collect all the liquid in the large centrifuge
- Thaw cutsmart buffer on ice and take out the 2 enzymes you need and keep them on the ice as well (depending on how many you&#39;re doing at once, you may need more than one tube of each of these)
- Once the buffers are thawed, vortex and spin them down. Same with the enzymes
- Make a master mix on ice of the digestion mix. Generate an _n_ number which is the number of wells/samples + ~5% for pipette error. Ex: the plate above has 72 samples and 5 for error is 77
  - 8μl Cutsmart Buffer (10X)  \* n =
  - 1μl enzyme1 \* n =
  - 1μl enzyme2 \* n =
- Add the larger volume first, then the smaller ones
- Vortex and spin down the mix and keep on ice
- Each well gets 10ul of master mix (total volume in each well is 80ul). You can use the multichannel by making strip tubes to take from. Example: the plate above has 8 rows and 10 columns (or less). Set up 8 strip tubes to pipette by column. In each tube add the amount of total master mix volume needed by that row (plus a little extra). For 10 columns, ~103ul is needed. For 9 columns, 92ul is needed, and for 8 columns, ~82ul is needed. Like so:

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.08.54%20AM.png)
- Use the multichannel to add 10ul of enzyme mix to each well. Change tips between each well. The final volume in each well should be 80ul
- Use a p200 set to 30ul to pipette mix 10 times
- Seal the plate with a labeled foil seal
- Centrifuge the plate briefly in the large centrifuge to collect all liquid
- Put the plate in the thermocycler you have signed up for. Make sure you have signed up for this thermocycler overnight because the program goes for 12 hours
- Login to the &quot;mes&quot; user with the password &quot;8888&quot;, put the plate in the thermocycler and close the lid
- Choose the program &quot;12 hr digest&quot; and press start. This incubates at 37 degrees C for 12 hours and then goes to 4 degrees
- After the program is done, it goes to a 4 degree C hold. The next morning the plate can be put in the 4 degree fridge for storage

## 7. 1.5X Bead Clean After Digestion - this removes any left over enzyme and buffer in your wells and keeps all DNA

- Make PEG-NaCl if not made previously:
  - PEG-NaCl: the salt solution that the beads are in, and this solution facilitates binding of the DNA to the beads. Keep freshly made PEG in the fridge when not in use, and keep it wrapped in foil. To make PEG, use a 50mL conical with:
  - 25mL of 5M NaCl solution (use a 5mL pipette for this)
  - 10g of Polyethylene gylcol 8000 (use a weigh boat, scooper, and scale by the microwave)
  - Nuclease Free water up to 49mL
  - Invert and vortex a few times, then mix on the orbital shaker for a while to combine
- If PEG-NaCl is from the fridge, take it out and let it get to room temp (similar to how you would with beads), this will take at least 60 min
- Take plate out of fridge and let get to room temp (takes about 5-10 min)
- Make a 50mL conical with fresh 80% ethanol: 40mL 100% ethanol and 10mL nuclease free water
- Make a trough/basin for PEG, waste, Ethanol, and 10mM Tris HCl
- Calculate how much PEG you&#39;ll need: 80\*1.5 = 120ul. 120ul \* number of samples
- Add that much PEG-NaCl plus a little extra into a basin. PEG-NaCl is very viscous, so pipette slowly when using it
- Use the multichannel to add 120ul of PEG-NaCl to each well of sample in your plate. Pipette slowly because it is viscous. Pipette mix at least 20 times because you want to mix the beads and everything very well. The volume in each well will basically be at its maximum, so be careful
- Once all of your sample wells have PEG, put the plate on the orbital shaker for 15 minutes at 200rpm to help bind the DNA to the beads
- After 15 minutes, transfer the plate to the white magnet rack with the metal posts, **put this back on the shaker** for at least 5 minutes. It will take a while for the beads to come to the magnet on this cleanup because the volume is so large. Be patient waiting for the solution to become clear and the beads to form a pellet on the side of the tube with the magnet
- When it&#39;s ready, remove 190ul of the clear supernatant from each well using the multichannel and expel it into a waste trough. Slide the tips down the side of the wells opposite from the bead pellet
- Add 200ul 80% ethanol to each well
- Remove 200ul of the supernatant from each well, sliding the tips down the side of the wells opposite from the bead pellet
- Add 180ul 80% ethanol to each well
- Remove 200ul of the supernatant from each well, sliding the tips down the side of the wells opposite from the bead pellet
- Make sure all liquid is out of each well by going back in with the multichannel for the p20 pipette set to 20ul and suck up any extra liquid at the bottom of each well
- Let wells sit open to &quot;dry&quot; for 2 minutes. You want extra ethanol to evaporate but you don&#39;t want the beads to dry until cracked
- Use a basin with 10mM Tris HCl (33\*number of samples + a little extra)
- Resuspend the beads in 33ul of 10mM Tris HCl. Pipette up and down to get the bead pellet off as best you can
- Keep the beads in!!!
- Cover the plate with a foil seal and store in the 4 degree fridge if not quantifying that day
- If you are quantifying, cover with a silicon pad and keep on an ice bucket until ready

## 8. Quantify Digested DNA**

- Use the [Biotium AccuBlue Plate Reader Protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/Biotium-BroadRange-DNA-PlateReader.md)
- You don&#39;t need to use all the standards, the concentration will likely not be over 50ng/ul
- If you do the whole row A of standards, this is a good suggestion:
  - 2 0ng/ul
  - 2 2ng/ul
  - 2 6.25ng/ul
  - 2 12ng/ul
  - 2 25ng/ul
  - 2 50ng/ul
- It&#39;s best to use the same plate layout as you have, if you have blank wells and you don&#39;t need to use the whole 96 well plate for the assay, just leave those wells blank on the assay
- Follow instructions in the protocol for generating a standard curve and calculating the concentration of DNA in each well
- For all samples that can&#39;t be run on the plate reader, use the Qubit to quantify

## 9. Ligation Calculation and Anneal/Dilute Adapters USE FILTER TIPS FOR ALL PIPETTING

- Check to make sure all your adapters are planned at this step. These are the i5 and i7 barcodes
- Before starting, calculate how much DNA volume is 100ng for each sample. It can be helpful to put it in a plate format. Choose 1 or 2 samples that have a lot of DNA and use an extra space in the plate layout to do that sample twice. This sample will be for the ligation test.
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.09.00%20AM.png)
- Then calculate the volume of10mM Tris HCl up to 31ul for each well (31-volume DNA for 100ng)
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.09.04%20AM.png)
- **Anneal adapters and dilute adapters if you have not done so for this project yet**
- Anneal top and bottom adapters into 40uM annealed stock solutions
- Make 10X annealing buffer if not made already (in a 50mL conical):
  - 5mL of 1M Tris HCl
  - 5mL 5M NaCl
  - 1mL 0.5M EDTA
  - 39mL Nuclease free water
- Top and bottom adapters are resuspended to 200uM concentration (usually, check first). Vortex and spin down each before combining
- For each adapter combine in a strip tube:
  - 10ul top adapter (200uM)
  - 10ul bottom adapter (200uM)
  - 5ul 10X annealing buffer
  - 25ul Nuclease-free water
- Vortex and spin down and keep on ice
- Place all adapters to be annealed in the thermocycler adapter annealing program under the JONP login (password 1234) (40 min)
- **Dilute adapters to the working stock concentration for your prep**. Copy this calculator sheet [here](https://docs.google.com/spreadsheets/d/1DBh93pa4xPJ6hOlxv2NDROh4vMusbmNf6u5llE14FPk/edit?usp=sharing) and create a new sheet for your project.
  - Clear field B4 and replace with 0.1 (DNA mass for ligation in ug, we are doing 100ng or 0.1ug)
  - Clear fields B6 and B7. Go to the TapeStation results on the TS computer in the analysis software where the single digestions for the enzymes you are using are. For the first enzyme, pick a representative sample single digestion and create a region across the whole distribution. Write down the concentration in ng/ul (in the table below for the region). Convert to pg/ul by multiplying by 1000. That goes in field B6. Write down the molarity as nmol/l (in the table below for the region). Convert to pmol/l by multiplying by 1000. That number goes in B7
  - Clear fields C6 and C7. Repeat the process in the step above for the second enzyme
  - Look for fields B19, B20, C19, and C20. Those tell you how much of the 40uM annealed stock and **1x annealing buffer** to add to a new tube for the working concentration adapters for your project
  - Dilute the 10X annealing buffer by adding 5mL of the 10X annealing buffer to a new 50mL conical and filling it to 50mL with nuclease free water
  - Combine the working stock adapters with the 1X annealing buffer and annealed adapters at the appropriate volume in new strip tubes. Keep these on ice while using and freeze when not in use

## 10. Adapter Ligation USE FILTER TIPS FOR ALL PIPETTING

- Place the plate on the magnet and let the beads go to the magnet
- Label a new 96 well plate with the plate name and &quot;digested cleaned DNA&quot;
- Remove the volume of clear liquid in each well to their corresponding well in the new plate (~30ul). Do not pick up the beads
- Well by well, add back to the bead-plate the volume of DNA for each well for 100ng. The DNA goes back into the same well. Use a plate map to avoid confusion. For the ligation test sample(s), add them in where you planned them to be extra in the plate
- Add the calculated amount of 10mM Tris HCl needed to increase the volume to 31ul for each well
- Remove the plate from the magnet and keep on an ice bucket
- Foil seal the digested DNA plate and freeze at -20 in case you need to do the ligation again later
- Make the Ligation Master Mix (LMM) on ice. Vortex and spin down the buffer before use. Flick to mix the ligase and spin down. **Do not vortex the ligase**
  - 4μl  of 10X ligation buffer \* number of samples+0.5 =
  - 1μl of T4 ligase \* number of samples+0.5 =
- Flick to mix the LMM and spin down, keep on ice
- Aliquot the LMM into strip tubes for multichannel pipetting into each well. Each well gets 5ul of LMM. Use rows or columns, whichever is easier to pipette. Keep on ice
- Aliquot out the adapters into strip tubes for easy addition to your samples (by going down the column and across the rows). Make one set of strip tubes for i5 adapters (added down columns) and make one set of strip tubes for i7 adapters (added across rows). Each well will get 2ul of the correct i5 adapter and 2ul of the correct i7 adapter. Keep on ice
- Add 5ul of LMM to each well in the plate using the multichannel
- Add 2ul of the correct i5 indexes by multichannel pipetting down columns
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.09.10%20AM.png)
- Add 2ul of the correct i7 indexes by multichannel pipetting across rows
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%2011.09.14%20AM.png)
- Make sure that the ligation test sample(s) get LMM and adapters, however it does not matter which adapters they get
- Pipette mix the wells with a p200 pipette set to 25ul
- Foil seal the plate and spin it down in the large centrifuge
- Put the plate in the Thermocyclers in the RAD LIGA program in the JONP login (password 1234). This takes between 4-5 hours to run. The program goes to a 4 degree hold afterwards
- The plate can be taken out and put in the fridge until pooling

## 11. Ligation Test

- Pipette the ligation test sample(s) into new PCR strip tubes (40ul)
- Perform a 1.5X bead cleanup for each test sample. Briefly:
  - Add 60ul room temp KAPA Pure Beads to each sample and pipette mix 10X
  - Place on orbital shaker 15 min
  - Place on magnet rack and wait for solution to go clear
  - Remove clear solution without disturbing beads
  - Add 200ul fresh 80% ethanol to tubes
  - Remove solution from tubes
  - Add 200ul fresh 80% ethanol to tubes
  - Remove solution from tubes
  - Remove extra liquid with a p20 pipette
  - Wait ~2 minutes for excess ethanol to evaporate
  - Resuspend beads in 20ul Tris HCL
  - Place on orbital shaker for 5 minutes
  - Place on magnet rack and wait for solution to go clear
  - Remove clear solution from tubes into new strip tubes
- For each ligation test tube, there will be 2 PCR reactions, a 12 cycle and a 30 cycle PCR
- Make a PCR master mix on ice. Thaw ready mix and primers on ice. Vortex and spin down the ready mix and primers before use. Remember each ligation test gets 2 PCRs, so for 1 test samples the &quot;n&quot; number is 2.1 (error), for 2 test samples the &quot;n&quot; number is 4.2, etc. Use any primer set, 50X and 70X pair
  - 10ul KAPA HiFi HotStart Ready Mix \* &quot;n&quot;
  - 4ul nuclease free water \* &quot;n&quot;
  - 0.5ul 50X primer \* &quot;n&quot;
  - 0.5ul 70X primer \* &quot;n&quot;
- Make one set of strip tubes for the 12 cycle PCR. Make a second set of strip tubes for 30 cycle PCR
- Into each tube in both strip tube sets that is going to be used (depends on how many test samples you have) add 15ul of the PCR master mix
- Add 5ul from the cleaned test sample(s) into both a tube in th 12 cycle set and the 30 cycle set
- Vortex and spin down the tubes meant for the PCR
- Use two thermocyclers, set the 12 cycle tubes in the thermocycler programed for the 12 cycle RAD LIG TEST program (in JONP Login). Set the 30 cycle tubes in the thermocycler programed for the 30 cycle RAD LIG TEST program
- While that is running, make a small 1% gel to set ([gel protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols/Agrose-Gel-Protocol.md))
- After the program is done, run 10ul from each PCR reaction (use 2ul dye for 10ul sample) on the gel with a 1kb Plus DNA ladder for 1 hr at 80V
- You should see a smear on the gel for all of the wells, the 30 cycle samples will be brighter, and might have brighter/more amplification at the smaller fragments (because smaller fragments amplify better in PCRs, which is why we only do 12 cycles in the real prep). The smear shows that the fragments got the adapters so they could be effectively primed and amplified to a level that you can see on the gel. If there is no smear for samples on the gel, it means the ligation did not work and you should go back to step 9 to do the ligation again.

## 12. Pooling Samples and 2 1.5X Clean-ups

- Take the PEG-NaCl out of the fridge for ~30 minutes to get to room temperature and make new 80% Ethanol
- **For each pool:** Transfer the full 40μl of ligation reaction (times the number of wells you are pooling), including the beads to a single 2mL tube. It might help to pipette mix first to make sure to transfer them all. **At this stage, do not combine samples from different pools together. It is best to do the pooling and clean ups 1 pool at a time to avoid confusion**
- **For each pool:** split the 2mL tube into 4 1.5mL tubes with equal volume in each, using a p200 pipette 50μl repeatedly to make sure each tube has the same volume. You can calculate an estimate of the volume in each of the 4 tubes, but usually there has been some evaporation in some wells, so each is not exactly 40ul when you combine them together (you&#39;ll notice this in the step above)
- Add 1.5 times the volume of the 4 tubes of PEG-NaCl to each aliquot tube and pipette to mix. _This number will change depending on the number of samples per pool_
- Incubate the 4 tubes on shaker for 15 minutes
- Place tubes on the magnet bar (long one) and wait until the solution goes clear. You can pipette to encourage the beads to move to the magnet
- Remove as much clear liquid as you can without removing any beads (10-20ul less than the volume in there)
- Add 1000μl 80% EtOH to each tube while keeping it on the magnet
- Remove 1000μl of the EtOH from the tubes and discard
- Add 1000μl 80% EtOH to each tube
- Remove ALL EtOH carefully from each tube, use the p20 or p200 to remove any excess ethanol
- Let samples sit for ~5 minutes, to let the ethanol evaporate but not letting the beads completely dry out
- Remove tubes from magnet and add 40μl of 10mM Tris HCl to each tube, mix by pipetting, and incubate for 5 minutes on the shaker to make sure all the beads are separated from the tube wall
- **Stop! Qubit these tubes to make sure you did not loose DNA. Use Qubit Protocol**
- **You should have about 100ng \* how many samples per pool total DNA. To calculate total DNA, multiply the qubit value x 4 x 40. **
- Once confirming no dramatic DNA loss, recombine the 4 separated tubes back together into one tube (1 for each pool), this can be one of the tubes you already have samples in
- Add 1.5X PEG-NaCl (240μl) to each tube, mix by pipetting, and incubate on a shaker for 5 minutes
- Put the tubes on the magnet, wait until the liquid becomes clear, and remove as much of the clear liquid as you can
- Add 1000μl 80% EtOH to each tube while keeping it on the magnet
- Remove 1000μl of the EtOH from the tubes and discard
- Add 1000μl 80% EtOH to each tube
- Remove ALL EtOH carefully from each tube, use the p20 or p200 to remove any excess ethanol
- Let samples sit for ~5 minutes, to let the ethanol evaporate but not letting the beads completely dry out
- Remove tubes from magnet and add 60μl of **1X TE buffer** to each tube and pipette to mix. Incubate for 5 minutes on the shaker
- Put tubes back onto the magnet and wait until the liquid goes clear, then remove supernatant and transfer to a new strip tube and keep on ice
- **Repeat these steps for all pools that have gone through the ligation test and are ready to be combined. It is best to cleanup each pool 1 at a time to avoid confusion**
- **Qubit the pools after the two clean ups to make sure that there is DNA going into the size selection.**
- **These tubes can now be frozen.**

## 13. BluePippin Size Selection

- Take out the electrophoresis buffer and marker V1 from the fridge ~30 minutes before use so they can come to room temperature
- Label new strip tubes for each pool to be size selected
- Transfer 30ul of each ligation pool into their new strip tube
- Add 10ul of Marker V1 to each tube with 30ul of pooled samples. Vortex and spin down the tubes
- Items to bring to the Blue Pippin bench:
  - p20 pipette and p20 tips
  - 2 cassettes just in case one continuously fails tests,
  - electrophoresis buffer,
  - samples,
  - gloves,
  - pamphlet about the bluepippin from the cassette box,
  - Strip tubes for storing the sample after size selection,
  - 0.1% tween
  - Sharpie
- Plug in the BluePippin and turn it on (button on back) wait for the computer to boot up
- Calibrate the machine: place the calibration fixture black side down on the electrodes, close the lid and press calibrate on the software. The calibration fixture is a pink plastic rectangle, it&#39;s stored in a knit sock in one of the drawers next to the BluePippin
- Take out a cassette and inspect **carefully,** tap away any bubbles behind the elution chambers, make note if this cassette has some used wells, look to see if all buffer chambers are full, look for breaks or cracks in the gel (look at manual for pictures here to guide you)
- Place the cassette in the nest with the elution wells on the right. Remove the sticker seals
- One by one, in each elution well, remove the liquid in there and discard (should be 40-50ul) and replace with 40ul of fresh electrophoresis buffer. Use a p20 for this because it has thin tips
- Check sample well buffer levels to make sure they are full of electrophoresis buffer. Add in more if needed
- On the software, perform the continuity test by pressing &quot;TEST&quot;. The cassette must pass all lanes you are going to use, if some lanes have been run before it&#39;s ok if those fail, if it fails unused lanes, remove and replace all buffer in elution wells and try test again. If it continues to fail, use a different cassette
- To load, remove 40μl of buffer from each sample well to be used and replace with the 40uL of sample/Marker V1 solution. Do this one well at a time. Be mindful that the wells are numbered 1-5 on the cassette from the bottom up
- Select program in the software or go to the protocol manager tab and create a new one
- Make sure reference is set to internal for all lanes, if some lanes are not to be used turn the reference off on just those lanes
- Make sure the range of bp is what you want
- Make sure the marker on the top dropdown window is V1!
- Re-inspect the settings on the main page and name lanes if you want to. Press start if all is good
- The program will stop when elution is finished, it&#39;s good to check back in an hour or 2 hours
- Once done, remove the entire volume from the elution wells and place into new tubes, volumes range between ~35-50ul
- To get out any extra, add 40ul 0.1% tween to each elution well, wait 1 minute, and remove into separate tubes. In theory a % of the sample is recovered with a rinse with tween
- Review the run log to ensure that the standards were observed, if it didn&#39;t detect peaks then it won&#39;t elute that lane ever, so you might as well just stop it. Also look for spikes in the voltage early in the run: voltage near or above 2.5mV cause the DNA to run at unpredictable rates (despite the internal standards). If spikes are observed, check the size of the final library (post-PCR) and/or the pre-PCR elution on the TapeStation
- Samples can be frozen at -20 degrees C if not being used immediately

## 14. PCR and Index Addition USE FILTER TIPS FOR ALL PIPETTING

- **For each pool** you are going to set up 6 PCR reactions. This minimizes possible PCR biases but also amplifies the libraries to a good amount. If you are amplifying more than one pool at a time (say 5), it can be easier to carry out all the reactions on a 96 well plate instead of individual strip tubes
- Set up a plate or however many tubes you&#39;ll need to have 6 wells/tubes per pool. Label A, B, C etc as these are very temporary
- Thaw size-selected samples, ready mix, and 50X, 70X primers on ice. Vortex and spin down all before using
- Each pool needs a master mix because each pool gets their own 50X-70X primer pair
- Make a master mix for **each pool** (ex for 5 pools, you would make 5 mixes, each with their specific primer pair):
  - 10µl of 2X KAPA HiFi Hot Start Ready Mix \* 6.1 =
  - 4µl water \* 6.1 =
  - .5μl 20uM PCR primer 50X \*6.1 =
  - .5μl 20uM PCR primer 70X \*6.1 =
- Vortex and spin down the master mixes
- Pipette 15ul of each master mix into their planned 6 tubes or wells
- Add 5ul of DNA from a size-selected pool to their respective wells, and repeat for the other pools
- Cover the plate with a foil seal, vortex to mix, and spin down
- Put in the Thermocycler for amplification, 12 cycle RAD PCR program under JONP login
- Samples can be frozen afterwards, or continue to clean-up

## 15. 1X Cleanup after PCR

- Take out KAPA Pure Beads ~30 minutes before use and make fresh 80% ethanol
- Combine the 6 reactions into a single 1.5 mL tube, for a total of 120μl
- Add 1.5X of KAPA Pure Beads (180μl) to each pooled tube, mix by pipetting, and incubate on a shaker for 15 minutes
- Put the tubes on the long magnet rack, wait until the liquid becomes clear, and remove as much of the clear liquid as you can
- Add 1000μl 80% EtOH to each tube while keeping it on the magnet
- Remove 1000μl of the EtOH
- Add 1000μl 80% EtOH to each tube
- Remove ALL EtOH carefully from each tube, use the p20 or p200 to remove any excess ethanol
- Let samples sit for ~5 minutes, letting the ethanol evaporate, but the beads not dry out
- Take tubes of the magnet stand and elute the DNA in 35μl 10mM Tris HCl and incubate shaking for 5 minutes
- Place the tubes back in the magnet, and wait until the liquid goes clear. Remove all liquid and put into new strip tubes: this is your library!

## 16. Quantify and Validate

- UseBR dsDNA Qubit [protoco](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/Invitrogen-Qubit-Assay-Protocol.md)l. Run this twice, as in re-make the standards and new sample tubes
- Analyze the accuracy of the Pippin Prep and the addition of indexes by running a [D5000 TapeStation](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/D500-GenomicDNA-Tapestation-Protocol.md) or [D1000 TapeStation](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/D1000_Tape_Protocol.md) on all the samples 
- The PCR reaction adds 55bp of Illumina flowcell annealing sequences. Thus, library size after PCR should be similar across library indices
-  **It is critical that the sizes be similar between indices of this library (and all other libraries for which data are to be combined) to ensure that the loci included are the same**
- If the size ranges are not the same across samples are wrong, you have to go back to size selection with section 8 (why you save 30ul)
