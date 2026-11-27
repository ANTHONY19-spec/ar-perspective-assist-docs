# 03 — User & Administrator Manuals

## Part I: Learner User Manual
### A. 3D Grid Mode (Perspective Drawing Guide)
1. Launch **AR Perspective Assist**, allow **Camera** permission, read the **How to Use** guide, and tap **Start Sketching** (tap **`?`** in the right dock anytime to reopen).
2. Move your phone slowly over a well-lit, matte desk or sheet of drawing paper until faint white **Guide Dots** appear.
3. Tap the paper surface to anchor the perspective grid flat onto the sheet (the scan prompt and dots hide automatically).
4. Use the right-side dock to switch **1-Point / 2-Point**, tap **Snap Wall** for vertical walls, toggle **Guide Dots**, or tap **Reset** to clear and re-scan.
5. Drag **Horizon Elevation**, **VP Spread**, and **Grid Opacity** at the bottom-left to customize your guide.

### B. Trace Photo Mode (Reference Overlay)
1. Tap **Trace** in the right-side dock and tap your drawing paper to anchor the trace surface.
2. Tap **Sample** to cycle built-in sketches or **My Photo** to pick an image from your gallery.
3. Tap **Clear White** to remove white paper backgrounds in real time, adjust **Opacity**, **Scale**, and **Rotate**, and tap **Pin** to lock placement.

## Part II: Administrator / Developer Build Manual
- **Prerequisites:** Unity `6000.6.9f1` with Android Build Support (SDK/NDK/OpenJDK), URP, AR Foundation, Google ARCore XR Plugin, and `NativeGallery`.
- **Deployment:** Open `Assets/Scenes/SampleScene.unity`, verify **Google ARCore** is enabled under **Project Settings → XR Plug-in Management (Android)**, connect an ARCore-supported Android phone via USB debugging, and run **File → Build Profiles → Build And Run**.
