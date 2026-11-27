# 04 — Functional & Device Testing Log

| Test ID | Feature Tested | Test Procedure | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-01** | Plane Detection & Guide Dots | Scan textured floor/desk in well-lit room; tap **Guide Dots** toggle and place grid | Faint dots appear during scan, toggle manually, and auto-hide upon placement | Verified on Android ARCore device; dots hide on placement and restore on **Reset** | Passed |
| **TC-02** | Flat Horizontal Grid & Horizon Elevation | Tap flat surface to place 2-Point grid, then drag **Horizon Elevation** slider | Horizon shifts smoothly while grid remains flat on the surface | Verified after `PaperHorizonAligner` execution-order fix | Passed |
| **TC-03** | Snap Wall Mode | Aim at vertical wall and tap **Snap Wall** | Grid rotates flush against the vertical wall plane | Verified; toggles cleanly between upright wall and flat paper | Passed |
| **TC-04** | Trace Photo & Clear White Shader | Switch to **Trace**, load sample/gallery photo, and toggle **Clear White** | White background becomes transparent over live camera paper view | Verified real-time GPU keying with **Opacity**, **Scale**, **Rotate**, and **Pin** | Passed |
| **TC-05** | Side Dock UI & How to Use Modal (`?`) | Launch app, dismiss guide, tap **`?`** button, and test **Hide UI** | Guide modal centers cleanly; **`?`** reopens modal; side buttons do not overlap sliders | Verified after `SideDockUIStyler` and Canvas hierarchy fix | Passed |
| **TC-06** | Low-Light Tracking Warning | Cover camera / test in dim lighting | Compact red warning banner prompts user for brighter lighting without overlapping buttons | Verified top-center pill banner layout | Passed |

*Note: Actual device test screenshots are stored in `04-testing-and-qa/screenshots/`.*
