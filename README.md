# Traffic_light_controller_Synthesis

## Aim:

Synthesize Traffic Light Controller design using Constraints and analyse area and Power reports.

## Tool Required:

Functional Simulation: Incisive Simulator (ncvlog, ncelab, ncsim)

Synthesis: Genus

### Step 1: Getting Started

Synthesis requires three files as follows,

◦ Liberty Files (.lib)

◦ Verilog/VHDL Files (.v or .vhdl or .vhd)

### Step 2 : Creating an SDC File

•	In your terminal type “gedit input_constraints.sdc” to create an SDC File if you do not have one.

### Step 3 : Performing Synthesis

The Liberty files are present in the library path,

• The Available technology nodes are 180nm ,90nm and 45nm.

• In the terminal, initialise the tools with the following commands if a new terminal is being used.

◦ csh

◦ source /cadence/install/cshrc

• The tool used for Synthesis is “Genus”. Hence, type “genus -gui” to open the tool.

• Genus Script file with .tcl file Extension commands are executed one by one to synthesize the netlist.

Synthesis RTL Schematic :
![Screenshot 2024-11-14 162129](https://github.com/user-attachments/assets/dde33772-41a8-4e74-9025-cd4c74d79d62)

Area report:
============================================================
  Generated by:           Genus(TM) Synthesis Solution 21.14-s082_1
  Generated on:           Nov 14 2024  05:49:05 am
  Module:                 TrafficLight
  Technology library:     slow 
  Operating conditions:   slow (balanced_tree)
  Wireload mode:          enclosed
  Area mode:              timing library
============================================================

  Instance   Module  Cell Count  Cell Area  Net Area   Total Area   Wireload  
------------------------------------------------------------------------------
TrafficLight                 89    892.615     0.000      892.615 <none> (D)  
  (D) = wireload is default in technology library
Power Report:
Instance: /TrafficLight
Power Unit: W
PDB Frames: /stim#0/frame#0
  -------------------------------------------------------------------------
    Category         Leakage     Internal    Switching        Total    Row%
  -------------------------------------------------------------------------
      memory     0.00000e+00  0.00000e+00  0.00000e+00  0.00000e+00   0.00%
    register     1.22163e-06  1.54232e-06  0.00000e+00  2.76395e-06  40.78%
       latch     7.32978e-07  6.70833e-07  0.00000e+00  1.40381e-06  20.71%
       logic     1.31800e-06  1.29241e-06  0.00000e+00  2.61041e-06  38.51%
        bbox     0.00000e+00  0.00000e+00  0.00000e+00  0.00000e+00   0.00%
       clock     0.00000e+00  0.00000e+00  0.00000e+00  0.00000e+00   0.00%
         pad     0.00000e+00  0.00000e+00  0.00000e+00  0.00000e+00   0.00%
          pm     0.00000e+00  0.00000e+00  0.00000e+00  0.00000e+00   0.00%
  -------------------------------------------------------------------------
    Subtotal     3.27261e-06  3.50556e-06  0.00000e+00  6.77817e-06 100.00%
  Percentage          48.28%       51.72%        0.00%      100.00% 100.00%
  -------------------------------------------------------------------------
Result:

The generic netlist of Traffic Light Controller has been created, and area, power reports have been tabulated and generated using Genus.
