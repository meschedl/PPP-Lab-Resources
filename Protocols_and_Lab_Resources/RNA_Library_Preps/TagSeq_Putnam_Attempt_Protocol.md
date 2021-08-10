# TagSeq Library Prep Protocol

### Warning: this protocol has not been able to yield sequencing ready libraries as of 2021-08-10. This is the attempted protocol

### Library prep follows almost exactly the protocol from UT Austin (where applicable), except stops before pooling. Adapter and template switching oligo sequences are from the original Lohman protocol. Index primers are the same as the WGBS primers (sequences [here](https://github.com/Putnam-Lab/Lab_Management/blob/master/Lab_Resourses/DNA_RNA-protocols/Indexes_and_Barcodes/UDI_Index_Primer_Pairs_for_Pico_WGBS.csv))

**Every step besides Qubit or TapeStation should be done on the RNA Bench**

**For information on how to dilute or prepare primers, see [this](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/Oligos-Anneal-Adapters.md)**

#### RNA Fragmentation and RT Primer Annealing

- Thaw RNA samples on ice
- Dilute or aliquot samples to 100ng-1ug total RNA in 10ul, either in a plate or tubes. **Each sample in a project must have the same starting RNA amount** (this prep has been attempted with either 125ng or 500ng starting RNA)
- To make up the difference to 10ul per sample, use ultra pure water
- Turn on themocycler and started program **95** (in PUTNAM TagSeq folder) so the themocycler warms up and the block is at 95 C (Program is: 95C hold, 95C 2.5min)
- Determine _n_ number: number of samples + 5% for error
- Prepare RNA fragmentation/RT master mix on ice(RFRT)
  - 1ul dntps (10uM) * _n_ = Xul
  - 2ul 0.1M DTT * _n_ = Xul
  - 4ul 5x FS buffer * _n_ = Xul
  - 1ul 3iLL-30TV (10uM) * _n_ = Xul
- Pipette mix and spin down RFRT
- Add 8ul RFRT to each strip tube with aliquoited RNA (total volume in tubes is 18ul)
- Pipette mix strip tubes and spin down
- Place strip tubes in warmed up thermocycler (in the 95 degree hold) and press enter on program
- Watch program for the 2.5 min
- Take tubes out at the 2.5 min mark and put on the ice bucket for at least 2 minutes

####  1st Strand cDNA Synthesis

- Make 1st strand master mix (FSMM) on ice
  - 1ul SiLL - SWMW (10uM) * _n_ = Xul
  - 1ul SmartScribe RT * _n_ = Xul
- Pipette mix and spin down FSMM, keep on ice
- Add 2ul FSMM to each strip tube from the previous step
- Pipette mix with 15ul and spin down strip tubes and keep on ice until going in the thermocycler
- Turn on themocycler and start 1st Strand cDNA program, once the block gets to 42 degrees (a hold), put the strip tubes in the machine and press enter (Program is: 42 degrees C hold, 42 degrees C 60 min, 65 degrees C 15 min, 4 degree hold)

#### 0.9X Bead Cleanup 1

- Take out KAPA pure beads 1 hour before use, stored in drawer for warm up
- Make fresh 80% ethanol
- Spin down tubes out of the thermocycler
- Add 30ul ultra pure water to each sample (total vol now 50ul)
- Add 45ul KAPA pure beads to each tube, pipette mixing 10 times for each tube
- Place tubes on the shaker for 15 min at 200rpm shaking
- After, place tubes on the magnet stand and wait until the liquid is clear
- Remove 90ul of the clear supernatant from each tube
- Add 100ul of fresh 80% ethanol to each tube
- Remove 100ul of the clear supernatant from each tube
- Add 100ul of fresh 80% ethanol to each tube
- Remove 100ul of the clear supernatant from each tube
- Remove any remaining liquid with a p20
- Let "dry" for 3 min max
- Resuspend beads in 15ul ultra pure water
- Incubate tubes on the shaker for 5 minutes 2000rpm
- Place on magnet and let solution go clear
- Remove 10ul in to strip tubes for continuing lib prep "c"
- Remove 5ul into strip tubes for "save S1"
- This is a safe stopping point where the C tubes can be frozen for the next day

#### cDNA Amplification

