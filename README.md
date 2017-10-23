# Docker image for gdal2tiles-leaflet

## What is gdal2tiles-leaflet?
gdal2tiles-leaflet is developed by Commenthol See https://github.com/commenthol/gdal2tiles-leaflet

It generates raster image tiles from a given image for the use with leaflet.

This is a modified version of gdal2tiles.py which adds support for raster images as plain 2D maps in leafletjs.  It adds the option -l or --leaflet to generate the resulting images with the reference point [0,0] in the upper-left (North-West) corner, opposed to the standard behaviour for TMS tiles using the lower-left (South-East) corner.

Together with the small leafletjs plugin leaflet-rastercoords you'll be able to add markers at the correct position using the (x, y) coordinates of the full-size image.

This docker installs gdal2tiles-leaflet in a docker container so you can use docker to run the gdal2tiles-leaflet command.


## How to run as a docker command?

To run the docker gdal2tiles-leaflet command, run this command in the folder with your image. It links the current working directory to a folder called data in the docker container. Then run:

	docker run --rm -v `pwd`:/data niene/gdal2tiles-leaflet -l -p raster -z 0-5 -w none /data/<image> /data/<tilesdir> 

The --rm flag removes the docker container and its volume after it is finished executing. 


# Doccumentation from gdal2tiles-leaflet from Commenthol

See: https://github.com/commenthol/gdal2tiles-leaflet

## Contribution and License Agreement

If you contribute code to this project, you are implicitly allowing your
code to be distributed under the respective license. You are also implicitly
verifying that all code is your original work or correctly attributed
with the source of its origin and licence.

## License

Modifications and samples are [MIT licensed][LICENSE].

[gdal2tiles.py][]: (MIT licensed)
* Copyright (c) 2008, Klokan Petr Pridal
* Copyright (c) 2010-2013, Even Rouault

## References

<!-- !ref -->

* [/gdal-1.11.1/swig/python/scripts/gdal2tiles.py][gdal2tiles.py]
* [example][example]
* [gdal2tiles-Ticket-4379][gdal2tiles-Ticket-4379]
* [leaflet-rastercoords][leaflet-rastercoords]
* [leafletjs][leafletjs]
* [LICENSE][LICENSE]

<!-- ref! -->

[LICENSE]: ./LICENSE
[leafletjs]: http://leafletjs.com
[leaflet-rastercoords]: https://github.com/commenthol/leaflet-rastercoords
[gdal2tiles.py]: http://download.osgeo.org/gdal/1.11.1/gdal-1.11.1.tar.gz "/gdal-1.11.1/swig/python/scripts/gdal2tiles.py"
[gdal2tiles-Ticket-4379]: http://trac.osgeo.org/gdal/ticket/4379
[example]: https://commenthol.github.io/leaflet-rastercoords/
