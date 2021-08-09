# Preparation of D-Loop PCR Product for Sanger Sequencing

Prada Lab
Last Updated 20210705 MES

**Steps**
- Bead cleanup
- Qubit quantification (or plate reader depending on number of samples)
- Dilute DNA (1:5 or 1:10)
- Calculate and prepare sequencing plate(s)
- Prepare spreadsheet for GSC

### 1. 1X Bead Clean

**Notes**
- Bead cleans remove any left over primer, polymerase enzymes, and reaction buffer that is in the solution with your PCR product. Having that in there will disrupt the sequencing
- The PCR product will bind to the brown beads, and the beads are magnetic so you can separate the PCR product from the rest of the solution and wash away all the extra components, purifying the PCR product.
- Work at Post-PCR bench

**Steps**

1.	Take out MagBio beads at least 30 minutes before use so they come to room temperature. Swirl the beads to resuspend the settled beads
2.	Make fresh 80% ethanol each day you do a bead cleanup (use 40mL of 100% ethanol and 10mL of molecular grade water in a 50mL conical)
3.	Thaw D-loop PCR product (after gel is finished to confirm a band amplification) on ice
4.	You can cut off the tube that has the negative control, you no longer need it
5.	Spin down the thawed PCR to collect all liquid to the bottom of the tubes
6.	There should be 20ul of PCR product left (12.5ul of reaction, 12.5ul water added before gel, and 5ul removed for the gel)
7.	Add 20ul of MagBio beads to the first tube. Pipette slowly because the beads are viscous. Pipette to mix the tube 15 times slowly and gently, avoiding making bubbles
8.	Add 20ul of MagBio beads to the rest of the tubes in the same manner as step 7
9.	Cap all tubes and place them on the orbital shaker at 200rpm for 15 minutes
10.	After the samples have been on the shaker for 15 minutes, place them on the magnetic rack. To facilitate binding you can place the magnetic rack with the samples on the shaker for a minute or two
11.	Wait until the liquid inside of the tubes goes clear and the beads have migrated to the sides of the tube
12.	Remove the clear supernatant by carefully placing the pipette on the bottom side of the well away from the beads. Use a pipette set to ~5ul less than the amount of liquid that is in the tube: use 35ul. If you suck up any brown liquid that is the beads and you need to expel the liquid back into the tube and wait for it to go clear again. Expel of the liquid into a waste beaker
13.	Repeat for each tube always changing tips
14.	Add 150ul of fresh 80% ethanol to each tube gently changing tips
15.	Remove all the liquid in the tubes carefully without disturbing the beads (150ul) and expel the liquid in the waste trough
16.	Repeat ethanol wash: add 150ul to each tube gently changing tips
17.	Remove all the liquid in the tubes carefully without disturbing the beads (150ul) and expel the liquid in the waste trough
18.	Remove any remaining liquid by using a p20 set to 20ul on each tube to get anything left over
19.	Take the tubes off the magnet
20.	Use a p20 pipette tip to remove any droplets of ethanol that are visible on the sides of the tubes
21.	Resuspend the beads in each tube with 30ul of molecular grade water by pipetting up and down many times to get the beads entirely off the sides of the tubes and mixed in the liquid
22.	Repeat above step for each tube or well
23.	Place the tubes back on the orbital shaker for 5 minutes
24.	Prepare a set of strip tubes for the cleaned samples
25.	After the 5 minutes on the shaker, place the tubes back on the magnet plate
26.	When the liquid is clear, remove the  clear liquid into the new tubes for each sample. Avoid getting any beads in the final tube
27.	Samples can be frozen for later, or quantified immediately

### 2. Quantification


- Quantify the cleaned PCR product DNA concentration by using either the Qubit (less than 30 samples) or the plate reader (more than 30 samples)
- Work at Post PCR bench
- Qubit protocol
- Plate reader protocol

### 3. Dilute DNA : May not be applicable for all samples!

**Notes**

- For Sanger sequencing at the URI GSC the amount of DNA to send them depends on how long the fragment is. The equation for how many ng to send is
((number of bases / 100)) * 1.25) * 2
- For D-loop the calculation is ((400/100)*1.25)*2 = 10ng
- This means that the total amount of PCR product we need to send to the GSC is only 10ng. If you have PCR product that has greater than 10ng/ul concentration, it should be diluted before preparing for sequencing. It is always best practice to pipette over 1ul, which we want to avoid when possible.
- The volume of liquid sent to the GSC is 12ul total, and 2ul of that is one of the primers. So you have 10ul to use for DNA. Depending on the concentrations, you’ll have to decide if a 1:10, 1:5, 1:2, etc dilution will work to pipette over 1ul for 10ng but under 10ul
- Work at Post-PCR bench

**Steps**

