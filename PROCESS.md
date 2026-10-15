http://localhost:8000
#### 2. `PROCESS.md`
```markdown
# Process and Reflection

## Starting Idea & Design Choices
The goal was to create a self-contained interactive audio experiment with strong visual-auditory feedback loops. Starting from a single-line melody, I expanded the project into a dual-track polyphonic synthesizer to produce a richer, more engaging soundscape without external library overhead.

## User Trial & Iteration
- **Iteration 1**: Initial single-line melody felt audibly plain and lacked depth.
- **Iteration 2 (Dual-Track Upgrade)**: Added a secondary bass track (triangle wave, octave down) and vertical harmony lines connecting lead and bass notes. Added a dedicated toggle button (`Toggle Bass Track`) allowing users to compare single-track versus harmonic playback.

## AI Tools Used
- **Tool**: AI Assistant (ChatGPT/Gemini).
- **Use Case**: Assisted in structuring the dual-track Web Audio synth logic, setting up parallel audio nodes (Sine + Triangle oscillators), and drafting documentation.
- **Suggestion Retained**: Using distinct visual shapes (circles for lead, squares for bass) and vertical connection lines to clearly depict polyphonic harmony.
- **Suggestion Modified**: Originally considered sample loading for bass, but retained native synth oscillators to avoid network cross-origin issues and preserve single-file portability.