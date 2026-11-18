# ⚡ ELE 211L Lab Simulator

A browser-based simulator of the **NI ELVIS II+** workstation for practising the ELE 211L (Electric Circuits I) lab final at the American University of Sharjah: DC measurements, Thevenin equivalents, RC transients and AC steady state.

**[▶ Open the live simulator](https://claude.ai/artifact/Dd5CHjZdx84pdsnEH9Ccrs)**. You can also download `index.html` and open it in any browser. It's a single file with no build step.

![Lab bench view](preview.png)

## Features

- **3D ELVIS II+ bench.** A prototyping board with vertical breadboard strips, power rails, header pins (+15V, −15V, GROUND, +5V, FGEN), scope BNCs, DMM banana jacks and a working power switch with a click sound.
- **Real wiring.** Drag jumper wires between holes, place parts from the component drawer and move each lead. The DMM leads and scope clips plug in like the real ones, and the red plug moves between VΩ and A.
- **Circuit solver.** A nodal (MNA) solver for DC, plus a backward-Euler transient solver with an adaptive time step for the capacitor circuits.
- **Realistic faults.** Supply shorts, an ammeter across a source, the ohmmeter used on a powered circuit, and a scope ground clip that grounds a node.
- **Computer screen tab.** Mock NI ELVISmx panels for the DMM (V⎓, V~, A⎓, A~, Ω), the function generator (sine, square, triangle) and the oscilloscope (Immediate/Edge trigger, slope, cursors, autoscale, RMS / Vp-p readouts).
- **Lab sheet.** The schematic, step-by-step procedure, and a worksheet that checks your measured values within 3%.
- **Check circuit.** Compares your breadboard wiring with the schematic and tells you which part is misplaced.

## Verified against theory

| Quantity | Simulator | Hand calculation |
|---|---|---|
| V1 | 6.928 V | 6.928 V |
| Voc / Isc / Rth | 9.866 V / 23.83 mA / 413.9 Ω | same |
| τ = Rth·C | 0.414 ms | 0.414 ms |
| Vc at 1 kHz | 2.36 Vpp, −69° | same |

Built with plain HTML, SVG, Canvas and JavaScript (no frameworks). Vibe-coded with Claude.
