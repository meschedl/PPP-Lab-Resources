# [EpiGentek MethylFlash Global DNA Methylation (5-mC) ELISA Easy Kit (Colormetric)](https://www.epigentek.com/catalog/methylflash-global-dna-methylation-mc-elisa-easy-kit-colorimetric-p-5370.html) 48 Assay Protocol



#### Notes and info for samples

- Each sample should be run in duplicate: so you only have room in the kit for 16 samples (there are 7 standards run in duplicate too)
- Ideal input amount is 100ng
- **Input amount of DNA volume is 5ul**


### Sample Prep

- Make a plate layout for where your samples will go on the plate
- Thaw DNA samples on ice
- Vortex and spin down DNA
- Make 1 dilution tube per sample **with the amount of DNA you need for both reactions**
- Add the volume of DNA for 2 reactions to each tube
- Add the volume of 10mM tris HCL to 10ul for each tube
- Vortex and spin down each dilution tube and keep on ice until beginning the assay

### Standards and Kit Prep

- Start the incubator genie to 37 degrees C
- Take all components out of the fridge, freezer, and kit box. Let all come to room temp
- **Make sure the concentrated wash buffer comes to room temp. It can form precipitates. If it is not warming, put in the incubator at 37 until there are no precipitates**
- Make diluted wash buffer:
  - 117mL of Type I DI water
  - 13mL of 10X wash buffer
- Swirl to mix
- If needed: Check wash buffer pH by using the pH meter: Calibrate, and buffer should be between 7.2-7.5
- Vortexed and spun down positive (PC) and negative control (NC) (kit provided)
- Make diluted positive control (DPC)
  - 9ul of NC
  - 1ul of PC
  - Vortex and spin down
- Make prep tubes for standards in same way as for samples: each sample would get 1 tube with the volume for 2 assays
- Add 5ul of NC to NC prep tube (volume of standards to add to plate is 2ul only -- this is based off using 100ng)
- 0.1% standard
  - 1ul DPC
  - 9ul NC
- 0.2% standard
  - 1ul DPC
  - 4ul NC
- 0.5% standard
  - 3ul DPC
  - 3ul NC
- 1% standard
  - 1ul PC
  - 9ul NC
- 2% standard
  - 1ul PC
  - 4ul NC
- 5% standard
  - 3ul PC
  - 3ul NC
- Vortex and spin down all tubes and kept on ice

### Assay

- Make sure you have a map of where the standards and samples go in front of you
- Vortex and spin down binding solution (BS)
- Add 100ul BS to each NC well
- Add 2ul of NC to each NC well, pipetting up and down a few times
- Add 100ul BS to each standard well, 2 at a time
- Add 2ul of appropriate standard solution, 2 at a time, pipetting up and down a few times (do each standard at a time, then go to the BS for the next standard)
- Add 100ul of BS to each sample well, 2 at a time
- Added 5ul of each sample to their wells, 2 at a time, pipetting up and down a few times (do each sample at a time, then go to the BS for the next sample)
- Once finished, rock the plate back and forth to make sure the bottom of the wells were covered in liquid and shake it a little gently while the bottom of the plate is against the table
- Cover the plate with the same seal it came with
- Place the plate in the incubator genie for 1 hour at 37 degrees C
- With 10 minutes left in the incubation, make the 5mc Detection Complex Solution:
  - 2.4mL diluted wash buffer
  - 2.4ul mc-antibody
  - Vortex and spin down
  - 2.4ul signal indicator
  - 1.2ul enhancer solution
  - Vortex and spin down again
- Remove the plate from the incubator after 60min
- Pipette out the BS into waste basin
- Make a basin with diluted wash buffer
- Wash each well 3 times with 150ul of diluted wash buffer:
  - Use the multichannel by column
  - Pipette in and then out wash buffer one column at a time
- After the last wash, go back through and try to suck out any remaining volume
- You can also try tapping the plate over a paper towel
- Add 50ul of the 5-mc Detection Complex Solution to each well
- Cover the plate with the same seal and leave at RT on the bench for 50 minutes
- After the incubation, remove the solution in each well by pipetting
- Wash each well 5 times with 150ul diluted wash buffer:
  - Use the multichannel by column
  - Pipette in and then out wash buffer one column at a time
- After the last wash, go back through and try to suck out any remaining volume
- You can also try tapping the plate over a paper towel
- Use a small basin for the developing solution:
  - Use the multichannel to add 100ul of the developing solution to each well **by column** so that each replicate got solution at the same time
- Gently shake the plate while the plate is touching the bench
- Watch the color change in the wells for up to 5 minutes: it's ready when the 5% standards are a strong aqua blue
- Use a small basin for the stop solution:
  - Use the multichannel to add 100ul of the stop solution to each well **by column** so that each replicate got solution at the same time
- Gently shake the plate while the plate is touching the bench
- Wait 1-2 minutes, all the wells should turn from blue to yellow when adding the SS pretty much immediately
- Within 15 minutes you should read the plate on the plate reader at 450nm absorbance

Save the readings as an excel file and analyze the data in R. [Example analysis script](https://github.com/meschedl/MESPutnam_Open_Lab_Notebook/blob/master/rscripts/MethylFlash_Analysis.md)
