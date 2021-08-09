# One Fourth Reaction [KAPA HyperPrep DNA Library Prep Kit](https://sequencing.roche.com/en-us/products-solutions/by-category/library-preparation/dna-library-preparation/kapa-hyperprep.html) Protocol

**DNA should be sheared beforehand to the desired size. This prep has been used with 100ng input amount and 300-500bp size DNA**

### End Repair and A-tailing

- Determine _n_ number to be # of samples + 0.05% for error
- Thaw on ice, vortex and spin down ERAT Buffer and Enzyme mix
- Prepare end repair and a-tailing master mix on ice:
  - ERAT buffer 1.75μl * _n_ = Xul
  - ERAT enzyme 0.75μl * _n_ = Xul
- Make PCR strip tubes with 25ul of sheared DNA
- Add 2.5μl of ERAT master mix to each sample
- Vortex and spin down strip tubes
- Place samples in thermocyler HyperPrep ERAT program in JONP login (~ 1 hour)

### Adapter Ligation

- Thaw ligation buffer and enzyme on ice. Vortex the buffer and spin down. **do not vortex ligase enzyme**, invert to mix and spin down
- Prepared ligation master mix on ice:
  - ligation buffer 7.5μl * _n_ = Xμl
  - DNA ligase 2.5μl * _n_ = Xμl
  - nuclease free water 1.25μl * _n_ = Xμl
- Pipette mix and spin down master mix
- Add 11.25ul of the ligation master mix to each sample tube
- Add 1.25ul of the planned adapter to the appropriate sample (1-12 adapters, see [oligo datasheet](https://docs.google.com/spreadsheets/d/1K0JaTR9PWUAhTSiKEU6sEJeHmLmcyGW0Vrs57O5GRPs/edit))
- Pipette mix all samples with 10ul
- Incubate tubes on the orbital shaker for 1 hour at 200rpm

### 0.8X Cleanup

- Make fresh 80% EtOH (either 50mL or 5mL: 40ul 100% ethanol with 10mL nuclease free water or 4mL 100% ethanol and 1mL nuclease free water, depending on how many preps)
- Take KAPA Pure Beads out of fridge 30 min beforehand to warm to room temp
- After incubation at RT, add 22μl of KAPA pure beads to each sample and pipette up and down at least 10 times to mix beads careful to avoid bubbles
- Place tubes on shaker at room temp for 15 minutes
- Place tubes on magnet plate and remove supernatant from tubes when it was fully clear not disturbing the beads
- Add 200μl of 80% EtOH to each tube while still the magnet not disturbing the beads
- Remove supernatant from each tube on the magnet plate without disturbing the beads
- Add 200μl of 80% EtOH to each tube while still the magnet not disturbing the beads
- Remove ALL the supernatant from each tube on the magnet plate without disturbing the beads. Extra EtOH blobs should be removed with p20 pipette tips
- Resuspend beads in 6μl 10mM Tris HCl pH 8 and incubate tubes on shaker for 5 minutes at 200rpm
- Place tubes back onto the magnet stand and remove 5ul supernatant when clear to new labeled PCR strip tubes

### Library Amplification

- Determine if master mixes can be made for some samples (samples with the same index pairs), or if each sample needs individual additions
- **If multiple samples are getting the same index pairs, make a master mix on ice.** Vortex and spin down the KAPA HiFi Hot Start Ready Mix and the 20uM primers and keep on ice while working
  - 6.35μl HotStart Ready mix * # of samples with this index pair = Xul
  - 0.75μl 50X primer * # of samples with this index pair = Xul
  - 0.75μl 70X primer * # of samples with this index pair = Xul
- Make multiple mixes if necessary
- Vortex and spin down master mix when done
- For samples with a master mix, add 7.5ul master mix to the corresponding sample tubes
- **If all samples have different index pairs, add each component individually to each tube**
  - 6.25ul HotStart Ready Mix
  - 0.75ul 50X primer
  - 0.75ul 70X primer
- Vortex and spin down sample tubes
- Place tubes in the thermocycler in the Genomic PCR 6 program in the JonP Login

### Double 1X Cleanup

- After PCR, add 12.5μl of KAPA pure beads to each sample and pipette up and down at least 10 times to mix beads careful to avoid bubbles
- Place tubes on shaker at room temp for 15 minutes
- Place tubes on magnet plate and remove supernatant from tubes when it was fully clear not disturbing the beads
- Add 200μl of 80% EtOH to each tube while still the magnet not disturbing the beads
- Remove supernatant from each tube on the magnet plate without disturbing the beads
- Add 200μl of 80% EtOH to each tube while still the magnet not disturbing the beads
- Remove ALL the supernatant from each tube on the magnet plate without disturbing the beads. Extra EtOH blobs should be removed with p20 pipette tips
- Resuspend beads in 13μl 10mM Tris HCl pH 8 and incubate tubes on shaker for 5 minutes
- Place tubes back onto the magnet stand and remove 12.5ul supernatant when clear to new labeled PCR strip tubes
- Repeat cleanup: add 12.5μl of KAPA pure beads to each sample and pipette up and down at least 10 times to mix beads careful to avoid bubbles
- Place tubes on shaker at room temp for 15 minutes
- Place tubes on magnet plate and remove supernatant from tubes when it was fully clear not disturbing the beads
- Add 200μl of 80% EtOH to each tube while still the magnet not disturbing the beads
- Remove supernatant from each tube on the magnet plate without disturbing the beads
- Add 200μl of 80% EtOH to each tube while still the magnet not disturbing the beads
- Remove ALL the supernatant from each tube on the magnet plate without disturbing the beads. Extra EtOH blobs should be removed with p20 pipette tips
- Resuspend beads in 16μl 10mM Tris HCl pH 8 and incubate tubes on shaker for 5 minutes
- Place tubes back onto the magnet stand and remove 16ul supernatant when clear to new labeled PCR strip tubes


### QC

- Broad Range DNA [Qubit](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/Qubit-Assay-Protocol.md)
- [D1000](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/D1000_Tape_Protocol.md) or [D5000](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/D500-GenomicDNA-Tapestation-Protocol.md) TapeStation Assay
