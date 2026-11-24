# Small Structure Vibration Rig — Resonance & Peak Response

An interactive **Google Colab** engineering tool built with `ipywidgets`, `NumPy`, `Pandas`, and `Matplotlib` to simulate a vibration test rig for a small structure and identify the frequencies that produce the largest dynamic response.

## Overview

When a structure is excited near one of its natural frequencies, resonance amplifies its vibration response[cite: 7]. This notebook lets you configure a small test structure, sweep excitation frequency across a chosen band, visualize the 2D rig and dominant mode shape, and highlight the frequencies creating the largest response peaks.

### Supported Structures & Materials
- **Structures:** `Cantilever Beam`, `Simply Supported Beam`, `Small Frame Structure`
- **Materials:** `Aluminum 6061`, `3D-Printed PLA`, `Balsa Wood`

## Key Features

- **Interactive English UI (`ipywidgets`):** Select structure type, material, length (`L`), width (`b`), thickness (`h`), tip mass (`Tip Mass`), damping ratio (`ζ`), sweep upper bound (`Max Freq [Hz]`), and base excitation (`Base Input [g]`).
- **2D Test Rig & Mode Shape View:** Displays a schematic 2D representation of the test setup, boundary conditions, shaker/exciter location, and dominant deflection shape.
- **Frequency Response & Peak Identification:** Plots response amplitude against excitation frequency (`Hz`), marks the top resonant peaks, and lists ranked peak frequencies and amplitudes in a summary table.
- **Out-of-Band Guidance:** Reports estimated natural frequencies (`f1 / f2 / f3`) if a mode lies above the selected `Max Freq [Hz]` sweep range so you can widen the sweep band easily.

## How to Run in Google Colab

1. Open a new notebook in [Google Colab](https://colab.research.google.com/).
2. Paste the vibration test rig code into a code cell and run it.
3. Adjust the sliders and dropdowns—or click **Run Vibration Sweep**—to inspect natural frequencies and peak response behavior.

## Engineering Notes

- Natural frequencies depend on bending stiffness ($EI$), mass distribution, boundary conditions, and added/tip mass, while peak amplitude strongly reflects structural damping ($\zeta$).
- Analytical/multi-mode sweep models provide rapid insight for test planning and rig setup, and are best paired with physical shaker/impact testing or finite element modal analysis for final hardware.
