# [Zymo RRBS Library Prep Kit](https://www.zymoresearch.com/products/zymo-seq-rrbs-library-kit) Protocol (Reduced Representation Bisulfite Sequencing)


#### This library prep has only been done with _Montipora_ and _Pocillopora_ Corals. 300ng starting DNA was used

#### It is easiest to do this prep over two days

**Steps**
1. MspI Digestion
2. Adapter Ligation
3. DCC Cleanup
4. Bisulfite Conversion
5. DCC Bisulfite Cleanup
6. Index Primer Amplification
7. Bead Cleanup
8. QC


## MspI Digestion
- Thaw DNA on ice, vortex and spin down
- Aliquot 300ng DNA to new strip tubes
- Increase volume in each tube to 35.5ul with ultra pure water
- Determine _n_ number: number of samples + 5% excess
- Make master mix for digestion on ice:
  - 10X RRBS buffer 4µl * _n_ = Xµl
  - MspI 0.5µl * _n_ = Xµl
- Add 4.5µl of digestion master mix to each sample and pipette to mix and spin down
- Place in thermocycler RRBS digestion program:
 - 4 hours at 37 degrees C
 - 4 degree hold

## Adapter Ligation

- Make master mix for adapter ligation on ice:
  - 10X RRBS buffer 1µl * _n_ = Xµl
  - rATP 0.5µl * _n_ = Xµl
  - MspI 1µl * _n_ = Xµl
  - T4 DNA ligase 1µl * _n_ = Xµl
  - ultra pure water 6µl * _n_ = Xµl
- Pipette to mix master mix because ligase enzyme cannot be vortexed
- Add 9.5µl of master mix to each sample tube
- Add 0.5µl RRBS adapters to each tube (adding separately minimizes adapters ligating to themselves)
- Pipette to mix
- Put in thermocycler program RRBS adapters (best to do this overnight):
  - 21 degrees C 3 hours
  - 37 degrees C 1 hour
  - 20 degrees C 1 hour
  - 37 degrees C 1 hour
  - 20 degrees C 1 hour
  - 4 degree hold
- Once done (or next day) make gap filling master mix on ice:
  - Taq DNA Polymerase 0.5µl * _n_ = Xµl
  - 5-methylcytosine dNTP Mix 1.5µl * _n_ = Xµl
- Add 2µl of gap filling mix to each tube and pipette to mix
- Place in theremocyler program 74 degrees C (74 temp for 30 minutes)

## Cleanup with DCC

- Make a 1.5mL tube for each sample
- To each new 1.5mL tube, add a 7:1 ratio DNA binding buffer, or 364µl of DNA binding buffer
- Put elution buffer in thermomixer 56 degrees
- Add DNA sample (52µl) to the appropriate 1.5mL tube
- Make a spin column and collection tube per sample
- Vortex, spin down, and add to the appropriate column
- Centrifuge 12,000 rcf 30 seconds, discard flow through for kit waste hazardous waste
- Add 200µl M-wash buffer to each column
- Centrifuge 12,000 rcf 30 seconds, discard flow through for kit waste hazardous waste
- Adde 200µl M-wash buffer to each column
- Centrifuge 12,000 rcf **1 minute and 30 seconds**, discarded flow through for kit waste hazardous waste
- Transfer columns to new labeled 1.5mL tubes
- Add 20µl warmed elution buffer to each column directly
- Incubate 1 minute
- Centrifuge 12,000 rcf 30 seconds

### Bisulfite Conversion

- Transfer each sample to PCR tubes
- Add 130µl lightning conversion reagent to each sample in the PCR tubes
- Put PCR tubes in the thermocycler Pico bisulfite conversion program

### DCC Bisulfite Cleanup

