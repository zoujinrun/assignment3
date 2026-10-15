http://localhost:8000

python3 -m http.server 8000
```markdown
# Process, Iterations, and Reflection

## 1. Project Overview & Evolution
The core goal of Assignment 3 was to design an interactive, web-based audio experiment with a complete Input-Response-Feedback loop. Over the course of development, the project evolved through **four distinct iterations**—transforming from a simple single-line melody into a feature-rich, **Triple-Track Polyphonic Synthesizer with Audiovisual Synesthesia**.

---

## 2. Detailed Iteration Log

### Iteration 1: Native Single-Line Melody & Cross-Origin Fix
- **Motivation / Problem**: The initial build relied on external p5.js/audio libraries and raw AudioContext setups, which frequently triggered CORS (Cross-Origin Resource Sharing) restrictions and browser audio-security blocks (suspended AudioContext on initial load).
- **Technical Changes**:
  - Transitioned to a **single-file architecture (`index.html`)** to ensure 100% local and remote portability.
  - Implemented dynamic base64 WAV data-URI generation to bypass cross-origin asset loading entirely.
  - Added explicit user-interaction handlers (clicking the canvas) to initialize and resume audio playback safely.
- **Outcome**: A stable, single-line pitch loop that works reliably across all modern browsers (Chrome, Safari, Edge) without missing file or CORS errors.

---

### Iteration 2: Dual-Track Polyphony System (Lead + Bass)
- **Motivation / Problem**: While single-note playback worked, the auditory experience was monophonic and musically plain. It lacked harmonic depth and failed to showcase complex interaction state changes.
- **Technical Changes**:
  - Expanded the audio engine to synthesize two parallel audio tracks:
    1. **Track 1 (Lead)**: High-pitched Sine Wave ($C_4 - C_5$).
    2. **Track 2 (Bass)**: Low-pitched Triangle Wave ($C_3 - C_4$, an octave lower).
  - Designed interactive UI controls, including a dedicated `Toggle Bass Track` button allowing users to mute/unmute the bass line dynamically during playback.
  - Rendered vertical harmony connection lines on Canvas to visually bridge active lead and bass nodes.
- **Outcome**: Created a richer polyphonic soundscape and allowed users to hear and see the immediate contrast between monophonic and polyphonic modes.

---

### Iteration 3: Audiovisual Synesthesia (Frequency-Synced Node Vibration)
- **Motivation / Problem**: In Iteration 2, canvas nodes were visually static on the Y-axis until active. The user interface felt rigid and didn't intuitively convey the physical properties of pitch and sound frequency.
- **Technical Changes**:
  - Developed a physics-based visual motion algorithm driven by harmonic oscillator formulas ($\sin(\text{time} \times \text{freq})$).
  - Bound vertical node vibration speeds directly to each note's actual Hz frequency:
    - **High-frequency notes (Lead)**: Vibrate rapidly with subtle horizontal jitter.
    - **Low-frequency notes (Bass)**: Sway smoothly and slowly.
- **Outcome**: Achieved **Audiovisual Synesthesia**, giving users an intuitive visual indicator of pitch height and waveform frequency even before notes are triggered.

---

### Iteration 4: Triple-Track Multi-Waveform Polyphonic Synthesizer (Final Build)
- **Motivation / Problem**: To further maximize expressive potential, I wanted to provide full multi-timbre control (Lead, Bass, Arp/Harmony) and allow users total freedom over track combinations.
- **Technical Changes**:
  - Added **Track 3 (Arpeggio/Harmony)** using a sharp **Sawtooth Wave** in the mid-high register ($E_4 - E_5$).
  - Provided **3 independent track toggle buttons (`Track 1`, `Track 2`, `Track 3`)**, enabling $2^3 = 8$ possible track mix combinations (from solo lines to full 3-part synth ensemble).
  - Differentiated track geometry and colors on Canvas:
    - **Track 1 (Lead)**: Blue/Red Circles (Fast jitter).
    - **Track 2 (Bass)**: Yellow/Green Squares (Slow sway).
    - **Track 3 (Arp)**: Purple Diamonds (Horizontal oscillation).
- **Outcome**: Delivered a highly polished, interactive synth experience with rich visual diversity, total user agency over arrangement, and zero external dependency friction.

---

## 3. Reflection on AI Tools Used
- **AI Tool**: AI Assistant (ChatGPT / Gemini).
- **Key Contributions**:
  - Assisted in designing the zero-dependency, multi-waveform WAV Data-URI generator.
  - Formulated the mathematical equations for frequency-scaled sinusoidal node vibration.
  - Guided cross-browser audio security troubleshooting (Safari AudioContext autoplay rules).
- **Critical Retained vs. Rejected Suggestions**:
  - *Retained*: Using distinct geometric shapes (circles, squares, diamonds) and frequency-scaled physics to convey timbre and pitch.
  - *Rejected*: AI initially suggested introducing external audio sample files and complex UI frameworks. I rejected these to maintain a clean, single-file lightweight architecture that guarantees instant loading without missing assets.