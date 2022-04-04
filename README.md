### D5_ProceduralDots
This is a group of inserts for detailing based on the dots generators. All inserts have been given a z offset of 0.001 to help prevent z fighting. 

## List of Generators
### Random Lines
Simulates lines of windows on something like an office building. Lines of a random length radiate from the center creating a pattern with solid top and bottom lines and a broken or jagged profile on the sides.


### Concentric
Concentric produces a series of rings with options for even spacing between the rings or random spacing.


### Concentric-ngon
Options are almost identical to the concentric circle generator, however a resample option has been added. Allowing modifying a low poly circle into an ngon with many dots along the edges.


### CircleExplosion
Starts with a ring and projects lines of windows outward and inward. Effect is similar to a solar eclipse.


### Grid
Setting one or both dimensions to 1 can be used to make lines or single points. Otherwise will produce a brick of windows.


### Accumulated Line
Dot positions are calculated cumulatively with both a multiplier and a constant addition option for both translation and rotation. In the simplist form this can be used to create straight lines. It can also be used to create exponential offset between subsequent dots, simple arcs, and spiral patterns. Currently only works facing in the z+ direction.

## Composite Nodes
The nodes have been made stackable so multiple versions of the same modifier or different modifiers can be applied. If you're using a mesh with real geometry use the "ClearGeometry" node.

### Circle Hexagon Dot
This is an example of a single object with the circle explosion, concentric ngon, and grid modifiers all applied to the same object.
