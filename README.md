# scaffoldg
 
A layout manager for directed graphs that decomposes the graph into a set of configurable modules and an embedded grid.
A suite of functions and methods to improve graph legibility and customize layout parameters.

## Render steps
1. Decompose graph into modules
2. Initialize grid with indefinite points
3. Generate configuration object for each module
4. Generate configuration object for graph
  * width, height, etc
5. Calculate position and style for module content
6. Allow user to interface with graph content and grid

## Ideas

In order to render graph content, additional information is required beyond the content of the nodes and links. A configuration object with parameters to define dimensions/render/styling will help make explicit the additional metadata to enable proper rendering. It should also allow for the user to lock positioning on graph content and still run layout process.

Configuration object parameters will define:
* root content
* terminal content
* main axis
* bounds
* padding, margin
* node rendering
* link rendering
  * points to use for path
* ordering of content

Grid anchors:
* top left
* top right
* center
* bottom left
* bottom right

Module link typing:
* root single
* root fork
* root join
* single
* terminal fork
* terminal join
* terminal single

Sibling content will have configuration information to dictate how to order and criteria to generate rows.
