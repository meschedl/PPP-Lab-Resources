# Long Read DNA Library Prep Protocol with the [Oxford Nanopore Ligation Sequencing Kit](https://store.nanoporetech.com/ligation-sequencing-kit.html) and the [NEB Companion Module for Oxford Nanopore Technologies Ligation Sequencing](https://www.neb.com/products/e7180-nebnext-companion-module-for-oxford-nanopore-technologies-ligation-sequencing#Product%20Information) for MinION Sequencing

#### This prep has been successful with 1.3ug total starting DNA. DNA quality should be very very high molecular weight: the majority of fragments over 60,000bp in length (as measured by Genomic TapeStation Assay)

#### Usually you won't be sequencing more than one sample on a MinION at once. You can do more than one library prep with the same sample to have enough library to re-load the MinION multiple times.

#### Use wide-bore pipette tips when working with HMW DNA. Avoid pipetting as much as possible the DNA and never vortex the DNA. You should also use "DNA lo-bind" tubes. Never freeze HMW DNA, keep in the fridge for storage.

#### Bead cleanups for HMW DNA are much more drawn out than regular ones. Long fragments take much more time to move (bind or un-bind to beads).

## DNA Repair and End-Prep

- Thaw DCS (DNA control sequence) from the Nanopore kit room temp and once it is thawed put the tube on ice
- Thaw FFPE DNA Repair Buffer, FFPE DNA Repair Mix, Ultra II End-prep reaction buffer, and Ultra II End-prep enzyme mix on ice. These are from the NEB kit
- Flick to mix reagents and spin down
- Determine _n_ number: how many library preps + 5% for error
- Prepare DNA for input: aliquot DNA into a strip tube with a wide bore tip and increase the volume to 47ul with nuclease free water
- Make master mix for DNA repair and end prep in ice (if you are doing only 1 library prep, don't make a master mix and add the components individually):
  - 1µl DNA CS x _n_ = Xul
  - 3.5µl FFPE DNA repair buffer x _n_ = Xul
  - 2µl FFPE DNA repair mix x _n_ = Xul
  - 3.5µl Ultra II end prep reaction buffer x _n_ = Xul
  - 3µl Ultra II end prep enzyme mix x _n_ = Xul
- Pipette to mix master mix
- Add 13µl of master mix to each strip tube
- Flick tubes to mix and spin down in the minifuge
- Place tubes in thermocycler JONP login Nanopore Incubation program:
  - 30min at 20 degrees C
  - 30min at 65 degrees C

## Bead Cleanup

- Take out KAPA Pure beads, swirl to resuspend, and let them come to room temp (~30 min before use)
- Make fresh 80% ethanol
- Take sample tubes out of the thermocyler and add 60µl beads to each tube (don't mix!)
- Flick tubes to mix and spin them down briefly on a minifuge
- Place tubes on the orbital shaker for 30 minutes at 300rpm to facilitate binding
- Place tubes on the magnet plate and wait 5 minutes
- Remove and save supernatant without disturbing the beads
- Gently adde 200µl 80% EtOH to the tubes
- Remove and discard wash supernatant
- Add 200µl 80% EtOH
- Remove and discarded wash supernatant
- Spin down tubes with minifuge and place back on magnet
- Remove any remaining supernatant
- Let beads dry maybe 30 seconds
- Resuspend pellet in 61µl nuclease-free water: flick and spin down, flick and spin down. **No pipette mixing**
- Incubate tubes at room temp on the orbital shaker at 300rpm for at least 60 minutes
- **Keep liquid with beads**
- To check, you can place the tubes back on the magnet to do a [Qubit Assay](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/Invitrogen-Qubit-Assay-Protocol.md) for concentration

**Adapter Ligation**

- Thaw AMX (Adapter Mix from Nanopore kit) and T4 DNA Ligase (NEB kit) on ice
- Thaw LNB (Ligation Buffer from Nanopore kit) at room temp, spin down, pipette to mix, then place on ice
- Thaw EB (Elution Buffer from Nanopore kit) at room temp, vortex, spin down and put on ice
- Thaw LFB (Long Fragment Buffer from Nanopore kit) at room temp, vortex, spin down and put on ice
- Make ligation and adapter master mix on ice (if you are doing only 1 library prep, don't make a master mix and add the components individually):
  - 25µl LNB x  _n_ = Xul
  - 10µl T4 DNA ligase x  _n_ = Xul
  - 5µl AMX x  _n_ = Xul
- Flick master mix tube to mix then spin down (do not vortex ligase)
- Add 40µl ligation and adapter mix to each tube with the DNA and the beads
- Flick to mix the tubes then spin down
- Incubate tubes on the orbital shaker at room temp for 30min at 300rpm

## Bead Cleanup

- Take out beads and let get to room temp
- After incubation, spin down tubes and add 40µl beads to each sample tube
- Flick tubes to mix then spin down
- Incubate tubes on shaker at room temp for 30min at 300rpm
- Place on magnet plate after incubation
- Wait 5 minutes
- Remove clear supernatant without disturbing beads and save just in case
- Take tubes off magnet and add 250µl LFB
- Flick tubes to mix and spin down
- Place tubes back on magnet
- Remove and save supernatant just in case
- Take tubes of magnet and add 250µl LFB
- Flick tubes to mix and spin down
- Place tubes back on magnet
- Remove and save supernatant
- Spin down tubes
- Remove any residual supernatant
- Remove tubes from magnet and add 15µl EB
- Flick tubes to mix then spin down
- Place tubes on the orbital shaker at 300rpm at room temp overnight
- Place in the fridge if storing before starting sequencing

**Use the Broad Range [Qubit Assay](https://github.com/meschedl/PPP-Lab-Resources/blob/master/Protocols_and_Lab_Resources/DNA_Quality_Control/Invitrogen-Qubit-Assay-Protocol.md) to check the concentration of your finished libraries**
