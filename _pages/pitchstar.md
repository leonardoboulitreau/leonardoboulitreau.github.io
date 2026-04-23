---
title: "PitchSTAR: Pitch Style Transfer with Auto-Regularized Flow Matching for Singing Voice"
layout: single
permalink: /pitchstar/
date: 2026-04-23T00:00:00-03:00
---
<link rel="stylesheet" href="/_papers/PitchSTAR/css/tinyPlayer.css">

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
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 500px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 500px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition D</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="4">Sample 2</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 500px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 500px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition D</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="4">Sample 3</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 500px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 500px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition D</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px; font-weight: bold; white-space: nowrap;" rowspan="4">Sample 4</td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="reference spectrogram" style="max-width: 500px; width: 100%;"></td>
      <td style="padding: 8px 12px;">Condition A</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
      <td style="padding: 8px 12px; text-align: center;" rowspan="4"><img src="/_papers/PitchSTAR/pictures/output.png" alt="spectrogram" style="max-width: 500px; width: 100%;"></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition B</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition C</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
    </tr>
    <tr>
      <td style="padding: 8px 12px;">Condition D</td>
      <td style="padding: 8px 12px; text-align: center;"><audio class="iru-tiny-player" preload="none"><source src="/_papers/PitchSTAR/audios/glissando_strong_ref.wav" type="audio/wav"></audio></td>
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

