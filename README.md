# sif2mat

Basic usage demonstrated below. All subdirectories of the repository should be added to the Matlab path.

Load the SIF movie into Matlab using `load_andor_kinetic`:
```
>> M = load_andor_kinetic('20160801_f4-week12-1.5x.sif');
File "20160801_f4-week12-1.5x.sif" contains 2000 frames, exposure time 0.1 sec. Loading...
```
Returned matrix `M` is `[height x width x num_frames]`.

Afterwards, the movie data can be saved into different formats, e.g. into a ImageJ-compatible TIF file:
```
>> save_movie_to_tif(M, '20160801_f4-week12-1.5x.tif');
  Frames 1000 / 2000 written to 20160801_f4-week12-1.5x.tif (15-Dec-2016 19:47:36)
  Frames 2000 / 2000 written to 20160801_f4-week12-1.5x.tif (15-Dec-2016 19:48:02)
  All done! (15-Dec-2016 19:48:02)
```
