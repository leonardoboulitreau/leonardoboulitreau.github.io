---
title: "PitchSTAR: Self-Supervised Pitch Style Transfer with Complementary Temporal and Time-Agnostic Style Representations"
layout: single
classes: wide
author_profile: false
permalink: /pitchstar/
date: 2026-04-23T00:00:00-03:00
---
<link rel="stylesheet" href="/_papers/PitchSTAR/css/essential_audio.css">
<style>
  div.essential_audio { max-width: 40px; margin: 0 auto; }
  #main .page { width: 100%; float: none; }
  .page__content p { font-size: 0.7em; }
  .fig-caption { font-size: 0.65em; color: #666; text-align: center; margin-top: 4px; margin-bottom: 2em; }
  table td, table th { border: none !important; }
</style>
<div style="display: flex; gap: 12px; margin: 24px 0; justify-content: center;">
  <a href="#" class="btn btn--primary"><i class="fas fa-file-alt"></i> Paper</a>
  <a href="#" class="btn btn--primary"><i class="fab fa-github"></i> Code (Upon Acceptance)</a>
</div>

This is an accompanying page for the paper "PitchSTAR: Self-Supervised Pitch Style Transfer with Complementary Temporal and Time-Agnostic Style Representations", currently under review. PitchSTAR is a self-supervised framework for arbitrary pitch style transfer (PST). The PST task is defined as generating a pitch curve given a reference ornamented pitch (style) and notes (content), represented in the Figure 1.

<div style="text-align: center; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/pst.svg" alt="PitchSTAR" style="max-width: 100%; width: 35%;">
</div>
<div class="fig-caption">Figure 1. The (Pitch Style Transfer) PST task.</div>

PitchSTAR is a flow-matching framework for pitch style transfer. It models a full style reference through note-relative pitch modulation and temporal and time-agnostic branches, which capture phrase-level organization and ornament details and limit trivial copying in a self-supervised training setting, as shown on Figure 2.

<div style="text-align: center; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/pitchstar.svg" alt="PitchSTAR" style="max-width: 100%; width: 75%;">
</div>
<div class="fig-caption">Figure 2. Training scheme of PitchSTAR. Two optimization steps at low and high noise levels are shown with highlighted sharp and blurred cross-attention matrices, respectively.</div>

# Sound Samples

## In-Domain 

### Sample 1

### Sample 2

### Sample 3

### Sample 4

## Out-of-Domain 

### Sample 1

### Sample 2

### Sample 3

### Sample 4


# Effect of CFG
In this section we show the effect of the guidance CFG scale, which balances guided by style and unguided generation.

### Sample 1

### Sample 2

# Pitch Style Classifier 
In this section we plot the results of the trained Pitch Ornament Classifier, through its confusion matrices.

## Test Data
This confusion matrix is obtained on the test set of the GTSinger.

<div style="text-align: center; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/classifier_cm_test.png" alt="PitchSTAR" style="max-width: 100%; width: 35%;">
</div>
<div class="fig-caption">Figure 3. Confusion Matrix of the Pitch Style Classifier on the test set.</div>

## Pitch Style Transfer Models
These are the matrices obtained applying on the transfer of each of the models.

<div style="display: flex; justify-content: center; gap: 16px; margin: 24px 0;">
  <div style="text-align: center; width: 23%;">
    <div style="font-weight: bold; font-size: 0.8em; margin-bottom: 6px;">PitchSTAR</div>
    <img src="/_papers/PitchSTAR/pictures/cm_pitchstar.png" alt="PitchSTAR" style="max-width: 100%; width: 100%;">
  </div>
  <div style="text-align: center; width: 23%;">
    <div style="font-weight: bold; font-size: 0.8em; margin-bottom: 6px;">PitchSTAR w/o Flow</div>
    <img src="/_papers/PitchSTAR/pictures/cm_transnoise.png" alt="PitchSTAR" style="max-width: 100%; width: 100%;">
  </div>
  <div style="text-align: center; width: 23%;">
    <div style="font-weight: bold; font-size: 0.8em; margin-bottom: 6px;">StylePitcher w/ Mod</div>
    <img src="/_papers/PitchSTAR/pictures/cm_detpitcher.png" alt="PitchSTAR" style="max-width: 100%; width: 100%;">
  </div>
  <div style="text-align: center; width: 23%;">
    <div style="font-weight: bold; font-size: 0.8em; margin-bottom: 6px;">StylePitcher</div>
    <img src="/_papers/PitchSTAR/pictures/cm_stylepitcher.png" alt="PitchSTAR" style="max-width: 100%; width: 100%;">
  </div>
</div>
<div class="fig-caption">Figure 3. Confusion Matrix of the Pitch Style Classifier on the test set.</div>

# Synthetic Dataset Samples
Four examples of the synthetic ornament dataset are shown. Two with ornament and two without ornament.

### With Ornament 1
<div style="display: flex; justify-content: center; gap: 24px; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/syn_1.png" alt="PitchSTAR" style="max-width: 35%; width: 35%;">
  <img src="/_papers/PitchSTAR/pictures/syn_1_pitch.png" alt="PitchSTAR" style="max-width: 35%; width: 35%;">
</div>
<div class="fig-caption">Figure 8. Synthetic notes and their corresponding ornamented pitch.</div>

### With Ornament 2
<div style="display: flex; justify-content: center; gap: 24px; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/syn_2.png" alt="PitchSTAR" style="max-width: 35%; width: 35%;">
  <img src="/_papers/PitchSTAR/pictures/syn_2_pitch.png" alt="PitchSTAR" style="max-width: 35%; width: 35%;">
</div>
<div class="fig-caption">Figure 9. Synthetic notes and their corresponding ornamented pitch.</div>

### Without Ornament 1
<div style="display: flex; justify-content: center; gap: 24px; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/syn_nomod_1.png" alt="PitchSTAR" style="max-width: 35%; width: 35%;">
  <img src="/_papers/PitchSTAR/pictures/syn_nomod_1_pitch.png" alt="PitchSTAR" style="max-width: 35%; width: 35%;">
</div>
<div class="fig-caption">Figure 10. Synthetic notes and their corresponding non-ornamented pitch.</div>

### Without Ornament 2
<div style="display: flex; justify-content: center; gap: 24px; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/syn_nomod_2.png" alt="PitchSTAR" style="max-width: 35%; width: 35%;">
  <img src="/_papers/PitchSTAR/pictures/syn_nomod_2_pitch.png" alt="PitchSTAR" style="max-width: 35%; width: 35%;">
</div>
<div class="fig-caption">Figure 11. Synthetic notes and their corresponding non-ornamented pitch.</div>

<script src="/_papers/PitchSTAR/js/essential_audio.js"></script>
