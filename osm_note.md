## method for updating openstreetmap data:
- `osmupdate` can get the differences between the old osm file and the new osm file.
- `osmconvert` can find the differences between two osm files. (this should be checked later.)
  - need to pay attention to the memory size.


## method for extracting data from openstreet map:
##### osmosis: currently the most easy tool for extracting
- method for getting one kind of data:
```
osmosis.bat --read-pbf japan.pbf --tf accept-ways amenity=* --tf reject-relations --used-node  --write-xml japan.osm
```

**the command parameter completeWays seems to extract not only the ways but also the relations.**

Memo:
A difficult problem is that for relation data, there are multiple polygons.

### Several python packages for overpass api of openstreetmap:
1. [overpass](https://pypi.org/project/overpass/): overpass api is current most useful to query the geojson type.
install: `pip install overpass`
2. [overpy](https://pypi.org/project/overpy/): seems to be more official(?), more functional but seems cannot get the geojson type directly.
3. [osmnx](https://github.com/gboeing/osmnx): currently the best tool for extracting road network from openstreetmap.


### osm data editing:
Browser editing:

Script editing:
[osmapi](http://osmapi.metaodi.ch/#osmapi.OsmApi.OsmApi.WayCreate)