- Make 6 spin column, one for each sample
- Add 600µl M-binging buffer to each spin columns
- Add 150µl of the BS reaction (all) to each individual tube
- Invert columns to mix
- Centrifuge columns at 12,000 rcf for 30 seconds and discarded flowthrough for kit waste hazardous waste
- Warm DNA elution buffer to 56 degrees C in a thermomixer
- Add 100µl M-Wash buffer to each column
- Centrifuge columns at 12,000 rcf for 30 seconds and discard flowthrough for kit waste hazardous waste
- Add 200µl L-desulfonation buffer to each column
- Let them sit for 15 minutes
- Centrifuge columns at 12,000 rcf for 30 seconds and discard flowthrough for kit waste hazardous waste
- Add 200µl M-wash buffer to each column
- Centrifuge columns at 12,000 rcf for 30 seconds and discard flowthrough for kit waste hazardous waste
- Add 200µl M-wash buffer to each column
- Centrifuge columns at 12,000 rcf for **1 minute and 30 seconds** and discard flowthrough for kit waste hazardous waste
- Add 24µl warmed (56C) DNA elution buffer to each column and let sit for 1 minute in new 1.5mL tubes to collect
- Centrifuge columns at 12,000 rcf for 30 seconds

### Index Primer Amplification

- Transfer 24µl of DNA to new PCR tubes on ice
- Add 25µl of Library Amp Master mix to each tube
- Make sure each sample has a planned primer pair (Putnam primer pairs [here](https://github.com/Putnam-Lab/Lab_Management/blob/master/Lab_Resourses/DNA_RNA-protocols/Indexes_and_Barcodes/UDI_Index_Primer_Pairs_for_Pico_WGBS.csv) or [here](https://github.com/Putnam-Lab/Lab_Management/blob/master/Lab_Resourses/DNA_RNA-protocols/Indexes_and_Barcodes/UDI_Index_Primer_Pairs_for_Pico_WGBS.xlsx))
- Thaw indexes (combined by number for i5 and i7 at 5uM) on ice, vortex and spin down
- Add 0.5µl of each planned primer set to the appropriate sample
- Vortex and spin down samles
- Place in theremocyler RRBS index amp program for 11 cycles:
  - 94 for 30 sec
  - **94 for 30 sec** (11)
  - **55 for 30 sec** (11)
  - **68 for 1 min** (11)
  - 68 for 5 min
  - 4 hold

## KAPA Pure Bead Cleanup
- Take KAPA Pure Beads out of the refrigerator ~30 minutes before use to get to room temperature. Swirl the bottle to mix the beads but don't vortex
- Make fresh 80% ethanol for the day, using 100% ethanol (in the flammable cabinet) and ultrapure water
- When beads are at room temp, add 50ul (equal volume) of beads to each strip tube. Pipette slowly because the bead solution is very viscous. Pipette mix the bead-sample mix at least 10 times until homogeneously brown
- Set up the rotating shaker on the Qubit bench and place the strip tubes on the shaker, rotating at 200rpm for 15 minutes
- Use the grey long 24-spot magnet on the Putnam bench
- At the 15 minutes on the shaker, place the tubes on the magnet rack and wait until the liquid goes clear and the beads have gone to the magnet
- Using a p200 pipette set to 95ul, carefully remove the clear supernatant from each tube without disturbing the beads and discard in a waste trough
- Add 200ul of 80% ethanol to each tube
- Remove the ethanol (200ul) from each tube carefully, without disturbing the beads, and discard the liquid in the waste trough
- Add another 200ul of 80% ethanol to each tube
- Remove the ethanol (200ul) from each tube carefully, without disturbing the beads, and discard the liquid in the waste trough
- Use a p20 set to 20ul to remove any residual liquid in each tube
- Let tubes air dry for ~1 more minute
- Take the tubes off the magnet
- Resuspend the beads in 16ul of DNA elution buffer: Pipette directly onto the bead patch over and over until the beads go into solution
- Place the tubes back on the shaker at 200rpm for 5 minutes
- After the 5 minutes place the tubes back on the magnet plate and wait until the liquid goes clear and the beads are to the magnet
- Make new strip tubes (final tubes) that are well labeled for your libraries (sample name, date, "lib" initials)
- Freeze at -20 degrees C if not doing QC on the same day, if QCing next, place on ice

## QC

- Use the [Qubit Protocol](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/Invitrogen-Qubit-Assay-Protocol.md) and the Broad Range assay to determine concentration of libraries
- Use the [D5000 TapeStation](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/D500-GenomicDNA-Tapestation-Protocol.md) to check size
