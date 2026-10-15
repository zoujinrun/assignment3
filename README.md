# assignment3
Interactive Melody Synthesizer

# Interactive Melody Synthesizer

An interactive, web-based melody synthesizer built using HTML5 Canvas and native Web Audio synthesis for Assignment 3.

## Idea & Intended User
This project is designed for users interested in exploring pitch, sequence loops, and visual music feedback. Users can dynamically manipulate a playing sequence and observe instant auditory and visual feedback.

## Main Interaction (Input, Response & Feedback)
- **Input**:
  - Click on the central dark canvas to toggle melody loop playback.
  - Click control buttons (`Reverse Melody`, `Pitch Up`, `Reset`) to manipulate the sequence in real-time.
- **Response**:
  - Synthesizes dynamic pitch audio using audio nodes.
  - Updates note sequence array order and pitch octaves instantly.
- **Feedback**:
  - **Visual**: Real-time canvas rendering highlighting active steps with animated note indicators.
  - **Auditory**: Immediate pitch and melody structure feedback.
  - **Text**: Dynamic status bar displaying playback status and mode toggles.

## How to Run
1. Ensure Python 3 is installed.
2. Clone this repository locally.
3. Open terminal in the directory and run:
   ```bash
   python3 -m http.server 8000