Romania stereo70 to etrs89 and back
===================================

This repo should describe how to properly use proj4 with the official Romanian projection.


- The ``verification_points`` directory holds some shapefiles with points in stereo70 and
their correspondent in WGS84.

- The ``grids/stereo70_etrs89A.gsb`` file is a [standard binary shift grid](https://en.wikipedia.org/wiki/NTv2)
 for Romania, provided and created by [Daniel Urdă](https://github.com/danieluct/ntv2generator)

Usage
-----

**Transform from Stereo70 to ETRS89/WGS84**

``cs2cs +proj=latlong +datum=WGS84 +to +proj=sterea +lat_0=46 +lon_0=25 +k=0.99975 +x_0=500000 +y_0=500000 +ellps=krass +nadgrids=stereo70_etrs89A.gsb +units=m +no_defs -f %.8f -I /usr/share/proj/coordinates.txt``


**Transform from ETRS89/WGS84 to Stereo70**

``cs2cs +proj=latlong +datum=WGS84 +to +proj=sterea +lat_0=46 +lon_0=25 +k=0.99975 +x_0=500000 +y_0=500000 +ellps=krass +nadgrids=./stereo70_etrs89A.gsb +units=m +no_defs -f %.8f coordinates.txt``
