# Blueprint To Path

Place blueprints along a curved or straight path with customizable spacing and curve types.

## Usage

* **Right-click** to add path points
* **Left-click** on a point gizmo to select it
* **Drag** the gizmo axes to move points
* **Delete** key removes the selected point (or all points if none selected)
* Press **Enter** to paste the blueprints along the path
* Press **Escape** to deselect the current point

<div align="center"><img src="../.gitbook/assets/BpToPathTool (1).png" alt="" width="500"></div>

## Tool Options

### Blueprints Section

* `Add Blueprint`: Opens the blueprint browser to add a blueprint
* `Add Clipboard`: Adds the current clipboard selection (only available when clipboard is not empty)
* `Clear`: Removes all added blueprints
* `Paste Mode`: Only appears when multiple blueprints are added
  * **Chance Based**: Randomly selects blueprints based on their chance percentage
  * **Alternating**: Cycles through blueprints in order

### Curve Settings

* `Type`: The interpolation method for the path
  * **Line**: Straight segments between points (DDA algorithm)
  * **Catenary**: Hanging rope/chain curve between points
  * **Catmull-Rom**: Smooth spline that passes through all points
  * **Bezier**: Smooth curve using all points as control points
* `Distance`: Spacing between blueprint insertion points along the path (0-50 blocks)
  * Note: This is the distance between insertion points, not between each blueprint's bounds
* `Looped`: Connects the last point back to the first point (requires 3+ points)
* `Inverted` (Catenary only): Flips the catenary curve upside down (arc instead of hang)
* `Slack` (Catenary only): How much the curve sags between points (0-200%)

### Flags

* `Offset When Placing`: When enabled, places on the block face you click rather than inside the block
* `Random Yaw`: Randomly rotates each blueprint (0, 90, 180, or 270 degrees)
* `Random XZ Flip`: Randomly flips blueprints on X and/or Z axis
* `Keep Existing`: Preserves existing blocks; new blocks only fill air
* `Extend To Ground`: Extends the bottom layer of each blueprint down to the ground

### Point Section

When a point is selected, you can:

* View and edit the exact **Position** (X, Y, Z coordinates)
* **Remove** the selected point

## Tips

{% hint style="info" %}
Use **Catenary** curves to create natural-looking hanging bridges, chains, or power lines between posts.
{% endhint %}

{% hint style="info" %}
**Catmull-Rom** is great for organic paths like rivers or roads since it creates smooth curves that pass through every point you place.
{% endhint %}

{% hint style="info" %}
When placing decorations like lanterns along a path, set `Distance` to match the spacing you want between each lantern.
{% endhint %}

{% hint style="info" %}
Select a point and then right-click to insert a new point after it, allowing you to add detail to specific sections of your path.
{% endhint %}

{% embed url="https://www.youtube.com/watch?v=ibA2YGyv_sQ" %}
