---
title: "PitchSTAR"
layout: single
permalink: /pitchstar/
date: 2026-04-23T00:00:00-03:00
---
This is an accompanying page for the paper “PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice”, currently under review. PitchSTAR is a self-supervised framework for arbitrary pitch style transfer based on flow matching, which operates on note-relative pitch modulation, allowing it to disentangle note tone from pitch techniques. PitchSTAR also uses an auto-regularization strategy of exploiting the noisy inputs inherent to flow matching training, to allow conditioning on the full reference through a blurred cross-attention, forcing the model to capture both global and local stylistic characteristics while avoiding trivial reference copying.

<div style="display: flex; gap: 12px; margin: 24px 0; justify-content: center;">
  <a href="#" class="btn btn--primary"><i class="fas fa-file-alt"></i> Paper</a>
  <a href="#" class="btn btn--primary"><i class="fab fa-github"></i> Code</a>
</div>

<div style="text-align: center; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/pitchstar.svg" alt="PitchSTAR" style="max-width: 100%; width: 100%;">
</div>

## Effect of CFG

Describe what problem you were solving and why it mattered.

## Sound Samples

<table style="border-collapse: collapse; width: 100%;">
  <thead>
    <tr>
      <th style="padding: 8px 12px; text-align: left;"></th>
      <th style="padding: 8px 12px; text-align: left;">Condition</th>
      <th style="padding: 8px 12px; text-align: center;">Audio</th>
      <th style="padding: 8px 12px; text-align: center;">Spectrogram</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="3">Sample 1</td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="3"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 320px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="3">Sample 2</td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="3"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 320px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="3">Sample 3</td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="3"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 320px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="3">Sample 4</td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="3"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 320px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><audio controls style="width: 120px;"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
  </tbody>
</table>

## links

- [GitHub Repository](https://github.com/leonardoboulitreau)
