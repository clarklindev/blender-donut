Beginner Blender 4.0 Tutorial
# Blender Guru

## Part 01: fundamental user interface basics
- 80/20 rule -> 20% of blender features are used 80% of the time
- G -> grab -> then using middle mouse button to drag out in direction it sticks to X , Y or Z axis
- learn interface shortcuts

## Part 02: basic modelling
- learnt about making a donut shape but tweaking it so it doesnt look perfect using proportional editing and circle of influence

## Part 03: Modelling the Icing
- create icing by duplicating donut (SHIFT + D)
- delete bottom half of duplicate
- z-fighting 
- use solidify modifier to give icing thickness (offset should be changed to 1 so normals are facing out)
- thickness 0.025

#### wavey edges for icing
- to hide the shape of icing -> select solidify modifier -> uncheck edit mode (so it doesnt show the shape in edit mode) -> you should be able to see the vertices
- use proportional editing to drag down icing vertices randomly
- BUT... if you drag a vertex down, it doesnt follow the shape of the donut (its separate)
- FIX: snap vertices to donut underneath by turning on snapping: 3d viewport menu -> snapping (magnet icon) -> snap individual elements to "face project"

#### snapping type
1. increment (default which snaps to grid floor)
2. vertex 
3. edge
4. face
...
snap individual elements to 
1. face project
2. face nearest

- if the icing looks like its falling inside the donut its because there is not enough vertices
- FIX: add more geometry -> apply the subdivision surface modifier of icing
- now... pulling down a vertex will stick the icing to the donut BUT... it pulls from the hole side of the icing..BECAUSE circle of influence is so high that it reaches the other side of the donut
- FIX: hide the part of the mesh that we dont want to be influenced by proportional editing tool.
- select the inner vertices (select a vertex then alt + click on a edge) -> then CTRL + -> this increases the selection
- hide it H (hide) / show (ALT + H)
- now we can tweak the icing
- need to fix icing drip edge so its not 90 deg.
- FIX: add sub surface modifier (AFTER the solidify modifier)
- problem: the icing drips down but on the inner side it goes up, where it shouldnt
- FIX: solidify edge data -> add crease to inner part -> 1.0

#### create icing drip
- select 2 vertices -> drag down on z axis -> extend again

## Part 04: Sculpting
- fix the mesh icing vs donut where the icing vertices are in the donut (overlaps)
- FIX: we want the icing to wrap the donut
- this lesson (0-> 3min) we learn about modifier -> deform -> shrink wrap modifier 
- it needs a target -> what are we shrink wrapping (what is the mesh we are shrink wrapping) ie the donut -> eyedropper picker select the donut as target
- modifier stack order matters: 1. shrinkwrap, 2. solidify, 3. subdivision
- it corrects the vertices alignment: donut vs icing
- you can apply the shrinkwrap modifier...


## Part 05: Shading
## Part 06: Geometry Nodes
## Part 07: Geometry Nodes (Long Sprinkles)
## Part 08: Rendering!
## Part 09: Layout
## Part 10: Lighting
## Part 11: Compositing
## Part 12: Animation
## Part 13: Rendering
## Part 14: Finale!