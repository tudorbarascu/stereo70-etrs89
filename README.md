Romania stereo70 to etrs89 and back
===================================

This repo should describe how to properly use proj4 with the official Romanian projection.


- The ``verification_points`` directory holds some shapefiles with points in stereo70 and
their correspondent in WGS84.

- The ``grids/stereo70_etrs89A.gsb`` file is a standard binary shift grid (https://en.wikipedia.org/wiki/NTv2)
 for Romania, build by Daniel Urdă (see. https://github.com/danieluct/ntv2generator)
