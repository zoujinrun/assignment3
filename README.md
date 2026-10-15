# Dual-Track Interactive Melody Synthesizer

An interactive, web-based polyphonic melody synthesizer built using HTML5 Canvas and native Web Audio synthesis for Assignment 3.

## Idea & Intended User
This project is designed for users interested in exploring pitch, polyphonic harmony, and visual music feedback. It features a dual-track architecture (Lead Melody + Bass Accompaniment) that gives users full control over spatial arrangement and harmonic layers.

## Main Interaction (Input, Response & Feedback)
- **Input**:
  - Click on the central dark canvas to toggle dual-track loop playback.
  - Click `Toggle Bass Track` to independently mute/unmute the secondary bass line.
  - Click control buttons (`Reverse Melody`, `Pitch Up`, `Reset`) to dynamically alter sequence pitch and direction.
- **Response**:
  - **Track 1 (Lead)**: Generates bright sine-wave melodic notes in high octaves.
  - **Track 2 (Bass)**: Synthesizes rich triangle-wave harmonic bass notes.
  - Updates note sequence arrays and active step pointers in real time.
- **Feedback**:
  - **Visual**: Animated canvas rendering showing high-note nodes (circles), bass nodes (squares), and vertical harmonic connecting lines glowing in sync with playback.
  - **Auditory**: Layered polyphonic audio with controllable bass presence.
  - **Text**: Real-time status bar displaying playback state and track toggles.

## How to Run
1. Ensure Python 3 is installed.
2. Clone this repository locally.
3. Open terminal in the project directory and run:
   ```bash
   python3 -m http.server 8000