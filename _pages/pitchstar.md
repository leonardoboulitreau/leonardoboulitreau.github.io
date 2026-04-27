---
title: "PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice"
layout: single
permalink: /pitchstar/
date: 2026-04-23T00:00:00-03:00
---
<link rel="stylesheet" href="/_papers/PitchSTAR/css/essential_audio.css">
<style>
  td.condition { color: #ff0000; font-weight: bold; }
  div.essential_audio { max-width: 40px; margin: 0 auto; }
</style>

This is an accompanying page for the paper “PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice”, currently under review. 

PitchSTAR is a self-supervised framework for arbitrary pitch style transfer based on flow matching, which operates on note-relative pitch modulation, allowing it to disentangle note tone from pitch techniques. PitchSTAR also uses an auto-regularization strategy of exploiting the noisy inputs inherent to flow matching training, to allow conditioning on the full reference through a blurred cross-attention, forcing the model to capture both global and local stylistic characteristics while avoiding trivial reference copying.

<div style="display: flex; gap: 12px; margin: 24px 0; justify-content: center;">
  <a href="#" class="btn btn--primary"><i class="fas fa-file-alt"></i> Paper</a>
  <a href="#" class="btn btn--primary"><i class="fab fa-github"></i> Code (Upon Acceptance)</a>
</div>

<div style="text-align: center; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/pitchstar.svg" alt="PitchSTAR" style="max-width: 100%; width: 100%;">
</div>
Training scheme of PitchSTAR. Two optimization steps at low and high noise levels are shown with highlighted sharp and blurred cross-attention matrices, respectively.

# Sound Samples

We randomly select style references for each pitch style from the training set of the GTSinger, and randomly select content note sequences from the test set. 

<table style="border-collapse: collapse; width: 100%;">
  <thead>
    <tr>
      <th style="padding: 8px 12px; text-align: left;"></th>
      <th style="padding: 8px 12px; text-align: center;">Source</th>
      <th style="padding: 8px 12px; text-align: center;" colspan="2">Reference</th>
      <th style="padding: 8px 12px; text-align: left;">Model</th>
      <th style="padding: 8px 12px; text-align: center;" colspan="2">Transfer</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="5">Sample 1</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/nomod/English_EN-Alto-2_Vibrato_Young_And_Beautiful_Vibrato_Group_0000_score.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/pitchstar/English_EN-Alto-2_Vibrato_Young_And_Beautiful_Vibrato_Group_0000_Korean_KO-Tenor-1_Vibrato_되풀이（Repeatedly）_Vibrato_Group_0003_Label0.npy_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 650px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Notes</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/nomod/English_EN-Alto-2_Vibrato_Young_And_Beautiful_Vibrato_Group_0000_score.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 650px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/pitchstar/English_EN-Alto-2_Vibrato_Young_And_Beautiful_Vibrato_Group_0000_Korean_KO-Tenor-1_Vibrato_되풀이（Repeatedly）_Vibrato_Group_0003_Label0.npy_tVibrato.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR w/o Flow</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/transnoise/English_EN-Alto-2_Vibrato_Young_And_Beautiful_Vibrato_Group_0000_Korean_KO-Tenor-1_Vibrato_되풀이（Repeatedly）_Vibrato_Group_0003_Label0.npy_tVibrato.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher w/ Mod</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/detpitcher/English_EN-Alto-2_Vibrato_Young_And_Beautiful_Vibrato_Group_0000_Korean_KO-Tenor-1_Vibrato_되풀이（Repeatedly）_Vibrato_Group_0003_Label0.npy_tVibrato.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/stylepitcher/English_EN-Alto-2_Vibrato_Young_And_Beautiful_Vibrato_Group_0000_Korean_KO-Tenor-1_Vibrato_되풀이（Repeatedly）_Vibrato_Group_0003_Label0.npy_tVibrato.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="5">Sample 2</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 650px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Notes</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 650px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher w/ Mod</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR w/o Flow</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="5">Sample 3</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 650px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Notes</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 650px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher w/ Mod</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR w/o Flow</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="5">Sample 4</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 650px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Notes</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 650px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher w/ Mod</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR w/o Flow</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
  </tbody>
</table>

# Effect of CFG

Describe what problem you were solving and why it mattered.

<table style="border-collapse: collapse; width: 100%;">
  <thead>
    <tr>
      <th style="padding: 8px 12px; text-align: left;"></th>
      <th style="padding: 8px 12px; text-align: center;">Source</th>
      <th style="padding: 8px 12px; text-align: center;" colspan="2">Reference</th>
      <th style="padding: 8px 12px; text-align: left;">Model</th>
      <th style="padding: 8px 12px; text-align: center;" colspan="2">Transfer</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="5">Sample 1</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 650px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Notes</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 650px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher w/ Mod</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR w/o Flow</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="5">Sample 2</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 650px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Notes</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 650px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher w/ Mod</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR w/o Flow</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="5">Sample 3</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 650px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Notes</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 650px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher w/ Mod</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR w/o Flow</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="5">Sample 4</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 650px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Notes</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="5"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 650px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">StylePitcher w/ Mod</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR w/o Flow</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">PitchSTAR</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
  </tbody>
</table>

# Pitch Style Classifier 

## Test Data

## Pitch Style Transfer Models

# Citation

If you use our work in your research, please cite our paper:


<div style="position: relative; margin: 16px 0;">
  <pre id="bibtex" style="padding: 6px 10px; overflow-x: auto; font-size: 0.55em;">@article{boulitreau2026pitchstar,
  title     = {PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice},
  author    = {Boulitreau, Leonardo and Richard, Gael},
  journal   = {arXiv preprint},
  year      = {2026}
}</pre>
  <button onclick="navigator.clipboard.writeText(document.getElementById('bibtex').innerText).then(() => { this.innerText = 'Copied!'; setTimeout(() => this.innerText = 'Copy', 2000); })" style="position: absolute; top: 8px; right: 8px; padding: 4px 10px; font-size: 0.8em; cursor: pointer;">Copy</button>
</div>

<script src="/_papers/PitchSTAR/js/essential_audio.js"></script>
