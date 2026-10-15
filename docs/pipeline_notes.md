## Spatial calibration

- Calibration: 1.178 µm/pixel.
- Measured using a microscope calibration slide.
- Objective: 10×.
- Camera: Canon EOS 650D.
- Original and test video dimensions: 1920 × 1080 pixels.
- The test video was shortened in iMovie without spatial cropping.

The calibration slide's known distance and the corresponding measured pixel
distance have not yet been recorded here.


## Detection measurement conventions

- Frame numbers are zero-based; inspecting the first decoded frame uses frame 0.
- Image x increases rightward; image y increases downward.
- Positions ending in `_px` are in pixels; `_um` are in micrometres.
- `area_px` is a pixel count; `area_um2` is calibrated area in square micrometres.
- `axis_major_length_px` and `axis_minor_length_px` are shape-axis lengths in pixels.
- `orientation_value` is the shape major-axis angle in radians, measured from
  the image row axis. A shape axis has no head/tail direction and does not by
  itself give the swimming direction.
- `eccentricity_value` is dimensionless.
- `mean_intensity` is measured on background-minus-grayscale, not raw intensity.
- `threshold_value` uses the same corrected-image intensity scale.
- Analysis settings are collected near the top of the notebook. Frame rate is
  read from the input video metadata.

## Cleanup scope: steps 1–6

The segmentation, assignment, gap-closing formulas, thresholds, and manual merge
pairs are preserved. The first-frame inspection label was corrected from 8 to 0.
Empty tables retain their column names; unavailable optional inspections are
skipped, and an analysis with no accepted detections stops with a clear message.
Axis-length column names now include `_px`; numerical values are unchanged.
The random preselection of orientation examples remains unseeded as before.
Saved notebook outputs were preserved for reference and are not a fresh run.
