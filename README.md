# Docker image for gdal2tiles-leaflet

Generate raster image tiles for use with leaflet in docker.


	docker run --rm -v `pwd`:/data niene/gdal2tiles-leaflet -l -p raster -z 0-5 -w none /data/<image> /data/<tilesdir> 






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
