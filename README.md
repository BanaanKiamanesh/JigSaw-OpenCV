# Vision-Based Puzzle Solver

### Purpose

Reconstruct a jigsaw-style puzzle from individual piece images using a known solved reference image—fully with classical computer vision (no deep learning).&#x20;
****
### Description

The notebooks segment puzzle pieces via HSV background filtering, clean the masks, and separate any stuck-together fragments (watershed), producing one image per piece ready for matching.&#x20;
Features are extracted with ORB on both the reference and each piece; matches are filtered (ratio test) to estimate an affine transform per piece, which is then applied to place it onto a canvas. Alpha blending smooths borders for a cleaner final reconstruction.&#x20;

* `PEPPA.ipynb` — demo on the PEPPA puzzle (20 pieces), achieving a perfect reconstruction.&#x20;
* `BLUECITY.ipynb` — demo on the BLUE CITY puzzle (48 pieces), correctly placing 43/48 pieces after additional preprocessing.&#x20;

The approach and results are summarized in the included report.&#x20;
