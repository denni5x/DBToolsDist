# Poly Tool (WIP)

{% hint style="warning" %}
This tool is currently a Work In Progress. Features and parameters may change.
{% endhint %}

A grid-based tile placement system using marching squares for automatic tile selection and transitions.

## Overview

The Poly Tool allows you to paint on a grid, and it automatically selects the appropriate tile/module based on the surrounding cells using a marching squares algorithm. This is useful for creating terrain, walls, or other tiled structures with proper edge transitions.

<!-- TODO: Add overview screenshot -->

## Usage

* The tool displays a grid overlay
* **Click** on cells to toggle them between filled and empty
* The marching squares algorithm automatically determines which module to place at each cell
* Modules are blueprints that have been configured with socket information for proper connections

## Concepts

### Dual Grid System

* **Main Grid**: The grid you interact with to mark cells as filled or empty
* **Offset Grid**: The rendering grid where actual tiles are placed (offset by half a cell)

### Marching Squares

The tool uses a marching squares algorithm to look at the 4 corners of each render cell and determine which tile configuration to use (0-15 possible configurations).

### Sockets

Each module face has socket information that determines how it can connect to neighboring tiles, ensuring proper transitions between different tile types.

## Tool Options

<!-- TODO: Add screenshots and document parameters -->

* `Cell Size`: The size of each grid cell
* `Opacity`: Preview render opacity (0-1)
* `Show Cell Outlines`: Display grid lines
* `Show Filled Cells`: Highlight filled cells

### Placement Options

* `Rotation`: Rotate the selected module (0, 90, 180, 270 degrees)
* `Flip X`: Mirror the module on the X axis
* `Flip Z`: Mirror the module on the Z axis

## Asset Configuration

Modules/blueprints need to be configured with socket information before they can be used with the Poly Tool.

<!-- TODO: Document asset configuration -->

{% hint style="info" %}
Join the Discord for updates on this tool's development and to provide feedback.
{% endhint %}
