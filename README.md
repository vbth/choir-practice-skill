# Choir Practice Skill

<p><picture><source media="(prefers-color-scheme: dark)" srcset="https://choir-practice-skill.pages.dev/img/header-dark.png"><img src="https://choir-practice-skill.pages.dev/img/header.png" alt="A man with headphones stands in an old bathtub and sings from a sheet of music, a rubber duck floats beside him" width="100%"></picture></p>

This repository only holds the downloads (releases) of the Choir Practice Skill: the `.skill` file and the example packs.

## Individual scores. For every voice. To listen and practise.

This project documents an AI music workflow and skill. Given a **choir score** (PDF, scan, photo or export from notation software), the skill produces one ZIP with **scores and MP3 recordings for every voice**: in three stages (solo, with accompaniment, in the choir) and in choir and piano sound. The AI agent transcribes the score, proofreads it twice and checks the audio technically. Everything is marked as created with AI assistance.

It is a private code experiment and a proof of concept for the shift from software as a service (SaaS) to result as a service (RaaS).

### What comes out

One ZIP with
- practice audio (MP3) and MIDI per voice: solo, with accompaniment, in the choir, plus tutti; in choir and piano sound; normal and slowed down
- tags in every MP3 and one album cover per piece, the same for all voices
- one ready-made ZIP per voice, a guide for the choir director, a check log and a correction log
- a start page (`Start.html`) that works with a double click, no server needed

### Start

1. Download `choir-practice.skill` from the latest release in the Releases section of this page.
2. Add it to Claude: upload it as a skill or, in Claude Code, unzip it into `~/.claude/skills/`.
3. Call the skill and attach the score (PDF, photo, scan or export).
4. Answer the questions: rights first, then title, melody voice, seating, tempo and layouts.
5. Download the finished ZIP, unzip it and open `Start.html`.

### Requirements

Python with the packages the skill lists, FluidSynth, ffmpeg, poppler and a soundfont (MuseScore General, or GeneralUser GS 2.0.3 beta by S. Christian Collins under its own licence). At the start the skill checks the installation and asks before it installs anything.

### Rights

The skill gives no legal advice and grants no rights. It asks whether the score is public domain, licensed, the user's own work or unclear, and notes the answer in the README of the package. The licence of the skill says nothing about the rights to the score.

### Limits

- The AI agent does not hear the audio; it is tested technically (duration against the MIDI, gaps, clipping, loudness, stereo).
- Accidentals, rhythm and signs are read from image crops and proofread twice, not measured. Spot-check real pieces.
- DIN A4 only.

### AI marking

Everything the skill creates is marked as created with AI assistance: the EU label "AI" and the note "Created with AI assistance." in the footer of every PDF and in the metadata of MP3, MIDI, MusicXML and PDF. The music itself does not come from the AI: the notes follow the source, the sound is software synthesis.

### Licence

PolyForm Noncommercial License 1.0.0, full text in `LICENSE.md`. Third-party components and their licences: `THIRD_PARTY_NOTICES.md`.

<picture><source media="(prefers-color-scheme: dark)" srcset="https://choir-practice-skill.pages.dev/img/ai-basic-dark.svg"><img src="https://choir-practice-skill.pages.dev/img/ai-basic.svg" alt="AI" height="18" align="absmiddle"></picture> 2026 Created with AI assistance.
