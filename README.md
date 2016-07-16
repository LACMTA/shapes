# shapes

The GEOJSON files in this repository were created from [Metro's GIS](http://developer.metro.net/introduction/gis-data/download-gis-data/) files using this command:

```
find . -name "*.shp" \
	-exec ogr2ogr \
	-skipfailures \
	-f GeoJSON \
	-t_srs crs:84 {}.geojson {}  \;
```

