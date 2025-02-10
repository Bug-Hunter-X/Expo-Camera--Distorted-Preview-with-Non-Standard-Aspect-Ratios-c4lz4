# Expo Camera Preview Distortion Bug

This repository demonstrates a bug in Expo's `Camera` component where the preview image is distorted or cropped when using certain aspect ratios.  The issue seems most prominent with aspect ratios that aren't simple multiples (e.g., 16:9). The `bug.js` file shows the buggy implementation; `bugSolution.js` offers a workaround.

**To reproduce:**
1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Observe the camera preview.  You'll likely notice distortion or cropping with the default aspect ratio (16:9).

**Potential Causes:**
The root cause might lie in how Expo handles aspect ratio calculations and/or the underlying camera API's handling of non-standard aspect ratios.

**Workaround:**
The provided workaround (`bugSolution.js`) involves adjusting the camera's `ratio` prop to a more compatible value. However, this solution requires compromise (changing your target aspect ratio). A more robust solution from the Expo team is desirable.