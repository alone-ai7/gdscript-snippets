# 🎮 GDScript Snippets Library

A collection of isolated, modular GDScript attachments and reusable mechanics. These scripts are designed to be copied directly into Godot engine projects to handle independent player logic, mathematical formulas, and node behaviors. Also make sure to read the INSTRUCTIONS.md, it's inside the gdscript-snippets folder.

## 📁 Library Index

This repository separates code templates by functional categories. Each subdirectory contains standalone, raw `.gd` text files ready for script attachment. For example:

* **[2D_Movement](./2D_Movement/)**
  * `player_top_down.gd` — Fluid 8-way directional velocity controls.
  * `player_platformer.gd` — Vector-based gravity, jumping mechanics, and floor checks.
* **[Physics_Formulas](./Physics_Formulas/)**
  * `custom_acceleration.gd` — Linear interpolation (`lerp`) adjustments for friction and inertia.
  * `projectile_trajectory.gd` — Mathematical angling for gravity-influenced paths.
* **[Camera_Utilities](./Camera_Utilities/)**
  * `smooth_follow.gd` — Script attachment for tracking target positions smoothly.

## 🛠️ Implementation Guide

To implement these scripts inside your local Godot Engine project interface:

1. Create a new, blank script file on your target Node in the scene tree.
2. Ensure the base type declared at the absolute top of the file matches the node's class requirement (e.g., `extends CharacterBody2D` or `extends KinematicBody2D`).
3. Replace the default template layout text with the snippet code copied from the corresponding repository file here.

## ⚙️ Target Environment
* **Engine Reference:** Structured for Godot 3.5.3 stable logic patterns.

