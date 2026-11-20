LPW Visible Pupil and Iris Segmentation

This collection contains 200 frames from 18 LPW videos recorded with 12 participants. It includes 189 newly extracted frames and 11 images retained from version 3. The masks for those 11 images follow the labeling rules used in this release.

Mask labels
Each mask is a 640 x 480 single-channel PNG. Pixel values are 0 for background and other tissue, 1 for visible pupil, and 2 for visible iris. Small reflections inside the pupil or iris take the label of the surrounding region and contribute to training.

Files
The images/ directory contains the original video frames. Each frame has a mask with the same filename in masks/. The overlays/ and thumbs/ directories contain visual previews. Load the masks as grayscale images and preserve the integer class values. Use nearest-neighbor interpolation when resizing masks.

Annotation method
Reference contours were traced on selected frames. LPW pupil centers and bidirectional optical flow guided alignment to candidate frames. Pupil boundaries were refined, contours were smoothed, and each candidate overlay was checked against its original frame. These AI-assisted annotations await human review. LPW provides pupil centers only, so pixel-level accuracy could not be verified against the source annotations.

Training and validation
The manifest.csv file lists the participant, video, zero-based frame number, and reference frame for each image. Frames from the same recording are correlated. To evaluate performance on new participants, keep all frames from each participant in a single split.

Source and license
Bulling, Andreas (2023). Labeled pupils in the wild (LPW). DaRUS, V1. https://doi.org/10.18419/DARUS-3237
The source data and derived annotations are licensed under CC BY-NC-SA 4.0.

