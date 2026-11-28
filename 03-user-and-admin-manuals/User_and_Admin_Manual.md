# User and Administrator Manual

Project: AR Perspective Assist: A Real-Time 2-Point Perspective Drawing Guide  
Target Platform: Android (ARCore-Supported Mobile Devices)  
Engine Version: Unity 6 (6000.6.9f1)

---

## Part 1: End-User Manual (Students and Instructors)

### 1. System Requirements
- Operating System: Android 8.0 (Oreo) or newer with Google Play Services for AR (ARCore) installed.
- Hardware: Rear camera with autofocus, gyroscope, and accelerometer.
- Environment: Well-lit room with textured, non-glossy drawing paper or desk surface.

### 2. Calibration and Grid Placement
1. Launch AR Perspective Assist and grant camera permission when prompted.
2. Point the rear camera at a flat desk or drawing paper and move the phone slowly side-to-side until soft scanning dots appear.
3. Tap the detected surface to anchor the 3D perspective rig. Guide dots automatically hide once the grid is anchored.
4. Use the bottom-left sliders to adjust horizon height, left/right vanishing-point spread, and grid density.

### 3. Perspective Modes and Surface Alignment
- 1-Point and 2-Point Toggle: Switch between single central vanishing-point convergence and dual lateral vanishing points.
- Snap Floor / Snap Wall: Aligns the perspective grid flat onto a horizontal drawing sheet or upright against a vertical wall/board.
- Lock / Pin Grid: Freezes the current anchor position so accidental screen touches do not shift vanishing points while sketching.

### 4. Photo Trace Mode (Clear White Overlay)
1. Tap the Trace button on the right-side dock to switch from perspective grid mode to photo overlay mode.
2. Cycle through built-in reference sketches or tap Gallery to import a reference image from your device.
3. Toggle Clear White to run the GPU shader that removes white paper backgrounds, leaving only dark linework over your physical sheet.
4. Adjust opacity, scale, and rotation sliders to match your paper dimensions, then tap Pin to lock the overlay.

---

## Part 2: Administrator and Deployment Manual

### 1. Standalone APK Installation (Field Testing Devices)
1. Transfer the signed release APK (`ARPerspectiveAssist.apk`) to the test Android device via USB or local file transfer.
2. Open the device file manager, tap the APK file, and allow Install from Unknown Sources if prompted.
3. Verify offline functionality by launching the app in Airplane Mode (no external server or internet connection is required).

### 2. Common Field Troubleshooting
- Tracking Lost / Warning Pill Appears: Move the camera away from blank white walls or reflective glass toward a textured desk edge under steady indoor lighting.
- Gallery Import Fails: Confirm Storage / Media permissions are enabled under Android Settings > Apps > AR Perspective Assist > Permissions.
- App Fails to Install: Ensure Google Play Services for AR is updated on the device and at least 150 MB of free storage is available.

### 3. Repository Maintenance Rules
- Source Code (`ar-perspective-assist-system`): Keep only `Assets/`, `Packages/`, `ProjectSettings/`, `.gitignore`, and `README.md` in `main`. Never commit `Library/`, `Temp/`, `.utmp/`, or `.apk` build artifacts.
- Documentation (`ar-perspective-assist-docs`): Store anonymized evaluation data only in `06-user-feedback-and-evaluation/` in compliance with Republic Act No. 10173 (Data Privacy Act of 2012).