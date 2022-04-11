# D5_Details
This is a miscelaneous pack containg greebles, assemblies, and any other detailing stuff I've been using in my scenes.

## Credits
### Pipe
This geonode has been adapted from Amandeep's GeoPipes addon (https://amanbairwal.gumroad.com/l/GeoPipes). I've modifies it to accept object references instead of creating hex flanges. And I added the ability to specify an object for the pipe ends. If you just want some random pipes definitely check out his addon. The pipe insert will be created by default as completely white with no flanges. There is an issue with blender where inserts with materials/objects in the geo nodes do not deduplicate properly so you end up with many copies of the same materials. So assign a material, flange object, and endpoint object (included as separate inserts in this pack) then just duplicate the insert as many times as needed.

# D5_EE_Components
This is a project to create procedural GeoNodes implementations of common electrical engineering components. Currently there is only one insert design the DIP package chip but there are plans to create many more.

# D5_Glass
These inserts are details I created for some cyberpunk / virtual world renders. Hex Plate and Penta Plate are the main inserts but the cutters can be useful for creating effects similar to cut/etched crystal. The Diamond material is taken from a youtube tutorial by CG Vertex (https://www.youtube.com/watch?v=lEPZ1IUkoB4) The material uses a white noise texture to create an even dispersion of RG and B wavelengths across the IOR. It's called Diamond... because that's the IOR I used. The IOR is adjustable in the shader editor, obviously.

# D5_ProceduralDots
This is a group of inserts for detailing based on the dots generators. All 2d inserts have been given a z offset of 0.001 to help prevent z fighting. 


## Roadmap
Create a complex 3d grid capable of instancing custom geometry based on location within the cube.


## List of Generators


### 3d Dot Grid Simple
This generator creates a 3d lattice of dots. Similar to one of those LED cubes. Idea is using it for simulating holographics. Generator is listed as simple as it doesn't do instancing.


### Accumulated Line
Dot positions are calculated cumulatively with both a multiplier and a constant addition option for both translation and rotation. In the simplist form this can be used to create straight lines. It can also be used to create exponential offset between subsequent dots, simple arcs, and spiral patterns. Currently only works facing in the z+ direction.


### Anim Ascender (1,2, and 3)
Simple node group that creates a sphere that travels upward over time. 1 is just a sphere, 2 inculdes smaller spheres for it to move long (similar to landing lites), and 3 includes a line. Length and speed are adjustable.


### Arc
Group to create dots in an arc. Dots face upwards along the z axis


### CircleExplosion
Starts with a ring and projects lines of windows outward and inward. Effect is similar to a solar eclipse.


### Circle Hexagon Dot
This is an example of a single object with the circle explosion, concentric ngon, and grid modifiers all applied to the same object.


### Concentric
Concentric produces a series of rings with options for even spacing between the rings or random spacing.


### Concentric-ngon
Options are almost identical to the concentric circle generator, however a resample option has been added. Allowing modifying a low poly circle into an ngon with many dots along the edges.


### Cylinder
Creates dots along the surface of a cylinder. Dots face outwards along x and y axis


### Grid
Setting one or both dimensions to 1 can be used to make lines or single points. Otherwise will produce a brick of windows.


### Random Lines
Simulates lines of windows on something like an office building. Lines of a random length radiate from the center creating a pattern with solid top and bottom lines and a broken or jagged profile on the sides.


### TriColor
This insert creats a 3d line of dots (spheres or cubes) with different emission shaders for the first and last nodes. The effect is trying to emulate the nav buoys in Eve online entering and exiting space stations.
