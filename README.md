# From Baseline to HIT-Tracker: An Experimentally Optimized Pipeline for Infrared Multi-UAV Tracking

**Ighor de Souza Ribeiro** (CIAA), **Rigel Procópio Fernandes** (DSAM), **Gabriel de Sapienza Luna** (CIAA / UFRJ)

LAFusion 2026 — Fourth Latin American Workshop on Information Fusion

**[Slides (PDF)](slides/LAFusion2026_slides.pdf)**

---

## Slide 2 · From One UAV to a Swarm

<img src="media/single_uav.gif" width="100%" alt="Single UAV in visible light">

<img src="media/swarm.gif" width="100%" alt="Infrared swarm">

One visible UAV is easy to follow; in infrared swarms the targets are small, textureless and look alike.

## Slide 6 · Root Cause

<img src="media/fig1.png" width="100%" alt="Correlation of swarm density, camera motion, edge density and local contrast with IDF1">

Structured clutter (edge density) correlates with IDF1 at r = −0.600; swarm density and camera motion do not explain identity loss.

## Slide 8 · H: Hard-Example Mining

<img src="media/hard_examples.gif" width="100%" alt="Hardest training sequences">

The hardest training sequences (clutter, low contrast) are used to fine-tune the detector.

## Slide 9 · T: Tiled Inference (SAHI)

<img src="media/tiles_detection.gif" width="100%" alt="Full frame versus 512-px tiles">

Overlapping 512-px tiles help the detector find small targets (green: matched, orange: missed).

## Slide 12 · I in Action

<img src="media/association_switch.gif" width="100%" alt="Identity switch with BoT-SORT versus GM + NSA">

BoT-SORT switches the ID of the circled drone (894 → 1051); GM + NSA (γ = 0.55) keeps it (ID 6).

## Slide 14 · HIT-Tracker Results

<img src="media/fig3.png" width="100%" alt="MOTA, IDF1 and ID switches from baseline to HIT-Tracker">

MOTA 76.0 → 79.9, IDF1 71.2 → 82.7, identity switches 2,355 → 494 (−79.0%).

## Slide 15 · Seeing the Difference

<img src="media/facade_comparison.gif" width="100%" alt="Baseline versus HIT-Tracker on the facade sequence">

Same facade sequence: the baseline keeps changing identities, HIT-Tracker keeps them.

## Backup · UAV240, Frame 309

<img src="media/uav240_comparison.gif" width="100%" alt="Matched targets per frame on UAV240">

Matched targets per frame; at frame 309, BoT-SORT matches 5 of 20 and HIT-Tracker matches 20 of 20.

## Backup · γ Sweep

<img src="media/fig2.png" width="100%" alt="MOTA, IDF1 and ID switches as a function of gamma">

MOTA stays within 0.3 p.p. of its maximum for γ ∈ [0.25, 0.65]; identity switches are lowest at γ = 0.55.

---

## Code and paper

- Code and experimental materials: [github.com/IghorRibeiro/DroneTrackingMOT](https://github.com/IghorRibeiro/DroneTrackingMOT)
- Citation: I. S. Ribeiro, R. P. Fernandes and G. S. Luna, "From Baseline to HIT-Tracker: An Experimentally Optimized Pipeline for Infrared Multi-UAV Tracking," Fourth Latin American Workshop on Information Fusion (LAFusion 2026), Springer CCIS, to appear.

## Credits

- 4th Anti-UAV Challenge, Track 3 (China Telecom, 2025), DOI [10.5281/zenodo.15103888](https://doi.org/10.5281/zenodo.15103888)
- DUT Anti-UAV (Zhao et al., 2022)

Images derived from these datasets follow the original dataset terms.
