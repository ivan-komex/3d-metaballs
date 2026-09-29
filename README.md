Photorealistic Scene in Blender — Metaball Technique

An 8-second looping 3D animation built in Blender, where two soft, liquid-like shapes merge and split behind a fluted glass wall. Made for the 3D Computer Graphics course at the University of Osijek.

Overview
Engine: Cycles
Resolution: 1920 × 1080 (Full HD)
Length: 240 frames @ 30 fps (8s, seamless loop)
Output: MP4 (H.264)
Techniques used
Metaballs — the two main blob shapes are built from four metaball elements (two main + two smaller "satellites") using Blender's density-field system. Threshold: 0.6, Resolution / Render Resolution: 0.01 m.
Curve-driven motion — instead of manually keyframing object location, each metaball follows a Bézier circle via a Follow Path constraint. The motion itself lives on the curve's own Path Animation, not on the constraint's Offset value.
Array modifier — the glass wall is a single cube duplicated into a row of evenly spaced strips.
Glass material — Principled BSDF with Transmission Weight: 1.0, IOR: 1.5, Roughness: 0.0.
Lighting — two Area lights with scrim diffusers (soft, studio-style light), one lighting the background plane, the other the blobs, plus a flat low-strength White World background for ambient fill.
Camera — 98 mm focal length, f/2.8 for a shallow depth of field that keeps focus on the main body while the separating blob drifts out of focus.
Compositing — light film grain, edge vignette, and a color grading pass added in post.
A note on the wall

At first glance the glass strips look like they physically bend around the blob. They don't — the strips are completely static. The illusion comes from the gaps between strips revealing different slivers of the round metaball shape behind them, which the eye reads as a continuous curved edge.

Requirements
Blender 5.0 or newer. The file was saved in 5.0.1; opening it in an older version (e.g. 3.x) can silently fail and load an empty default scene instead of throwing an error.
Files
3D_Projekt.blend — main scene file
