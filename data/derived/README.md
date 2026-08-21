# DOI-preserved derived data

Place the final numerical data behind every manuscript and supporting figure in
this directory. Prefer NetCDF for time-dependent or multidimensional arrays and
CSV for compact relations and parameter tables.

Each NetCDF variable must have `long_name`, `units`, `coordinate_system`, and
`source_files` attributes. Each file must have global attributes for title,
authors, event interval, software version, creation date, and processing
history. CSV units must appear in column names or a companion metadata file.

Do not deposit only PNG/PDF figures. A reader must be able to recover the
plotted numerical values.