1.	Decide what dilution factor will work on all samples (if possible, if not possible you can do more than one dilution factor but that's just harder on you). You'll want to dilute to the point that you can pipette over 1ul of PCR product for 10ng total DNA but less than 10ul. For example if your PCR product concentration is 25ng/ul, a 1:10 dilution would work very well. This would make the diluted concentration 2.5ng/ul (25/10). Then you can pipette 4ul of the diluted PCR product to get 10ng total DNA.
2.	Make a new column in your spreadsheet that has your qubit values for the new dilution concentration values. This is the qubit concentration divided by the dilution factor (25/10 in the above example). Note that each sample will still have a different concentration here, they are all just diluted by the same factor
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-09%20at%203.34.11%20PM.png)
3.	Make a new plate or tubes for the dilution for your samples
4.	Add the planned amount of water for the dilution to each tube/well. This will be the same for each sample. For example, if you are doing a 1:10 dilution on your PCR product, add 18ul to each well, and then you'll add 2ul of the PCR product. It's good practice to make more than what you will need, just in case you need to use the dilution more than once. It is also good practice to use more than 1ul of DNA, which is why it's 2ul and 18ul in the example, not 1ul and 9ul.
5.	Added the planned amount of PCR product to each tube/well for dilution. This will be the same for each sample. A multichannel can be used if convenient
6.	Cover the tubes or plate and vortex and spin down. Keep on ice if using immediately, freeze if using another day

### 4. Prepare Sequencing Plate (or tubes)

**Notes**
- You’ll also have to dilute one of the primers to send with your DNA. Sanger sequencing amplifies the fragment with one of the two primers. Primers are at a working stock concentration of 10uM, but need to be added as 2ul of 3.2uM concentration to the 10ul of PCR product
- Work at post PCR bench

1.	Calculate how much diluted primer you need to make. This is the number of samples * 2 because each sample gets 2ul of diluted primer
2.	Dilute the primer from the 10uM working stock to 3.2uM in a new temporary tube. Use the solution dilution calculator to help with volumes. For example if you had 15 samples, you'll need 30ul of 3.2uM primer. Plug in the info into the calculator: 10uM for the "stock", 30ul for the volume, and 3.2uM for the desired concentration. This gives you 9.6ul of the 10uM primer. Subtract 9.6 from 30 to get how much molecular grade water is needed to reach 30ul (20.4ul)
3.	Vortex and spin down the diluted primer and keep on ice until you're ready to use it
4.	In your spreadsheet, determine how much volume of diluted (or not) PCR product is needed for 10ng. In the above example, the diluted DNA is now at 2.5ng/ul. For 10ng total DNA, 4ul of the diluted DNA is needed (10/2.5)
5.	Determine how much molecular grade water will need to go with the 10ng of DNA so the total volume is 10ul. In the example with 4ul of diluted PCR product, you'll need 6ul of molecular grade water to equal 10ul for that sample. Make another column in your spreadsheet for this
6.	If you have samples organized in a plate, you can make a plate map for easy pipetting, or you can keep things in a spreadsheet (see last two columns)
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-09%20at%203.34.25%20PM.png)
7.	Aliquot the molecular grade water first into new plates or tubes on ice. Because each volume is different, it can help to highlight off each number after you add it
8.	Vortex and spin down the diluted and cleaned PCR product
9.	Add the calculated amount of diluted PCR product to each corresponding tube or well, so that each tube/well reaches 10ul total volume and 10ng total DNA. Because each volume is different, it can help to highlight off each number after you add it
10.	Add 2ul of the diluted primer to each tube/well
11.	Cover the plate with a foil seal or close caps on tubes. Label CP# etc for tubes or "Prada Lab samples for Sanger Sequencing, well A1-X" on the plate
12.	Vortex and spin down the plate/tubes
13.	Place tubes/plate in the -20 freezer until ready to bring to sequence
14.	Download the GSC spreadsheet template: https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/PCR/Sanger_Sequencing/Files/Sanger_GSC_Sheet_Template.xls
15.	Delete the column that says Plasmid (as we aren't submitting a plasmid for sequencing)
16.	Create a 3 letter and number code for each sample, this is for the GSC. For simplicity use CP for Carlos Prada and your first initial, such as CPJ, and number after that. Ie: CPJ1, CPJ2, CPJ3. Go in order of how your samples are either laid out in tubes or wells in a 96 well plate. Add these codes to your personal spreadsheet so you know which sample is labeled as which. Write in CPJ1 etc etc in the 1st column of the GSC sheet
17.	The template type is "PCR" and template size for D-Loop is 400bp
18.	The rest of the sheet are things you've already calculated, you provide all this information to the GSC so they know you prepared the samples properly:
  - The template stock concentration is the concentration of the factor diluted PCR products (2.5ng/ul in the example sample)
	- Ng needed of PCR template is 10ng
	- Volume of PCR template is what you've already calculated and added to each well/tube: how much volume of diluted template needed for 10ng (4ul in the example sample)
	- Volume water need is the other same calculation: 10 - PCR product volume (6ul in the example sample)
	- And volume 3.2uM primer needed is always 2ul
	- Make sure you are putting this information in the sheet in the order of the samples you have in tubes or plates
19.	Example sheet with example sample:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-07-05%20at%202.35.48%20PM.png)
20. Example Full sheet:
![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-09%20at%203.28.52%20PM.png)
21. Email the sample sheet to jatoyan@uri.edu and say you are bringing these samples to the Pharmacy delivery room
22. Put the tubes or plate on a rack and inside a plastic bag labeled "Prada Samples for Sanger Sequencing". Take this to the Pharmacy delivery room: 187 across from the fake CVS and leave in the freezer there
23. Sequencing happens on Tuesdays and Thursdays, so you will get your data back the day after it's sequenced
