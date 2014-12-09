# makepat

# THIS DOC IS CURRENTLY INCOMPLETE / EARLY ALPHA

A collection of autolisp scripts for creating real autocad .pat hatch patterns.

## History:
In 1998 I was contracted to create a ton of hatch patterns. At the time I was creating them manually with text editor and my HP calculator. I took a contract for some designs that were way to complex to do manually so I spent 2 weeks creating a set of scripts that in most cases does all the work and in the more complex cases makes the process MUCH less time consuming. I've never found any tool that can do what this does so finally getting around to sharing it.

## makepat.lsp Commands
* makepat
* fixangles
* scalepat (currently missing. to be found or recreated)

## Installation 
todo

## Usage Instructions
All vectors for the hatch pattern must be inside a 1x1 unit square. Lines extending outside the square may produce overlapping vectors in the pattern but can also be used for interesting effects.

Curves (Arcs and circles) must be approximated with lines. Polygons with many sides work well for this. 

Explode everything: All lines must be single lines. No multisegment line types of any kind will work.

fixangles: After designing the pattern you should run the fixangles script to force all vectors to have hatch pattern compatible angles. Usually this results in minor tweaking of the vector angles. Trim / fillet as needed to clean up but do not alter the angles. The start and end points are unimportant but the angles are critical. The main script makepat will also fix angles prior to creating the pattern so this step gives you a chance to clean things up and make any adjustments to the design that might be necessary after the angle adjustments.

makepat: Makepat is the main script that creates the hatch pattern. It will ask for a pattern name. This should follow the old 8.3 filename rules but do not include any extension (example: testpat). Then select all the lines inside the 1x1 square to be included in the pattern.  The pattern will be created and written to your default user folder (user Documents folder).

The pattern 'should' be immediatly usable by using its name in the hatch command.

You can make tweaks and recreate the pattern with the same name (caution! no warning on .pat file overwrite) Then test the updated pattern. 


