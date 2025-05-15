# AMBER-Membrane_protein_PBRC
Tutorial on the setup of the Purple Bacteria Reaction Center (PBRC, 3i4d) membrane protein with charmm-gui

charmm-gui membrane-builder website:https://www.charmm-gui.org/?doc=input/membrane.bilayer

a) PDB input

Input "3i4d" and click "Next Step"

b) PDB info
fig002
We only click three protein peptide chains (PDB ID "A", "B", "C") 
fig003
Set the system PH value to 7.4 (Spectroscopic and kinetic studies of PBRC often use buffers around pH 7.5 to mimic natural conditions while ensuring protein stability.)

Regarding the protonation state, according to the PH value we use, Charmm-gui can suggest the protonation state for us. We can also use Propka or MCCE to check the protonation state.

c) STEP 1

As for the Orientation Options, I recommend 'Run PPM 2.0' or 'OPM'. I start with ‘Align the First Principal Axis Along Z’, but the structure does not look very vertical to the membrane.

