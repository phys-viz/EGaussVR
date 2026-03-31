# Gauss's Law Symmetry Explorer VR

An interactive VR simulation for exploring Gaussian surface symmetry in introductory electromagnetism, built with Three.js and WebXR for Meta Quest.

Designed and developed by Anthony Danese, high school physics teacher.

## What it does

Students choose a charge distribution and a Gaussian surface, then drag the surface through 3D space to discover where the electric field magnitude becomes constant on the surface - the condition that makes Gauss's Law useful for calculating E. Representative square tiles on each surface display E-field arrows whose color and length encode magnitude, giving students an immediate visual signal for whether the surface placement exploits symmetry.

## Features

- Two charge distributions: positive point charge and infinite line charge
- Three Gaussian surface choices: sphere, cylinder with axis parallel to line, cylinder with axis perpendicular to line
- Transparent shell surfaces with representative square dA tiles at evenly spaced sample points
- E-field arrows at each tile center - color-coded (blue -> red) and length-scaled by magnitude
- Nonlinear magnitude mapping (t^0.4) for strong visual contrast between weak and strong field regions
- Uniformity detection - when E is constant on the surface, all arrows turn green and the surface pulses
- 3D crosshair at sphere center and dashed cylinder axis line as symmetry alignment cues
- Icon-based VR selection panel with high-contrast labels and bold icons
- Movable VR panel - grip the panel background to reposition it
- Right thumbstick scene control - horizontal to orbit around the charge, vertical to raise/lower the scene
- Desktop preview mode with orbit controls and click-drag surface positioning

## Controls

| Action | Control |
|---|---|
| Select distribution/surface | Point controller ray at panel icon, press trigger |
| Drag Gaussian surface | Point at surface, hold trigger and move |
| Move VR panel | Point at panel background, hold grip and move |
| Orbit scene | Right thumbstick horizontal |
| Raise/lower scene | Right thumbstick vertical |
| Reset surface position | Press RESET button on panel |

## How to use

1. Open your Meta Quest browser and navigate to the live sim
2. Tap **Enter VR**
3. Select a charge distribution from the floating panel (POINT or LINE)
4. Select a Gaussian surface (SPHERE, CYL ∥, or CYL ⊥)
5. Point at the translucent surface and hold the trigger to drag it
6. Watch the E-field arrows - when all arrows match in color and length, you've found the symmetric placement
7. Use the right thumbstick to orbit and peek at the poles or endcaps
8. Try "wrong" combinations (for example, sphere around a line charge) to see why symmetry matters

**Live sim:** https://phys-viz.github.io/GaussSymmetryVR/

## Pedagogical context

This simulation targets a specific conceptual gap in Gauss's Law instruction: students memorize which surface pairs with which distribution but do not understand *why* the surface choice matters. By letting students drag surfaces freely and see the E-field magnitude vary (or not) across the surface in real time, they discover the symmetry argument for themselves. The "wrong" combinations - a sphere around a line charge, a perpendicular cylinder around a point charge - are just as important as the correct ones. Students can explore all six combinations and see that only specific pairings and placements produce the constant-magnitude condition that makes the flux integral tractable.

The square tiles on the surface are intentionally designed to evoke the dA area elements from the flux integral, connecting the visual experience to the mathematics students encounter on paper.

This simulation is part of a suite of VR simulations for introductory electromagnetism hosted at [phys-viz.github.io](https://phys-viz.github.io).

## Tech stack

- **Three.js** r162
- WebXR API
- Vanilla JavaScript - no build tools, no frameworks
- Hosted on GitHub Pages

## License

Copyright 2026 Anthony Danese. Licensed under **CC BY-NC-SA 4.0**.
Free for educational use. Commercial use requires explicit written permission.
