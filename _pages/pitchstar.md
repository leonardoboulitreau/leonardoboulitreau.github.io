---
title: "PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice"
layout: single
permalink: /pitchstar/
date: 2026-04-23T00:00:00-03:00
---
<link rel="stylesheet" href="/_papers/PitchSTAR/css/essential_audio.css">
<style>
  div.essential_audio > div:nth-child(1) div {
    left: 0px !important;
    transition: none !important;
  }
</style>

This is an accompanying page for the paper “PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice”, currently under review. PitchSTAR is a self-supervised framework for arbitrary pitch style transfer based on flow matching, which operates on note-relative pitch modulation, allowing it to disentangle note tone from pitch techniques. PitchSTAR also uses an auto-regularization strategy of exploiting the noisy inputs inherent to flow matching training, to allow conditioning on the full reference through a blurred cross-attention, forcing the model to capture both global and local stylistic characteristics while avoiding trivial reference copying.

<div style="display: flex; gap: 12px; margin: 24px 0; justify-content: center;">
  <a href="#" class="btn btn--primary"><i class="fas fa-file-alt"></i> Paper</a>
  <a href="#" class="btn btn--primary"><i class="fab fa-github"></i> Code</a>
</div>

<div style="text-align: center; margin: 24px 0;">
  <img src="/_papers/PitchSTAR/pictures/pitchstar.svg" alt="PitchSTAR" style="max-width: 100%; width: 100%;">
</div>

# Sound Samples

<table style="border-collapse: collapse; width: 100%;">
  <thead>
    <tr>
      <th style="padding: 8px 12px; text-align: left;"></th>
      <th style="padding: 8px 12px; text-align: center;">Reference</th>
      <th style="padding: 8px 12px; text-align: center;">Reference Spectrogram</th>
      <th style="padding: 8px 12px; text-align: left;">Condition</th>
      <th style="padding: 8px 12px; text-align: center;">Audio</th>
      <th style="padding: 8px 12px; text-align: center;">Spectrogram</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="4">Sample 1</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 500px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 500px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition D</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="4">Sample 2</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 500px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 500px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition D</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="4">Sample 3</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 500px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 500px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition D</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="4">Sample 4</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 500px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 500px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition D</td>
      <td style="padding: 8px 12px; text-align: center;"><div class="essential_audio" data-url="/_papers/PitchSTAR/audios/glissando_strong_ref.wav"></div></td>
    </tr>
  </tbody>
</table>

# Effect of CFG

Describe what problem you were solving and why it mattered.

# Citation

If you use our work in your research, please cite our paper:


<div style="position: relative; margin: 16px 0;">
  <pre id="bibtex" style="padding: 16px; overflow-x: auto; font-size: 0.85em;">@article{boulitreau2026pitchstar,
  title     = {PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice},
  author    = {Boulitreau, Leonardo and Richard, Gael},
  journal   = {arXiv preprint},
  year      = {2026}
}</pre>
  <button onclick="navigator.clipboard.writeText(document.getElementById('bibtex').innerText).then(() => { this.innerText = 'Copied!'; setTimeout(() => this.innerText = 'Copy', 2000); })" style="position: absolute; top: 8px; right: 8px; padding: 4px 10px; font-size: 0.8em; cursor: pointer;">Copy</button>
</div>

<script src="/_papers/PitchSTAR/js/essential_audio.js"></script>
