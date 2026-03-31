# CEMIA

**Coupled Electron Microscopy and Image Analysis**

## Overview

CEMIA is an open-source Python program for correlative electron microscopy analysis. It combines SEM imaging with Electron Backscatter Diffraction (EBSD) orientation mapping to enable image registration, phase correlation, and quantitative analysis of precipitate interactions with particles, grain boundaries, and subgrain boundaries.

CEMIA is described in the following publication:  
https://doi.org/10.1016/j.matchar.2026.116328

## Main features

- Correlative SEM–EBSD analysis
- Projective and Thin Plate Spline (TPS) registration
- Quantification of heterogeneous nucleation at second-phase particles
- Quantification of heterogeneous nucleation at grain boundaries and subgrain boundaries
- Particle statistics including size, number density, and area fraction
- Zener pinning analysis based on segmented particle distributions
- GUI-based workflow for practical microstructure analysis

## Repository structure

```text
CEMIA/
├── CEMIA.py                # Main startup script
├── EBSD_BSE.py             # Coupled EBSD–BSE workflow
├── BSE.py                  # BSE-only workflow
├── Crystallography/        # Custom crystallographic libraries and data
├── requirements.txt        # Python dependencies
├── Documentation/          # Detailed user documentation
└── README.md               # Project overview
```

## Requirements

CEMIA is written in Python and relies on the packages listed in `requirements.txt`, including:

- `numpy`
- `scipy`
- `pandas`
- `seaborn`
- `matplotlib`
- `pillow`
- `tkinter-tooltip`
- `imageio`
- `scikit-image`
- `openpyxl`


## Installation

It is recommended to create a dedicated Python virtual environment before installation.

- Create a virtual environment
`python -m venv venv`

- Activate the virtual environment

(a) Windows (PowerShell)
`.\venv\Scripts\activate`

If you see an error such as “running scripts is disabled”, run:

`Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass`

Then activate the environment again.

(b) macOS / Linux
`source venv/bin/activate`

- Install dependencies

With the virtual environment activated, run:

`pip install -r requirements.txt`

## Input data

Depending on the selected workflow, CEMIA uses the following inputs:

- EBSD maps in .ctf format
- BSE images in .tif or .png format
- phase segmentation output from Ilastik as a NumPy array

## Outputs

CEMIA generates project-specific output folders and can provide:

- registered EBSD/BSE datasets
- processed images and overlays
- particle statistics
- heterogeneous nucleation statistics
- boundary-related statistics
- exported quantitative results for downstream analysis
- Zener pinning analysis


## Documentation

Detailed user documentation is available in the Documentation/ folder.

Please refer to the documentation for:

- installation details
- supported workflows
- input preparation
- segmentation guidance
- registration workflow
- output interpretation
- troubleshooting

## Citation

If you use CEMIA in your research, please cite:

Moosavi, S.E., Cayron, C., Jing, Y., Liang, Z., Cantergiani, E., Aron, L., Friedli, J., Logé, R.
Quantitative correlative SEM–EBSD analysis of precipitate–particle and precipitate–boundary interactions in Al-Mg-Si alloys.
Materials Characterization 235 (2026) 116328.
https://doi.org/10.1016/j.matchar.2026.116328

## License

This project is released under the MIT License.

## Developers

Initial framework, Tk menu, CTF reading, and canvas components were developed by C. Cayron (August–November 2023), with further development by S.E. Moosavi (2024–2025).

## Development status

CEMIA is an ongoing development, and we are glad to receive feedback, suggestions, and ideas for further improvement.

## Contact

For questions, feedback, or collaboration, please contact: ezzatollah.moosavi@epfl.ch
