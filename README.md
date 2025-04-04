# trk2vtk
trk2vtk is a Bash script designed to convert .trk (TrackVis) files into .tck (MRtrix) and subsequently into .vtk (Visualization Toolkit) formats.

**Convert `.trk` tractography files to `.tck` and `.vtk` using DIPY and MRtrix**

This script provides a simple command-line tool to convert tractography files from the `.trk` format (commonly used by tools like TrackVis) to the `.tck` format (used by MRtrix), and finally to the `.vtk` format for visualization or further processing.

---

## 🛠 Requirements

Before using `trk2vtk.sh`, make sure you have the following dependencies installed and available in your `PATH`:

- `python3` (with the `dipy` and `nibabel` packages)
- `tckconvert` (part of the [MRtrix3](https://www.mrtrix.org/) suite)

You can install the required Python packages using:

```bash
pip install dipy nibabel
```

📦 Usage
```bash
./trk2vtk <input.trk> [output_prefix] [--force]
```

Arguments
input.trk: Path to the input .trk file.

output_prefix (optional): Prefix for the output .tck and .vtk files. Defaults to the input filename without the .trk extension.

--force: Overwrite existing output files if they already exist.

 Examples
 ```bash
./trk2vtk my_tract.trk

# Specify a custom output prefix and overwrite if needed
./trk2vtk my_tract.trk output/my_tract --force
 ```

---

📂 Output
The script will generate the following files:

<output_prefix>.tck – intermediate MRtrix tractogram

<output_prefix>.vtk – final output tractogram for visualization (e.g., in ParaView or 3D Slicer)

---

📄 License
This project is licensed under the MIT License. See the LICENSE file for details.
