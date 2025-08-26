# xyp-to-cp-sd-using-python-code-from-fluent-data
Post-processing tool for ANSYS Fluent simulations. Extracts X, Y, P at Z=0 plane, arranges coordinates in continuous order, and computes Cp vs S/D for surface analysis.
This repository provides a post-processing pipeline for ANSYS Fluent simulations of projectile bodies.

Input: Requires .cas.h5 and .dat.h5 files from Fluent.

Step 1 (Extraction): Automatically extracts X, Y coordinates and pressure (P) values at the Z=0 plane from the CFD results.

Step 2 (Arranging): Raw XYP data is often random (non-continuous surface order). The script arranges points in a continuous sequence from the front stagnation point to the back of the body.

Step 3 (Calculation): Using projectile diameter, velocity, and reference density:

Converts arc length into normalized surface distance S/D.

Converts pressure into pressure coefficient Cp.

Outputs a ready-to-use Excel file for Cp vs S/D plots.

This workflow ensures consistent, automated processing of Fluent data, making it easier to analyze surface pressure distributions around projectile-like bodies.
