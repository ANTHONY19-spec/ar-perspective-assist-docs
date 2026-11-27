# 02 — System Design & Architecture

## Architectural Overview
**AR Perspective Assist** uses an on-device modular component architecture attached to Unity's **`XR Origin (AR Rig)`** inside `SampleScene.unity`, built on **Unity 6 (`6000.6.9f1`)**, **AR Foundation**, **Google ARCore**, and the **Universal Render Pipeline (URP)**.

## Core Modules & Responsibilities
- **Plane Detection & Raycasting (`ARPlaneManager`, `ARRaycastManager`):** Tracks device 6DoF pose, detects horizontal desks/paper and vertical walls, and resolves screen taps into world-space poses.
- **3D Perspective Grid (`PerspectiveAssistManager`, `PerspectiveGridGenerator`, `PerspectiveModeController`):** Generates procedural `LineRenderer` geometry for **1-Point** and **2-Point** perspective and updates **Horizon Elevation**, **VP Spread**, and **Grid Opacity** in real time.
- **Surface Alignment (`PaperHorizonAligner`):** Pitches the perspective rig flat across horizontal paper/floors (`[DefaultExecutionOrder(1000)]` so slider updates preserve flat alignment) and toggles upright wall alignment via **Snap Wall**.
- **Guide Dots Controller (`GuideDotsController`):** Softens scanning plane dots (`0.25` opacity), toggles visibility (`Guide Dots: On / Off`), and auto-hides dots once a grid or trace quad is anchored.
- **Photo Tracing & GPU Shader (`TraceModeController`, `TraceWhiteKey.shader`):** Anchors a 3D `PrimitiveType.Quad` onto paper via `ARAnchor`, imports built-in sketches (`Assets/TraceSketches/`) or device photos (`NativeGallery`), strips white backgrounds on the GPU (**Clear White**), and applies **Opacity**, **Scale**, **Rotate**, **Pin**, and **Reset Size**.
- **UI & Tracking Diagnostics (`SideDockUIStyler`, `ThesisUXPolish`):** Arranges controls into a frosted right-hand thumb dock, displays the centered **How to Use** modal (`?`), keeps the screen awake, and displays `ARSession.notTrackingReason` warnings.
