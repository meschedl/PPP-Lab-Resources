# MinION Sequencing with the [Oxford Nanopore Ligation Sequencing Kit](https://store.nanoporetech.com/ligation-sequencing-kit.html) and the [Flow Cell Wash Kit](https://store.nanoporetech.com/flow-cell-wash-kit-r9.html)

### You will want to wash and re-load the MinION multiple times to generate enough sequencing. Previous attempts have had good sequencing success with loading library on 5 separate times, with a wash in between each. One load of library will last 9-12 hours on the sequencer before it should be replaced. Note that if you do want to replace the library a few times that you will be coming into the lab at late or strange hours to do so.

#### **FlowCell Diagram** (color not realistic)

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/minION.jpg)

## Starting the Experiment and Loading a Library

**Planning**
- Open minKNOW software on the sequencing computer
- Plug in minION
- Determine how much library to add to each sequencing run. The Nanopore protocol says 5-50 fmols of DNA is ideal. Use the [NEB calculator](https://nebiocalculator.neb.com/#!/dsdnaends) to convert from ng of DNA to fmols of DNA ends. Use the quantification from the end of the library prep for the concentration. Make a guesstimate off the last TapeStation report from that sample on what the size is. Sequencing done by the Puritz lab has use 20-22fmols of DNA as input for each loading and it has worked well. The total amount of DNA you can add each time is 12ul, so the amount of fmols you choose has to be at or below 12ul. Remember that you will need volume left in the libraries to load the MinION potentially multiple times

**Prepping Flowcell**
- Thaw sequencing buffer (SQB), loading beads (LB), flush tether (FLT), elution buffer (EB), and one new tube of flush buffer (FB) at room temp and then once thawed place on ice
- Vortex and spin down SQB, EB, and FB
- Pipette mix FLT
- Take out a fresh flow cell from fridge
- Remove test cell from the minION and plug in the new flow cell
- Click on the device on the minKNOW software and click "check flow cell"
- Slide open the priming port up to the left
- Make sure there isn't an air bubble in the priming port:
  - Take a p1000 and set it to 200µl
  - Spear (gently) the tip into the priming port completely vertical
  - Very carefully slowly turn the knob on the pipette (while in the locked position) to about 220µl
  - Watch the pipette tip to see a small volume (10-20µl) of liquid come back up into the tip
  - Quickly remove the tip without adding a bubble
- Prepare priming mix: add 30µl FLT to the new tube of FB. Pipette to mix
- Add 800µl of the priming mix to the priming port (keeping the SpotON port cover closed) with a vertical p1000 tip very slowly. Watch as carefully as possible to see if any bubbles show up
  - _most of the liquid at this point goes into the waste channel, but you can kinda of imagine it going through the channel, past the electrodes, over the sequencing array, and back around into the waste channels_
- Wait 5 minutes

**Prepping Library**
- Pipette mix LB with p200 set to ~150
  - _right before adding beads, mix again with it set to the right volume for extra thorough mixing_
- Prepare library in DNA lo bind tube:
    - Xul of library for determined fmol conentration
    - Xµl elution buffer up to 12ul total including the library
    - 37.5µl sequencing buffer
    - 25.5µl **just pipette mixed** loading beads
- After the 5 minutes open the SpotON port by flipping up
- Add another 200µl of priming mix with a p1000 tip to the **priming port**. **Make sure you do this very very slowly**
  - _at this step you can see a small bubble of priming mix come out of the SpotOn port every time you depress the pipette, it'll recede back down in the sequencing array as you pause when slowly depressing the pipette_
- Mix the prepared library with a wide bore p200 pipette

**Loading FlowCell and Starting Experiment**
- Using regular filter p200 pipette tip add 75µl library (all) to the **SpotON port** by dripping on the hole. Watch to see each drop recede down over the array before adding the next one
- Close SpotON port, putting the bung in the hole
- Close the priming port by swinging it back down
- Close the lid of the minION sequencer
- On the minKNOW software click New Experiment
- Name experiment
- Name sample
- Set sequencing kit to [the appropriate one](https://store.nanoporetech.com/ligation-sequencing-kit.html), no expansion packs for barcoding
- Set to high accuracy basecalling
- Save all data to new folder with name of your choice
- Don't change any other settings on the interface
- Press start!
- The program will give you an initial "mux scan" with how many pores are available for sequencing

**You can have the flowcell run sequencing for as long as you want. At about 9-12 hours after starting it at first, you will see a plateau in the speed of bases being read, and a decrease in pores actively reading. This is because the pores get clogged with DNA after a while. When you are not getting enough output per time, you can decide to do a nuclease wash of the flowcell and all on a fresh library. Not all the pores will come back put a big majority will and you will see an increase in sequencing output.**

**These images are example outputs from a sequencing run in the Puritz Lab. You can see the plateaus in the output graph, and then the uptick afterwards when the flowcell was cleaned and fresh library added. The other image is the "duty time plot" where you can see the decrease in pores sequencing "strand" vs various other states of non-sequencing.**

![](https://raw.githubusercontent.com/meschedl/PPP-Lab-Resources/master/images/Screen%20Shot%202021-08-13%20at%209.09.32%20AM.png)

![](https://raw.githubusercontent.com/meschedl/MES_Puritz_Lab_Notebook/master/images/dt.png)

## FlowCell Wash


- Thaw wash solution B at room temp ([from wash kit](https://store.nanoporetech.com/flow-cell-wash-kit-r9.html)), vortex, spin down, then place on ice
- Put wash solution A on ice
- When solution B is thawed, make wash mix in a DNA lo bind tube
  - 380µl wash solution B
  - 20µl wash solution A
- Pipette to mix (contains DNase)
- **Pause sequencing run on minKNOW software**
- Open lid and made sure priming and SpotON ports are still closed
- Remove all liquid from **waste port 1** (next to the priming port) with a p1000 pipette.  Pipette completely vertically from the opening. This will be a little over 1mL
- Open priming port
- Draw back liquid in priming port to remove bubbles:
  - Take a p1000 and set it to 200µl
  - Spear (gently) the tip into the priming port completely vertical
  - Very carefully slowly turn the knob on the pipette (while in the locked position) to about 220µl
  - Watch the pipette tip to see a small volume (10-20µl) of liquid come back up into the tip
  - Quickly removed the tip to avoid bubbles
- Add 400µl of the wash mix to the priming port slowly without adding a bubble
  - _at this step you can see the previous library come off the flowcell and get flushed into the waste channel because the white loading beads move through the channels_
- Close the priming port
- Wait 30 minutes for the nucleases to work
- **Then make sure that the priming port and the SpotON port are closed**
- Remove all the waste liquid from the waste channel using waste port 1 and a p1000 pipette. Again this should be about 1mL


### After you have done this wash you can load a library again by starting with the Prepping FlowCell section. Instead of starting a new experiment, after you close the flowcell lid, just press resume on the software. Sometimes it will not mux scan immediately, so you may have to wait a few minutes before it will scan again and show you the revived pores


**Note here about some issues with reloading libraries many times. One time during a reload library there seemed to be a clog in the flow cell somewhere. This means that when adding things, bubbles start forming or the liquid inside the flowcell doesn't go to the right place. This does not necessarily mean that the sequencing is over and the flowcell is done-for. Here are notes on how this issue was resolved when it has happened previously:**

During the prepping library step:

- Adding 800µl priming mix went fine, the problem occurred when the SpotON port was opened
- When adding 200µl of priming mix to the priming port when the SpotON port was open, it did not seem to go down into the sequencing array: I immediately noticed that the small bubble of liquid that usually pushes out the SpotON port when adding in this step would not recede back down into the array, it would just stay as a bubble on the top
- I stopped adding about 20µl in, and put the rest of the priming mix back into the tube
- At this point I didn't know exactly what to do. there are recommendations on the Oxford Nanopore community forum for what to do if your library won't go down the SpotON port, which seemed like a similar issue so I at first tried to follow those troubleshooting recommendations:
- I removed all the waste from the waste channel via waste port 1 with both ports closed, then I flushed it with 1mL of nuclease free water and removed that as well. This did nothing
- I added about 20µl of priming mix to the top of the SpotON port, it stayed there, then I stuck a p1000 set at 200µl in the priming port and drew back from there and watched the bubble go down from the SpotON port. I tried this twice and it still didn't release whatever blockage
- Finally with recommendations from [Jon](https://github.com/jpuritz) I added the 200µl of priming mix to the priming port regardless of the bubble. A large bubble formed over the SpotON port but I sucked up whatever was there hoping that some went down. I then mixed then added the library to the SpotON port, as expected it did not go down. I then drew back from the priming port to get it to go into the flow cell. I could see the loading beads go back up the channel towards the electrodes, but it also looked like some of it got over the sequencing array.
- I closed it and resumed the run at this point and it came back with 886 pores!

After this the flowcell was able to be washed and re-loaded another time. When washing the next time a bubble came out of the waste chamber and after that there were no issues.
