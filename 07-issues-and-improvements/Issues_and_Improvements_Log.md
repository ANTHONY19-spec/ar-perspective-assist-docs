# 07 — Issues, Corrections & Improvement Records

| Issue ID | Issue Description | Root Cause | Corrective Action |
| :--- | :--- | :--- | :--- |
| **ISS-01** | **Guide Dots: On** button did not hide white AR plane dots on screen. | Button listener only toggled `RoomSurfaceGrid` rather than `ARPlaneManager` trackables. | Implemented `GuideDotsController.cs` to toggle `ARPlane` trackables, reduce scanning dot opacity (`0.25`), and auto-hide dots upon placement. |
| **ISS-02** | Perspective grid stood vertically on horizontal paper/floor and flipped upright when dragging **Horizon Elevation**. | Local XY plane was not pitched flat, and slider/anchor updates reset rotation. | Created `PaperHorizonAligner.cs` (`[DefaultExecutionOrder(1000)]`) to pitch the grid flat on horizontal surfaces and lock orientation during slider adjustments. |
| **ISS-03** | **`?` (HelpButton)** was unresponsive and `HowToUseModal` clipped off-screen. | `HelpButton` and `HowToUseModal` were outside the `UI` Canvas hierarchy and lacked full touch bounds. | Nested both inside `UI`, wired direct `OnClick` activation, and centered `HowToUseModal` full-screen. |
| **ISS-04** | Top-row buttons cluttered the top screen edge and `TrackingWarning` overlapped side buttons. | Buttons were spread across `TopBar` and `TrackingWarning` lacked bounded pill dimensions. | Created `SideDockUIStyler.cs` to group buttons into a frosted right-side thumb rail and style `TrackingWarning` as a compact top pill. |