- Make cDNA master mix (CDMM) on ice :
  - 6ul ultra pure H20 * _n_ = Xul
  - 0.5ul 10uM dntps * _n_ = Xul
  - 2ul 10X PCR buffer * _n_ = Xul
  - 0.5ul 5iLL (10uM) * _n_ = Xul
  - 0.5ul 3iLL-30TV (10uM) * _n_ = Xul
  - 0.5ul Klentaq * _n_ = Xul
- Mix by pipetting, spun down, and kept on ice
- Add 10ul CDMM to the "c" 1st strand strip tubes
- Pipette mix and spin down
- Place in thermocycler cDNA AMP program (**either the 18 cycle or 10 cycle, depending on input RNA amount. For less than 150ng RNA use 18 cycle, for more use 10 cycle**) (Program is : 94 degrees C 1 min, _94 degrees C 1 min, 63 degrees C 2 min, 72 degrees C 2 min_, 4 degrees C hold. Italics are cycled 18 times)

#### 0.9X Bead Cleanup 2

- Take out KAPA pure beads 1 hour before use, stored in drawer for warm up
- Make fresh 80% ethanol
- Spin down tubes out of the thermocycler
- Add 30ul ultra pure water to each sample (total vol now 50ul)
- Add 45ul KAPA pure beads to each tube, pipette mixing 10 times for each tube
- Place tubes on the shaker for 15 min at 200rpm shaking
- After, place tubes on the magnet stand and wait until the liquid is clear
- Remov 90ul of the clear supernatant from each tube
- Add 100ul of fresh 80% ethanol to each tube
- Remove 100ul of the clear supernatant from each tube
- Add 100ul of fresh 80% ethanol to each tube
- Remove 100ul of the clear supernatant from each tube
- Remove any remaining liquid with a p20
- Let "dry" for 3 min max
- Resuspend beads in 22ul ultra pure water
- Incubate tubes on the shaker for 5 minutes 2000rpm
- Place on magnet and let solution go clear
- Remove 10ul in to strip tubes for continuing lib prep "c"
- Remove 10ul into strip tubes for "save S2"
- Froze save set of strip tubes at -20
- Kept "c" strip tubes on ice for continuing

#### Index PCR Amplification

- Make index master mix (IMM) on ice:
  - 12.65ul ultra pure water * _n_ = Xul
  - 0.75ul 10uM dntps * _n_ = Xul
  - 3ul 10X PCR buffer * _n_ = Xul
  - 0.6ul Klentaq * _n_ = Xul
- Pipette mix and keep on ice
- Add 17.5ul of IMM to each continue tube from the step above
- Make sure you have planned the indexes (UDI 1-60) for your samples
- Thaw all indexes on ice, vortex, and spin down
- Add 3ul of the appropraite planned 3.9uM index to each C continue tube
- Pipette mix C tubes and spun down
- Put in thermocycler idex PCR program ( 95 degrees C 5 min, _95 degrees C 40 sec, 63 degrees C 2 min, 72 degrees C 2 min_, 4 degree hold. Italics are cycled 4 times)

#### 0.9X Bead Cleanup 3

- Take out KAPA pure beads 1 hour before use, stored in drawer for warm up
- Make fresh 80% ethanol
- Spin down tubes out of the thermocycler
- Add 27ul KAPA pure beads to each tube, pipette mixing 10 times for each tube
- Place tubes on the shaker for 15 min at 200rpm shaking
- After, place tubes on the magnet stand and wait until the liquid is clear
- Remove 50ul of the clear supernatant from each tube
- Add 100ul of fresh 80% ethanol to each tube
- Remove 100ul of the clear supernatant from each tube
- Add 100ul of fresh 80% ethanol to each tube
- Remove 100ul of the clear supernatant from each tube
- Remove any remaining liquid with a p20
- Let "dry" for 3 min max
- Resuspend beads in 28ul ultra pure water
- Incubate tubes on the shaker for 5 minutes 2000rpm
- Place tubes on magnet and let solution go clear
- Remove 25ul in to final library labeled strip tubes and kept on ice for QC

## QC

**High Sensitivity DNA Qubit**
- Follow [Qubit Assay Protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/Qubit-Assay-Protocol.md)

**DNA TapeStation D5000**
- Follow [D5000 Protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/D500-GenomicDNA-Tapestation-Protocol.md)
