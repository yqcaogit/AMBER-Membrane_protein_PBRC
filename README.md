# AMBER-Membrane_protein_PBRC
Tutorial on the setup of the Purple Bacteria Reaction Center (PBRC, 3i4d) membrane protein with charmm-gui
(Note: remember the JOB ID, you can redo from any step with Job Retriever)

charmm-gui membrane-builder website:https://www.charmm-gui.org/?doc=input/membrane.bilayer

a) PDB input

Input "3i4d" and click "Next Step"
![Alt text](/figures/001.png?raw=true "input")

b) PDB info

We only click three protein peptide chains (PDB ID "A", "B", "C") 
![Alt text](/figures/002.png?raw=true "three chains")

Set the system PH value to 7.4 (Spectroscopic and kinetic studies of PBRC often use buffers around pH 7.5 to mimic natural conditions while ensuring protein stability.)
Regarding the protonation state, according to the PH value we use, Charmm-gui can suggest the protonation state for us. We can also use Propka or MCCE to check the protonation state.
![Alt text](/figures/003.png?raw=true "PH and protonation")



c) STEP 1

As for the Orientation Options, I recommend 'Run PPM 2.0' or 'Use PDB orientation'. These two can make reasonable structures. I start with ‘Align the First Principal Axis Along Z’, but the structure does not look very vertical to the membrane.

For the reaction center in purple bacteria, correct membrane orientation is essential because: 1)it ensures realistic lipid interactions in simulations. 2)Charge transfer and proton transfer processes are highly dependent on membrane alignment. 3)Asymmetric environments (periplasmic vs cytoplasmic) are preserved.
![Alt text](/figures/004.png?raw=true "Orientation")

This is the visualization plot of the oriented protein:
![Alt text](/figures/v1.png?raw=true "oriented protein")

d) STEP 2

In this step, we add a lipid bilayer to the system. We choose to use POPC for the membrane since Xuhui's previous study of Photosystem II used POPC.

To follow the Minimum Image Convention that the cutoff distance for nonbonded interactions must be less than half the shortest box dimension, and the x and y dimensions of the box cannot be too small. We need to choose an appropriate box length to satisfy the calculation efficiency and rationality。
![Alt text](/figures/005.png?raw=true "membrane")

This is the visualization plot of the membrane protein:
![Alt text](/figures/v2.png?raw=true "oriented protein")


e) STEP 3

In this step, we neutralize the system by adding ions. 
![Alt text](/figures/006.png?raw=true "ions")

f) STEP 4

In this step, charmm-gui will check the system (lipid penetration) automatically. We only need to click the "Next Step"
![Alt text](/figures/007.png?raw=true "penetration")

The membrain protein system built with Charmm-gui:
![Alt text](/figures/v3.png?raw=true "membrane protein")

g) STEP 5

In this step, charmm-gui can generate Equilibration and Dynamics Inputs for us
![Alt text](/figures/008.png?raw=true "make input")

![Alt text](/figures/009.png?raw=true "inputs")
