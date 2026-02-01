# Tree Tool

The infamous procedural Tree Tool. Generate fully customizable trees with trunks, branches, twigs, roots, and leaves.

<!-- TODO: Add hero screenshot showing a generated tree -->

## Overview

The Tree Tool generates procedural trees with extensive control over every component. Each part of the tree (trunk, branches, twigs, roots, leaves) can be independently configured with its own shape, size, and block types.

## Usage

* Position the tree origin where you want the base
* Configure each component in the tool options
* Preview updates in real-time
* Press **Enter** to place the tree

{% hint style="info" %}
You can also use branches as leaves by simply changing their blocks to leaf blocks - this creates a more organic, branchy canopy.
{% endhint %}

## Components

### Trunk

<!-- TODO: Add screenshot of trunk settings -->

The main vertical structure of the tree.

#### Trunk Settings

* `Length` [0-50]: Height of the trunk in blocks
* `Radius Begin` [0-10]: Thickness at the base
* `Radius End` [0-10]: Thickness at the top
* `Bend X / Y / Z` [-20 to 20]: Bending angles for each axis
* `End X Offset / End Z Offset` [-20 to 20]: Horizontal offset of the trunk top
* `Shape`: Cross-section shape of the trunk
  * **Circular**: Standard round trunk
  * **Multi-Lobed Foil**: Trunk with lobes (like a clover shape)
  * **Four Splines**: Custom spline-based shape
* `Lobe Count` [2-12]: Number of lobes (Multi-Lobed Foil only)
* `Twist Rotations` [-0.5 to 0.5]: Amount the trunk twists along its length

#### Trunk Blocks

* `Full Blocks`: Primary block type (e.g., Oak Log)
* `Stairs`: Stair variant for smooth transitions
* `Slabs`: Slab variant for detail
* `Walls`: Wall variant for thin sections

### Branches

<!-- TODO: Add screenshot of branch settings -->

Branches extend outward from the trunk.

#### Branch Settings

* `Per Segment` [1-10]: Number of branches per trunk segment
* `Climb Rate` [0-1]: How much branches angle upward
* `Length` [0-20]: Base length of branches
* `Length Variance` [0-10]: Random variation in length
* `Radius Begin / Radius End` [0-5]: Branch thickness at start and end
* `Length Falloff / Radius Falloff` [0-1]: How much length/radius decreases for higher branches
* `Y Direction` [-3 to 3]: Vertical direction bias
* `Bend X / Y / Z` [-10 to 10]: Bending angles

#### Branch Blocks

Configure separate block types for branches (Full, Stairs, Slabs, Walls).

### Twigs

<!-- TODO: Add screenshot of twig settings -->

Small extensions at the end of branches.

#### Twig Settings

* `Per Branch` [0-10]: Number of twigs per branch
* `Length` [0-10]: Twig length
* `Length Variance` [0-5]: Random length variation
* `Radius Begin / Radius End` [0-2]: Twig thickness
* `Bend X / Y / Z` [-10 to 10]: Twig bending

#### Twig Blocks

Configure separate block types for twigs.

### Roots

<!-- TODO: Add screenshot of root settings -->

Roots extend from the trunk base into the ground.

#### Root Settings

* `Number of Roots` [1-10]: How many roots to generate
* `Length` [0-20]: Root length
* `Length Variance` [0-10]: Random length variation
* `Radius Begin / Radius End` [0-5]: Root thickness
* `Y Direction` [-3 to 3]: Downward direction bias
* `Bend X / Y / Z` [-10 to 10]: Root bending

#### Root Blocks

Configure separate block types for roots.

### Leaves

<!-- TODO: Add screenshot of leaf settings -->

The foliage of the tree.

#### Leaf Type

* **Sphere**: Standard spherical leaf cluster
* **Super Sphere**: Sphere with adjustable exponent (can be more cubic or star-shaped)
* **Voxel**: Blocky, voxelized leaves
* **Palm**: Palm tree fronds

#### Leaf Settings (Sphere / Super Sphere / Voxel)

* `Radius X / Y / Z` [0.5-20]: Radius of the leaf volume on each axis
* `Unlock Radius`: Allow different values for each axis
* `Enable Radius Variance`: Add random variation to radius
* `Exponent` [0.5-20] (Super Sphere only): Shape exponent
  * Lower values: More star-like
  * Value of 2: Standard sphere
  * Higher values: More cube-like

#### Leaf Settings (Palm)

* `Number` [1-10]: Number of palm fronds
* `Leaf Length`: Length of each frond
* `Y Direction`: Vertical angle of fronds
* `Bend X / Y / Z`: Frond bending
* `Palm Depth` [0.1-5.0]: Thickness of the fronds

#### Leaf Noise Variation

Add procedural noise to break up the leaf shape:
* `Noise Type`: Type of noise pattern
* `Scale X / Y / Z`: Noise scale on each axis
* `Seed`: Random seed for the noise
* `Block Thresholds`: Control which blocks appear based on noise values

#### Leaf Rotation

* `Enable Center Rotation`: Rotate leaves toward the tree center
* `Rotation Toward Center` [0-1]: Amount of rotation

#### Leaf Blocks

Configure separate block types for leaves.

## Transform Settings

<!-- TODO: Add screenshot of transform settings -->

Global transformations applied to the entire tree.

* `Tree Scale` [0-3]: Overall scale multiplier
* `X Axis Rotation` [0-360]: Rotation around the X axis
* `Y Axis Rotation` [0-360]: Rotation around the Y axis
* `Z Axis Rotation` [0-360]: Rotation around the Z axis

## Segment Settings

<!-- TODO: Add screenshot of segment settings -->

Control trunk segmentation for branches.

* `Segments` [0-3]: Number of vertical segments
* `Offset Top` [0-1]: Branch offset at top of trunk
* `Offset Bottom` [0-1]: Branch offset at bottom of trunk

## Wind Settings

<!-- TODO: Add screenshot of wind settings -->

Simulate wind effects on the tree shape.

* `Direction` [0-360]: Wind direction in degrees
* `Power` [0-1]: Wind strength

## Feature Toggles

Enable or disable generation of each component:

* `Generate Roots`: Enable/disable root generation
* `Generate Branches`: Enable/disable branch generation
* `Generate Twigs`: Enable/disable twig generation
* `Generate Leaves`: Enable/disable leaf generation

## Block Style Options

For each component (trunk, branches, twigs, leaves, roots):

* `Use Stairs and Slabs`: Enable detailed blocks for smoother curves
* `Keep Existing`: Preserve existing blocks in that component's area

## Tips

{% hint style="info" %}
Start with a simple tree and gradually add complexity. Enable one component at a time to understand how each affects the result.
{% endhint %}

{% hint style="info" %}
Use `Super Sphere` leaves with a high exponent for more cube-like canopies, or a low exponent for spiky, organic shapes.
{% endhint %}

{% hint style="info" %}
Enable `Wind` settings for trees that appear to be naturally bent by prevailing winds.
{% endhint %}

{% hint style="info" %}
For dead trees, disable `Generate Leaves` and increase `Twig` settings for bare, branchy silhouettes.
{% endhint %}

## Tutorial Videos

{% embed url="https://www.youtube.com/watch?v=Wr_-LjmB5j0" %}

{% embed url="https://www.youtube.com/watch?v=hHKSrMDrrGk" %}

{% embed url="https://www.youtube.com/watch?v=_ZPfnazT0vs" %}