<script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/howler/2.2.4/howler.min.js"></script>
<script>
(function() {
  "use strict";
  $(document).ready(function() {
    var player = irubataru.tinyPlayer.createPlayerFromTags();
  });
  var irubataru = {
    tinyPlayer: {
      Player: class {
        constructor(playlist) {
          this._playlist = playlist; this._index = 0; this._mouse_down = false;
          this._seeking = false; this._animation_timestamp = 0;
          this.ns = irubataru.tinyPlayer;
        }
        play(index) {
          var self = this;
          index = typeof index === 'number' ? index : self._index;
          self._playlist[index].howl.play();
          self._index = index;
        }
        pause(index) {
          var self = this;
          index = typeof index === 'number' ? index : self._index;
          var sound = self._playlist[index].howl;
          if (sound) sound.pause();
        }
        stop(index) {
          var self = this;
          index = typeof index === 'number' ? index : self._index;
          self._playlist[index].howl.stop();
          self._index = index;
        }
        toggleTo(index) {
          var self = this;
          var sound = self._playlist[self._index].howl;
          if (sound.playing()) {
            if (index === self._index) { self.pause(); return; }
            else { sound.stop(); }
          }
          self.play(index);
        }
        seek(index, percentage) {
          var self = this; var ns = this.ns;
          var sound = self._playlist[index].howl;
          var html_elem = self._playlist[index].html_elem;
          var seek_to = percentage * sound.duration();
          sound.seek(seek_to);
          html_elem.find(".song-timer").html(ns._formatTime(seek_to) + " / " + ns._formatTime(sound.duration()));
        }
        updateDuration(index, percentage) {
          var self = this;
          self._playlist[index].html_elem.find(".song-progress").css("width", (percentage * 100 || 0) + "%");
        }
        volume(val) {
          var self = this;
          Howler.volume(val);
          self._playlist.forEach(function(song) {
            song.html_elem.find(".song-volume-bar#fg").css("width", (val * 60) + "%");
            song.html_elem.find(".song-volume-dot").css("left", (val * 60 + 20) + "%");
          });
        }
        step(timestamp) {
          var self = this; var ns = this.ns;
          var sound = self._playlist[self._index].howl;
          var html_elem = self._playlist[self._index].html_elem;
          var seek = sound.seek() || 0;
          html_elem.find(".song-timer").html(ns._formatTime(seek) + " / " + ns._formatTime(sound.duration()));
          if (!self._seeking) self.updateDuration(self._index, seek / sound.duration());
          if (sound.playing()) requestAnimationFrame(self.step.bind(self));
        }
      },
      createPlayerFromTags: function() {
        var ns = this; var playlist = [];
        $("audio.iru-tiny-player").each(function() {
          var title = $(this).attr("data-title") || $(this).prevUntil("audio", ":header").first().html() || "";
          var preload = !(($(this).attr("preload") === "none") || ($(this).attr("preload") === "metadata"));
          var files = [];
          $(this).children("source").each(function() { files.push($(this).attr("src")); });
          var song_elem = ns.createSongPlayer(title);
          playlist.push({ title: title, files: files, html_elem: song_elem, preload: preload, howl: null });
          $(this).after(song_elem);
          $(this).hide();
        });
        var player = new ns.Player(playlist);
        ns._setupEvents(player);
        return player;
      },
      createSongPlayer: function(title) {
        return $("<div>").addClass("iru-tiny-player")
          .append($("<div>").addClass("song-seek"))
          .append($("<div>").addClass("song-progress"))
          .append($("<div>").addClass("song-main-info")
            .append($('<div class="icon fa-play">'))
            .append($('<div class="icon fa-pause">').hide())
            .append($('<div class="icon fa-stop">'))
            .append($('<div class="song-title">').html(title + "  "))
            .append($('<div>').addClass("song-timer"))
            .append($('<div class="icon fa-volume-up">')))
          .append($("<div>").addClass("song-volume-control").hide()
            .append($("<div>").addClass("song-volume-bar").attr("id", "bg"))
            .append($("<div>").addClass("song-volume-bar").attr("id", "fg"))
            .append($("<div>").addClass("song-volume-bar").attr("id", "fgg"))
            .append($("<div>").addClass("song-volume-dot"))
            .append($("<div>").addClass("icon fa-times")));
      },
      _setupEvents: function(player) {
        var ns = this; var song_index = 0;
        player._playlist.forEach(function(song) {
          var this_idx = song_index;
          song.howl = ns._createHowlForPlayer(player, song);
          ns._bindPlayerControls(player, song.html_elem, this_idx);
          ++song_index;
        });
      },
      _createHowlForPlayer: function(player, song) {
        var song_elem = song.html_elem; var ns = this;
        return new Howl({
          src: song.files, html5: true, preload: song.preload,
          onplay: function() {
            song_elem.find(".fa-play").hide(); song_elem.find(".fa-pause").show();
            requestAnimationFrame(player.step.bind(player));
          },
          onload: function() { song_elem.find(".song-timer").html(ns._formatTime(this.duration())); },
          onend: function() {
            song_elem.find(".song-timer").html(ns._formatTime(this.duration()));
            song_elem.find(".song-progress").css("width", "0%");
            song_elem.find(".song-title").html(song.title + "  ");
            song_elem.find(".fa-pause").hide(); song_elem.find(".fa-play").show();
          },
          onpause: function() { song_elem.find(".fa-pause").hide(); song_elem.find(".fa-play").show(); },
          onstop: function() {
            song_elem.find(".song-timer").html(ns._formatTime(this.duration()));
            song_elem.find(".song-progress").css("width", "0%");
            song_elem.find(".song-title").html(song.title + "  ");
            song_elem.find(".fa-pause").hide(); song_elem.find(".fa-play").show();
          }
        });
      },
      _bindPlayerControls: function(player, elem, idx) {
        elem.find(".fa-play").click(function() { player.toggleTo(idx); });
        elem.find(".fa-pause").click(function() { player.pause(idx); });
        elem.find(".fa-stop").click(function() { player.stop(idx); });
        elem.find(".fa-volume-up").click(function() { elem.find(".song-volume-control").show(); });
        elem.find(".fa-times").click(function() { elem.find(".song-volume-control").hide(); });
        elem.find(".song-volume-bar#fgg").click(function(event) {
          var x = event.pageX - elem.find(".song-volume-bar#bg").offset().left - 7.5;
          player.volume(x / parseFloat(elem.find(".song-volume-bar#bg").innerWidth()));
        });
        elem.find(".song-volume-dot").mousedown(function() { player._mouse_down = true; });
        elem.find(".song-volume-control").mouseup(function() { player._mouse_down = false; });
        elem.find(".song-volume-control").mousemove(function(event) {
          if (player._mouse_down) {
            var x = event.pageX - elem.find(".song-volume-bar#bg").offset().left - 7.5;
            player.volume(Math.min(1, Math.max(0, x / parseFloat(elem.find(".song-volume-bar#bg").innerWidth()))));
          }
        });
        var _seekPct = function(event) {
          var x = event.pageX - elem.find(".song-seek").offset().left;
          return Math.min(1, Math.max(0, x / parseFloat(elem.find(".song-seek").innerWidth())));
        };
        elem.find(".song-seek, .song-progress").mousedown(function(event) {
          player._seeking = true; player.updateDuration(idx, _seekPct(event));
        }).mousemove(function(event) {
          if (player._seeking) player.updateDuration(idx, _seekPct(event));
        }).mouseup(function(event) {
          player._seeking = false; player.seek(idx, _seekPct(event));
        });
      },
      _formatTime: function(secs) {
        var hours = Math.floor(secs / 3600) || 0;
        var minutes = Math.floor((secs - hours * 3600) / 60) || 0;
        var seconds = Math.floor(secs - minutes * 60) || 0;
        return hours > 0
          ? hours + ":" + (minutes < 10 ? "0" : "") + minutes + ":" + (seconds < 10 ? "0" : "") + seconds
          : minutes + ":" + (seconds < 10 ? "0" : "") + seconds;
      }
    }
  };
})();
</script>

