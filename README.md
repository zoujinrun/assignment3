# Triple-Track Visual Melody Synthesizer

An interactive, web-based polyphonic melody synthesizer built using HTML5 Canvas and dynamic WAV audio synthesis for Assignment 3.

## Idea & Intended User
Designed for users interested in pitch, polyphonic harmony, and audiovisual synesthesia. The synthesizer features a 3-track architecture (Lead Melody, Bass Accompaniment, and Arpeggio Harmony) with visual frequency vibration matching the physical frequency of each note.

## Main Interaction (Input, Response & Feedback)
- **Input**:
  - Click on the central dark canvas to toggle 3-track playback loop.
  - Click individual track buttons (`Track 1 Lead`, `Track 2 Bass`, `Track 3 Arp`) to freely customize track combinations (1, 2, or 3 tracks simultaneously).
  - Click control buttons (`Reverse`, `Pitch Up`, `Reset All`) to manipulate melody direction and octave.
- **Response**:
  - **Track 1 (Lead)**: Clear sine wave melody in high register.
  - **Track 2 (Bass)**: Deep triangle wave bass in low register.
  - **Track 3 (Arp)**: Bright sawtooth wave electronic harmony in mid-high register.
- **Feedback**:
  - **Visual Synesthesia**: High-pitch notes vibrate rapidly while low-pitch notes sway gently in real-time sync with their actual sound frequency. Connective vertical harmony lines link active steps.
  - **Auditory**: Layered polyphonic chords with dynamic wave blending.
  - **Text**: Dynamic status display showing current track active states.

## How to Run
1. Ensure Python 3 is installed.
2. Open terminal in the project directory and start the server:
   ```bash
   python3 -m http.server 8000