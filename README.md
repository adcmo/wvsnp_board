# wvsnp_board

What is it?

This is the official board schematic, files, BOM and manufacturer files for the WVSNP Reduced board.

This is the Schematic and PCB layout (including gerber files) for the WVSNP Reduced Carrier Board 
and supporting components.

License and Copyright

This is the official repository of WVSNP Project. All code, SW and Hardware contributed here is 
subject to NDA and agreements you have with the WVSNP Project and ASU.

Quick Start Guide:

1- Download most recent stable build of Kicad at http://kicad-pcb.org/download/

2- Get a copy of the repository: - Using Command Prompt (Git Bash) git clone 
   https://github.com/adcmo/wvsnp_board/wvsnp_board.git
   - Using the GitHub page While logged in to GitHub, there are URLs available 
    in the sidebar: HTTPS clone URL - Using GitHub's GUI to clone repo.

3- Once repo is copied open Kicad - Chose File -> Open Project or CTRL+o - 
   Select "wvsnp_reduced_board.pro" file

   This will open the entire project with all the files necessary to see and 
   edit the schematic and PCB layout. 
   
4- Making Changes to schematic - Double click on "wvsnp_reduced_board.sch". 
   This will open the schematic - Make any necessary changes (add/removing 
   components, adding wires, etc) - If any components were added, ensure values 
   are properly filled (see any kicad tutorials) - Once happy with your changes, 
   save it and click the "NET" icon in the tool bar and follow prompts. This step 
   ensures components are populated in PCB side of things. - Run the CvPCB tool 
   to assign footprints for your components and save changes

5- Making changes to PCB file - Double click on "wvsnp_reduced_board.kicad_pcb" 
   - If components were added, click on "NET" on tool bar and click "Read Current 
     Netlist" This should add all the components you added to the schematic assuming 
     you have footprints available. If you don't have a footprint, look up tutorials 
     on how to create footprints. NOTE: If you assigned an existing footprint and it 
     doesn't populate, check to see if there are warnings after reading the netlist.

   - Once you finished routing all traces and placing all components, save it and run 
     "design rules check" (lady bug on tool bar).
     NOTE: Ensure that the place you are planning to have the boards manufactured 
     support your design rules. Set the design rules before making any changes.

   - Fix any issues that the checker points out. 
   - Save your changes and click "Plot" on toolbar (looks like a printer). Here you'll 
     generate your Gerbers. If you are unsure on what you'd like to add on the Gerbers, 
     look up toturials for generating Gerber files in Kicad. 
     
   - To view the board in 3D, click View -> 3D viewer. 
   
BOM

The Revision_BOM is part of the Repo (Excel file). To generate a BOM open the schematic 
portion and click "BOM." This will generate a csv file with the components. As of right 
now, we're still in the process of finding a good plugin for the BOM portion. The part 
numbers are manually added by looking at your preferred distributor.

Commiting Changes

Follow the same procedures as you would for any files. If using Git Bash, check which 
files have been changed with "git status" or if using GUI, see which files are showing 
in the change window.

Submitting Files for Fabrication

The zipped folder "Fab Files" have everything you need to send it for fabrication. 
Just submit the compressed folder and the shops know what to do with it. If you made 
changes, you'll need to generate new Gerber files and submit those. If you missed any 
important Gerbers (edge cuts for example) the shops will generally ask you for them.