# Stranded mRNA-Seq Library Prep used in EecSeq

#### Note that KAPA No Longer Sells this Kit and the Puritz lab is moving to use the mRNA HyperPrep Kit

### Annealing Custom Adapters That Inculde Restriction Enzyme Sites

Annealing buffer stock (10X):

| Component| Concentration|
|----------|--------------|
| Tris HCl, pH 8| 100 mM|
| NaCl|500 mM|
| EDTA| 10 mM|

For a 50mL conical of 10X annealing buffer:
* 5mL of 5M NaCl
* 500μl of 1M EDTA
* 5mL of 1M Tris HCl, pH. 8
* Fill rest of volume with nuclease free water

#### Custom Oligos needed to make adapters:

![](https://raw.githubusercontent.com/MarineEvoEcoLab/EecSeq/master/RNAadapter.png)

|Oligo Name| Sequence|Inline Barcode|
|----------|---------|--------------|
|Y-inline-SaIIa|CACTCTTTCCCTACACGACGCTCTTCCGATCTNNNNNNGTCGAC*T|NNNNNNGTCGACT|
|Y-inline-SaIIa_NO_N|CACTCTTTCCCTACACGACGCTCTTCCGATCTGTCGAC*T|GTCGACT|
|Y-inline-SaIIb|PA*GTCGACNNNNNNAGATCGGAAGAGCACACGTCTGAACTCCAGTC|NNNNNNGTCGACT|
|Y-inline-SaIIb_NO_N|PG*TCGACAGATCGGAAGAGCACACGTCTGAACTCCAGTC|GTCGACT|


### Anneal RNA Adapters
Single-stranded oligos need to be annealed with their appropriate partner before ligation. Then the annealed adapters have to be diluted to a working strength concentration.

1. To create Adapter SaIIa, combine Y-inline-SaIIa withY-inline-SaIIb in a 1:1 ratio in working strength annealing buffer (final buffer concentration 1x) for a total annealed adapter concentration of 40uM (for example, if purchased oligos are resuspended to an initial concentration of 100uM, use 40uL Y-inline-SaIIb, 40ul Y-inline-SaIIa, 10ul 10x annealing buffer and 10ul nuclease-free water). Pair Y-inline-SaIIa_NO_N with Y-inline-SaIIb_NO_N in the same fashion.
2.   In a thermocyler, incubate at 97.5°C for 2.5 minutes, and then cool at a rate of not greater than 3°C per minute until the solution reaches a temperature of 21°C. Hold at 4°C.
3.   Prepare final working strength concentrations of annealed adapters from this annealed stock (the appropriate working stock dilution for your experiment can be determined from the chart below). For convenience, it is possible to store the adapters at 4°C while in active use.

#### Adapter concentration will vary depending on overall RNA yield, see table below:
|Quantity of starting RNA|Adapter stock concentration (what you make for step 3 above)|Adapter concentration in ligation reaction|
|----|----|-----|
|100 – 250 ng|140 nM| 10 nM|
|251 – 500 ng|350 nM|25 nM|
|501 – 2000 ng|700 nM|50 nM|
|2001 – 4000 ng|1400 nM|100 nM|

For Puritz and Lotterhos 2017, we used 4000 ng starting RNA, but because of difficulties assessing and quantifying molluscan RNA, we chose to use a 700 nM working stock with a final reaction concentration of 50 nM.

### Using KAPA Stranded mRNA-Seq Kit using 1/2 rxn volumes
This should take 8-10 hours and can be done over 2 days safely.
Refer to manual during procedure (steps below are for notes and comments)

**Note: the input amount of RNA for this is a lot of RNA. Our lab has had success in making libraries with 4ug, 2ug, and 1ug as the input for each sample. That is 4000ng, 2000ng, or 1000ng. The starting volume is 25ul, sometimes RNA needs to be concentrated before use (such as with a vacuum centrifuge).**

#### Reagents

KAPA Stranded mRNA-Seq Kit (KAPA #KK8420). This kit includes all the enzymes and buffers required for cDNA library preparation from  isolation of poly(A)-tailed RNA. Kits include reagents for RNA fragmentation, 1st strand cDNA synthesis and 2nd strand synthesis/marking, and cDNA library preparation, including A-tailing, ligation and library amplification.

#### Additional reagents needed:

10 mM Tris-HCL (pH 8.0 - 8.5)
#### Equipment

* Magnetic stand and compatible tubes or striptubes
* Thermocycler
* SPRI purification beads (KAPA Pure Beads or AmpureXP)

Steps in Library construction:

* mRNA capture using magnetic oligo-dT beads
* Fragmentation using heat and magnesium
* 1st Strand cDNA Synthesis using random priming
* 2nd Strand cDNA Synthesis and marking, which converts the cDNA:RNA hybrid to double-stranded cDNA (dscDNA) and incorporates dUTP in the second cDNA strand
* A-tailing to add dAMP to the 3′-ends of the dscDNA library fragments
* Adapter ligation, where dsDNA adapters with 3′-dTMP overhangs are ligated to A-tailed library insert fragments
	* **NOTE** Here, we use the custom adapters
* Library amplification to amplify library fragments carrying appropriate adapter sequences at both ends using high-fidelity, low-bias PCR; the strand marked with dUTP is not amplified.
	* **NOTE** Here you can either multiplex your RNA libraries (if you are going to sequence them) using the PCR primers outlined in the Genomic Library Prep section. Or you can use the universal primer mix if you are not going to sequence them


## Procedure

### mRNA Capture

**Before mRNA capture beads can be used they must be washed with mRNA Bead Binding Buffer**
1. Resuspend beads thoroughly by gentle pipetting
2. For each library to be prepared, transfer 26.25 uL of the resuspended mRNA Capture beads into a 1.5mL tube
  	- Up to 48 libraries (1,260 uL) can be washed in a single tube
3. Place the tube on a magnet holder and incubate at room temperature until solution is clear
4. Discard supernatant and replace with an equal volume of mRNA Bead Binding Buffer
5. Remove tube from magnet and again resuspend the beads by pipetting
6. Place the tube on a magnet holder and incubate at room temperature until solution is clear
7. Discard supernatant and replace with an equal volume of mRNA Bead Binding Buffer
8. Remove tube from magnet and again resuspend the beads by pipetting

**mRNA Capture**
1. Combine the following for each RNA sample to be captured:

|Component|Volume|
|---------|------|
|RNA sample (in RNase-free water)| 25 μl|
|KAPA mRNA Capture Beads| 25 μl|
|**Total Volume per sample**| **50 μl**|

2. Mix thoroughly by gently pipetting up and down several times
3. Place the plate/tube in a thermal cycler and carry out the 1st mRNA capture program as follows:

|Step|Temp.|Duration|
|----|-----|--------|
|1st mRNA capture|65 °C|2 min|
|Cool|20 °C|5 min|


4. Place the plate/tube containing the mixture of KAPA mRNA Capture Beads and RNA on a magnet and incubate at room temperature until the solution is clear. Remove and discard the supernatant
5. Remove the plate/tube from the magnet and resuspend the beads thoroughly in 100 μl of KAPA mRNA Bead Wash Buffer by pipetting up and down several times
6. Place the plate/tube on the magnet and incubate at room temperature until the solution is clear. Remove and discard the supernatant
7. Remove the plate/tubes from the magnet and resuspend the beads in 25 μl of RNase-free water and pipette to mix
8. Place the plate/tubes in a thermal cycler and carry out the 2nd mRNA capture program as follows:

|Step|Temp.|Duration|
|----|-----|--------|
|2nd mRNA capture|70 °C|2 min|
|Cool|20 °C|5 min|

9. Add 25 μl of KAPA Bead Binding Buffer to the mixture of KAPA mRNA Capture Beads and RNA and mix thoroughly by gently pipetting up and down several times
10. Incubate the plate/tubes at 20 °C for 5 min (room temperature)
11. Place the plate/tubes on the magnet and incubate at room temperature until the solution is clear. Remove and discard the supernatants
12. Remove the tubes from the magnet and resuspend the beads in 100 μl of KAPA mRNA Bead Wash Buffer by pipetting up and down several times
13. Place the plate/tube on the magnet and incubate at room temperature until the solution is clear. Remove and discard the entire volume of supernatant

### mRNA Elution, Fragmentation, and Priming
1. Prepare the required volume of 1X Fragment, Prime and Elute Buffer as a master mix to be used for each sample as follows (multiply volume by number of samples):

|Component|Volume per sample|
|---------|------|
|Water| 5.5 μl|
|Fragment, Prime and Elute Buffer (2X)| 5.5 μl|
|**Total Volume per sample**| **11 μl**|

2. Thoroughly resuspend the KAPA mRNA Capture Beads with captured mRNA in 11 μl of 1X Fragment, Prime and Elute Buffer.

---

### Safe Stopping Point
Resuspended beads with captured mRNA may be stored at 4 oC for up to 24 hours. Do not freeze the samples as this will damage the beads. When ready, proceed to step below.

---

3.  Place the plate/tubes in a thermal cycler and carry out the fragmentation and priming program as follows:

|Desired Fragment Size| Temp.| Duration|
|---------------------|------|---------|
|100 – 200 bp|94 °C|8 min|
|200 – 300 bp|94 °C|6 min|
|300 – 400 bp|85 °C|6 min|

##### For Puritz and Lotterhos (2017), we chose 94 °C for 7 mins to have fragments between 150-250 bp, approximately the same size distribution as planned for our DNA libraries.

4. Immediately place the plate/tube on a magnet to capture the beads, and incubate until the liquid is clear. **Caution: To prevent hybridization of poly(A)- rich RNA to the capture beads, do not allow the sample to cool before placing on the magnet.**
5. Carefully remove 10 μl of the supernatant containing the eluted, fragmented, and primed RNA into a separate plate or tube.
6. Proceed immediately to **1st Strand Synthesis**.

### 1st Strand Synthesis

1. Make the 1st Strand Synthesis **master mix** on ice (multiply volumes by number of samples):

|Component| Volume needed for 1 reaction (1/2 reactions from kit protocol) with 20% |
|---------|--------------------|
|1st Strand Synthesis Buffer|5.5 μl|
|KAPA Script|0.5 μl|

2. On ice, assemble each 1st Strand Synthesis **reaction** as follows:

|Component|Volume per sample|
|---------|------|
|Fragmented, primed RNA eluted from beads| 10 μl|
|1st Strand Synthesis Master Mix| 5 μl|
|**Total volume per reaction**| **15 μl**|

3. Keeping the plate/tubes on ice, mix thoroughly by gently pipetting the reaction up and down several times.
4. Incubate the plate/tube in a thermocyler using the following protocol:

|Step|Temp.|Duration|
|----|-----|--------|
|Primer extension|25 °C|10 min|
|1st Strand synthesis|42 °C|15 min|
|Enzyme inactivation|70 °C|15 min|
|HOLD|4 °C|∞|

5. Place the plate/tube on ice and proceed immediately to **2nd Strand Synthesis and Marking**.

### 2nd Strand Synthesis and Marking

1. Make the 2nd Strand Synthesis and Marking **master mix** on ice (multiple volumes by number of samples):

|Component| Volume needed for 1 reaction (1/2 reactions from kit protocol) with 10% excess |
|---------|--------------------|
|2nd Strand Marking Buffer|15.5 μl|
|2nd Strand Synthesis Enzyme Mix|1 μl|

2. On ice, assemble each 2nd Strand Synthesis and Marking **reaction** as follows:

|Component|Volume|
|---------|------|
|1st Strand cDNA| 15 μl|
|2nd Strand Synthesis and Marking Master Mix| 15 μl|
|**Total volume per reaction**| **30 μl**|

3. Mix thoroughly by gently pipetting each reaction up and down several times.
4. Incubate the plate/tubes in the thermocyler using the following protocol:

|Step|Temp.|Duration|
|----|-----|--------|
|2nd Strand synthesis and marking|16 °C|60 min|
|HOLD|4 °C|∞|

5. Place the plate/tube on ice and proceed immediately to **2nd Strand Synthesis and Marking Cleanup**.

### Cleanup After 2nd Strand Synthesis and Marking

1. Bring KAPA Pure Beads to room temperature by taking them out of the fridge ~30 minutes before you need them, and swirl the bottle to resuspend the beads completely

2. Perform a 1.8X Bead cleanup by combining the following for each reaction:

|Component|Volume|
|---------|------|
|2nd Strand Synthesis reaction product (total volume)| 30 μl|
|KAPA Pure beads| 54 μl|
|**Total Volume**| **84 μl**|

3. Thoroughly resuspend the beads in each sample by pipetting up and down multiple times
4. Incubate the plate/tubes at room temperature for 15 min to allow the DNA to bind to the beads, having the tubes on an orbital shaker at ~200rpm is preferred
5. Place the plate/tubes on a magnet to capture the beads. Incubate until the liquid is clear
6. Carefully remove and discard 74 μl of supernatant in each tube
7. Keeping the plate/tubes on the magnet, add 200 μl of 80% ethanol
8. Incubate the plate/tube at room temperature for ≥30 sec
9. Carefully remove and discard the ethanol in each tube
10. Keeping the plate/tubes on the magnet, add 200 μl of 80% ethanol
11. Incubate the plate/tubes at room temperature for ≥30 sec
12. Carefully remove and discard the ethanol in each tube. Try to remove all residual ethanol without disturbing the beads
13. Dry the beads at room temperature, until all of the ethanol has evaporated.
  * **Caution: over-drying the beads may result in dramatic yield loss.**
14. Proceed immediately to **A-Tailing** immediately, or follow the Safe Stopping Point instructions below

---

### SAFE STOPPING POINT
* Resuspend the beads in 7.5 μl 1X A-Tailing Buffer (multiple volumes by number of samples):

|Component| Volume needed for 1 reaction (1/2 reactions from kit protocol)|
|---------|--------------------|
|Nuclease-free water|6.75 μl|
|A-tailing buffer (10X)| 0.75 μl|

* Cover the reaction and store at 4 degrees C for up to 24 hours. Do not freeze the samples as this will damage the beads. When ready, proceed to **A-Tailing after Safe Stopping Point**.

---

### A-Tailing
* A-Tailing is performed either directly after the 2nd Strand Synthesis and Marking Cleanup, or after the Safe Stopping Point, where beads were resuspended in 1X A-Tailing Buffer and stored at 4 °C for up to 24 hours.

#### A-Tailing immediately
1. On ice, make the A-Tailing Immediately **master mix** (multiple volumes by number of samples):

|Component| Volume needed for 1 reaction (1/2 reactions from kit protocol), including 10% excess|
|---------|--------------------|
|Water|13.2 μl|
|10X KAPA A-Tailing Buffer|1.65 μl|
|KAPA A-Tailing Enzyme|1.65 μl|

2. Resuspend the beads with cDNA with 15μl of the A-Tailing immediately master mix
3. Mix thoroughly by pipetting up and down several times.
4. Incubate the plate/tubes in the thermocyler using the following protocol:

|Step|Temp.|Duration|
|----|-----|--------|
|A-Tailing|30 °C|30 min|
|Enzyme inactivation|60 °C|30 min|
|HOLD|4 °C|∞|

5. Proceed immediately to **Adapter Ligation**.

#### A-Tailing after safe stopping point
1. To resume library preparation after storing the samples overnight, make the A-Tailing after safe stopping point **master mix** on ice (multiple volumes by number of samples):

|Component|  Volume needed for 1 reaction (1/2 reactions from kit protocol), including 10% excess|
|---------|--------------------|
|Water|5.775 μl|
|10X KAPA A-Tailing Buffer|0.825 μl|
|KAPA A-Tailing Enzyme|1.65 μl|

2. Combine the A-Tailing after safe stopping point master mix with the stored samples:

|Component|Volume|
|---------|------|
|Beads with dscDNA (in 1X A-Tailing Buffer)| 7.5 μl |
|A-Tailing Master Mix after Safe Stopping Point| 7.5 μl|
|**Total Volume**| **15 μl**|

3. Mix thoroughly by pipetting up and down several times.
4/ Incubate the plate/tubes in the thermocycler using the following protocol:

|Step|Temp.|Duration|
|----|-----|--------|
|A-Tailing|30 °C|30 min|
|Enzyme inactivation|60 °C|30 min|
|HOLD|4 °C|∞|

4. Proceed immediately to **Adapter Ligation**.

### Adapter Ligation

#### Adapter concentration will vary depending on overall RNA yield, see table below (also in the adapter annealing section):

|Quantity of starting material|Adapter stock concentration|Adapter concentration in ligation reaction|
|----|----|-----|
|100 – 250 ng|140 nM| 10 nM|
|251 – 500 ng|350 nM|25 nM|
|501 – 2000 ng|700 nM|50 nM|
|2001 – 4000 ng|1400 nM|100 nM|

For Puritz and Lotterhos 2017, we used 4000 ng starting RNA, but because of difficulties assessing and quantifying molluscan RNA, we chose to use a 700 nM working stock with a final reaction concentration of 50 nM.

#### This will be where we insert the custom adapters with restriction enzyme sites

1. Make the adapter ligation **master mix** on ice (multiple volumes by number of samples):

|Component| Volume needed for 1 reaction (1/2 reactions from kit protocol), including 10% excess|
|---------|--------------------|
|Water|8.8 μl|
|5X KAPA Ligation Buffer| 7.7 μl|
|KAPA T4 DNA Ligase|2.75 μl|

2. On ice, set up the adapter ligation **reactions** as follows, _note, if you are using more than one adapter, make sure to add the correct one to each sample_:

|Component|Volume|
|---------|------|
|Beads with A-tailed DNA| 15 μl |
|Adapter Ligation Master Mix| 17.5 μl |
|**Adapters***| 2.5 μl|
|**Total Volume**| **35 μl**|


3. Mix thoroughly by pipetting up and down several times to resuspend the beads
4. Incubate the plate/tube at 20 °C for 30 min (room temperature), if the samples can be placed on an orbital shaker at 200rpm this is ideal
5. Proceed immediately to **1st Post-Ligation Cleanup**

### Post-Ligation Cleanup

1. Bring PEG/NaCl to room temperature by taking out of the 4 degree ~30 minutes before use
2. Perform a 1X bead cleanup by adding 35 μl of PEG/NaCl to each ligated sample (that already contain beads)
3. Thoroughly resuspend the beads by pipetting up and down multiple times
4. Incubate the plate/tubes at room temperature for 15 min to allow the DNA to bind to the beads, if the samples can be placed on an orbital shaker at 200rpm this is ideal
5. Place the plate/tubes on a magnet to capture the beads. Incubate until the liquid is clear
6. Carefully remove and discard 65 μl of supernatant
7. Keeping the plate/tubes on the magnet, add 200 μl of freshly made 80% ethanol
8. Incubate the plate/tube at room temperature for ≥30 sec
9. Carefully remove and discard the ethanol
10. Keeping the plate/tube on the magnet, add 200 μl of 80% ethanol
11. Incubate the plate/tube at room temperature for ≥30 sec
12. Carefully remove and discard the ethanol. Try to remove all residual ethanol without disturbing the beads
13. Dry the beads at room temperature, until all of the ethanol has evaporated. **Caution: over-drying the beads may result in dramatic yield loss**
14. Remove the plate/tubes from the magnet
15. Thoroughly resuspend the beads in 25 μl of 10 mM Tris-HCl (pH 8.0)
16. Incubate the plate/tubes at room temperature for 5 min to allow the DNA to elute off the beads, if the samples can be placed on an orbital shaker at 200rpm this is ideal

---

### Safe Stopping Point
The solution with resuspended beads can be stored at 4 °C for up to 24 hours. Do not freeze the beads, as this can result in dramatic loss of DNA. When ready, proceed to **2nd Post-Ligation Cleanup**.

---

### 2nd Post-Ligation Cleanup

1. Bring PEG/NaCl to room temperature by taking out of the 4 degree ~30 minutes before use
2. Perform a 1X bead cleanup by adding 25 μl of PEG/NaCl to each ligated sample (that already contain beads)
3. Thoroughly resuspend the beads by pipetting up and down multiple times
4. Incubate the plate/tube at room temperature for 15 min to allow the DNA to bind to the beads,  if the samples can be placed on an orbital shaker at 200rpm this is ideal
5. Place the plate/tube on a magnet to capture the beads. Incubate until the liquid is clear
6. Carefully remove and discard 45 μl of supernatant
7. Keeping the plate/tube on the magnet, add 200 μl of 80% ethanol
8. Incubate the plate/tube at room temperature for ≥30 sec
9. Carefully remove and discard the ethanol
10. Keeping the plate/tube on the magnet, add 200 μl of 80% ethanol
11. Incubate the plate/tube at room temperature for ≥30 sec
12. Carefully remove and discard the ethanol. Try to remove all residual ethanol without disturbing the beads
13. Dry the beads at room temperature, until all of the ethanol has evaporated. **Caution: over-drying the beads may result in dramatic yield loss**
14. Remove the plate/tube from the magnet
15. Thoroughly resuspend the beads in 11.25 μl of 10 mM Tris-HCl (pH 8.0)
16. Incubate the plate/tube at room temperature for 5 min to allow the DNA to elute off the beads,  if the samples can be placed on an orbital shaker at 200rpm this is ideal
17. Place the plate/tube on a magnet to capture the beads. Incubate until the liquid is clear.
18. Transfer 10 μl of the clear supernatant to a new plate/tube and proceed to *Library Amplication*
---

### SAFE STOPPING POINT
The purified, adapter-ligated library DNA may be stored at 4 °C for up to 1 week, or frozen at -20 °C for up to 1 month. When ready, proceed to **Library Amplification**.

---
### Library Amplificiation

1. Make the library amplification **master mix** on ice, _note, if samples are being multiplexed and have different primers, do not make a master mix. If you are multiplexing, you can use the PCR primers outlined in the Genomic Library Prep section_:

|Component| Volume needed for 1 reaction (1/2 reactions from kit protocol), including 10% excess|
|---------|--------------------|
|2X KAPA HiFi HotStart ReadyMix|13.75 μl|
|10X KAPA Library Amplication Primer Mix|2.75 μl|

2. If multiplexing samples, add 2X KAPA HiFi HotStart ReadyMix and 10uM primers individually in volumes as stated in above table into new PCR tubes for each sample, and add 10μl of the cleaned ligated cDNA samples
3. If using a master mix, combine 15μl of the library amplification master mix and 10μl of the cleaned ligated cDNA samples
5. Mix well by pipetting up and down several times
6. Amplify the library using the following thermal cycling protocol:

|Step|Temp|Duration|Cycles|
|----|----|--------|------|
|Initial denaturation|98 °C|45 sec|1|
|Denaturation|98 °C|15 sec|12|
|Annealing*|60 °C|30 sec|12|
|Extension|72 °C|30 sec|12|
|Final Extension|72 °C|5 min|1|
|Hold|10 °C | ∞|1|


7. Place the plate/tube on ice and proceed to **Library Amplification Cleanup**

### Library Amplification Cleanup

1. Bring KAPA Pure Beads to room temperature by taking out of the 4 degree ~30 minutes before use and swirl to mix
2. Perform a 1X bead cleanup by adding 25 μl of KAPA Pure Beads to each sample after amplification
3. Thoroughly resuspend the beads by pipetting up and down multiple times
4. Incubate the plate/tube at room temperature for 15 min to allow the DNA to bind to the beads,  if the samples can be placed on an orbital shaker at 200rpm this is ideal
5. Place the plate/tube on a magnet to capture the beads. Incubate until the liquid is clear
6. Carefully remove and discard 45 μl of supernatant
7. Keeping the plate/tube on the magnet, add 200 μl of 80% ethanol
8. Incubate the plate/tube at room temperature for ≥30 sec
9. Carefully remove and discard the ethanol
10. Keeping the plate/tube on the magnet, add 200 μl of 80% ethanol
11. Incubate the plate/tube at room temperature for ≥30 sec
12. Carefully remove and discard the ethanol. Try to remove all residual ethanol without disturbing the beads
13. Dry the beads at room temperature, until all of the ethanol has evaporated. **Caution: over-drying the beads may result in dramatic yield loss**
14. Remove the plate/tube from the magnet
15. Thoroughly resuspend the dried beads in 22 μl of 10 mM Tris-HCl (pH 8.0)
16. Incubate the plate/tube at room temperature for 5 min to allow the DNA to elute off the beads, if the samples can be placed on an orbital shaker at 200rpm this is ideal
17. Place the plate/tube on a magnet to capture the beads. Incubate until the liquid is clear
18. Transfer 20 μl of the clear supernatant to a new plate/tubes.

## QC libraries

#### Use the [Broad Range Qubit Assay](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/Invitrogen-Qubit-Assay-Protocol.md) to get cDNA concentrations

#### Use the [D5000](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/D500-GenomicDNA-Tapestation-Protocol.md) or [D1000](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/D1000_Tape_Protocol.md) TapeStation Assays to assess quality and size of libraries

Example Library dones with this prep:
![](https://raw.githubusercontent.com/meschedl/MES_Puritz_Lab_Notebook/master/images/B10T24J03cDNA.png)
