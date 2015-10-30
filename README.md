# Hong Kong <br>District Council Election 2015 <br>JSON Collection
[**Download the Latest Release here**](https://github.com/UnKnoWn-Consortium/DC2015_JSON/releases/latest)

**Updated 30OCT2015:** <br>Updated with Gazette Extraordinary published on Monday, 26/10/2015, No. 40 Vol. 19

**Updated 24OCT2015:** <br>GeoJSON version is available now! Please check the latest release.

This repository is a collection of JSONs (plus relevant materials) for Hong Kong District Council Election 2015.

There are **THREE** versions avaiable: `districts.full.json`, `districts.json`, and `geojson.json`

1. `districts.full.json` is the full version; <br>
2. `districts.json` contains all fields in the full version except `GeoJSON` fields in districts and constituents; and <br>
3. `geojson.json` is a digestible GeoJSON of type `FeatureCollection` with GeoJSON objects of districts and constituents as `features` and respective district and constituent properties other than `GeoJSON` encompassed as `properties` in the respective GeoJSON object. 

Logos for the 18 district councils can be found in `dc_logo`. All are formatted to 350px sqaure png with transparent background. 

# Source and Reference

The Government of Hong Kong Gazette: <br>http://www.gld.gov.hk/egazette/english/gazette/volume.php?extra=1&year=2015&month=10&day=26&vol=19&no=40&gn=&type=0

District Info, Constituent Info, and Candidate Info: <br>http://www.elections.gov.hk/dc2015/chi/index.html <br>http://www.elections.gov.hk/dc2015/eng/index.html

District Council Election 2015 Constituent Boundary GeoJSON: <br>https://github.com/alanho/dc2015

Hong Kong District Council Boundary: <br>
GADM database of Global Administrative Areas ver. 2.7: <br>
http://www.gadm.org/
<br>P.S. The shapefile for these district council boundaries is based on District Council Election 2011, and thus outdated.

# Schema

`districts.full.json`
```
[{
    "region": (String) Hong-Kong-Island/Kowloon/New-Territories, 
    "ename": (String) English name of the district, 
    "cname": (String) Chinese name of the district, 
    "population": (Number) Projected Population as at 30 June 2015,
    "electors": (Number) Number of Electors in the 2015 Final Register,
    "iconSrc": (String) Icon link of the respective District Council,
    "exOfficio": (Number) Ex Officio seats,
    "GeoJSON": (GeoJSON Object),
    "seats": [
        {
            "type": (String) constutuent/exofficio,
            "cacode": (String) Constituent code,
            "cname": (String) Chinese name of the constituent,
            "ename": (String) English name of the constituent,
            "population": (Number) Projected Population as at 30 June 2015,
            "electors": (Number) Number of Electors in the 2015 Final Register,
            "GeoJSON": (GeoJSON Object),
            "finalized": (Boolean) ,
            "candidates": [
                {
                    "number": (Number) Candidate number,
                    "cname": (String) Chinese name of the candidate,
                    "ename": (String) English name of the candidate,
                    "sex": (String) Sex of the candidate,
                    "cAlias": (String) Chinese alias of the candidate,
                    "eAlias": (String) English alias of the candidate,
                    "cOccupation": [(String) Declared occupation in Chinese],
                    "eOccupation": [(String) Declared occupation in English],
                    "cAffiliation": [(String) Delcared political affliation in Chinese],
                    "eAffiliation": [(String) Delcared political affliation in English],
                    "vote": (Integer) Vote received,
                    "win": (Boolean) whether win or not
                }
            ]
        }
    ]
}]
```

`districts.json`
```
[{
    "region": (String) Hong-Kong-Island/Kowloon/New-Territories, 
    "ename": (String) English name of the district, 
    "cname": (String) Chinese name of the district, 
    "population": (Integer) Projected Population as at 30 June 2015,
    "electors": (Integer) Number of Electors in the 2015 Final Register,
    "iconSrc": (String) Icon link of the respective District Council,
    "exOfficio": (Integer) Number of Ex Officio seats,
    "seats": [
        {
            "type": (String) constutuent/exofficio,
            "cacode": (String) Constituent code,
            "cname": (String) Chinese name of the constituent,
            "ename": (String) English name of the constituent,
            "population": (Integer) Projected Population as at 30 June 2015,
            "electors": (Number) Number of Electors in the 2015 Final Register,
            "finalized": (Boolean) Whether the result has been finalized,
            "candidates": [
                {
                    "number": (Number) Candidate number,
                    "cname": (String) Chinese name of the candidate,
                    "ename": (String) English name of the candidate,
                    "sex": (String) Sex of the candidate,
                    "cAlias": (String) Chinese alias of the candidate,
                    "eAlias": (String) English alias of the candidate,
                    "cOccupation": [(String) Declared occupation in Chinese],
                    "eOccupation": [(String) Declared occupation in English],
                    "cAffiliation": [(String) Delcared political affliation in Chinese],
                    "eAffiliation": [(String) Delcared political affliation in English],
                    "vote": (Integer) Vote received,
                    "win": (Boolean) whether win or not
                }
            ]
        }
    ]
}]
```

`geojson.json`
```
[{ // District
    "type": "FeatureCollection",
    "crs": {"type": "name", "properties": {"name": "urn:ogc:def:crs:OGC:1.3:CRS84"}},
    "features": [{
        "type": "Feature", 
        "properties": {
            "region": (String) Hong-Kong-Island/Kowloon/New-Territories, 
            "ename": (String) English name of the district, 
            "cname": (String) Chinese name of the district, 
            "population": (Integer) Projected Population as at 30 June 2015, 
            "electors": (Integer) Number of Electors in the 2015 Final Register, 
            "iconSrc": (String) Icon link of the respective District Council,
            "seats": (Integer) Number of seats in the District Council, 
            "exOfficio": (Integer) Number of ex officio members in the District Council
        }, 
        "geometry": {
            "type": (String) GeometryCollection/Polygon,
            "geometries": [Coordinate Pairs]
        }
}, 
{ // Constituent
    "type": "FeatureCollection",
    "crs": {"type": "name", "properties": {"name": "urn:ogc:def:crs:OGC:1.3:CRS84"}},
    "features": [{
        "type": "Feature", 
        "properties": {
            type: (String) constituent
            cacode:(String) Constituent code, 
            "cname": (String) Chinese name of the constituent,
            "ename": (String) English name of the constituent,
            "population": (Integer) Projected Population as at 30 June 2015,
            "electors": (Number) Number of Electors in the 2015 Final Register,
            "finalized": (Boolean) Whether the result has been finalized,
            candidates: [
                {
                    "number": (Number) Candidate number,
                    "cname": (String) Chinese name of the candidate,
                    "ename": (String) English name of the candidate,
                    "sex": (String) Sex of the candidate,
                    "cAlias": (String) Chinese alias of the candidate,
                    "eAlias": (String) English alias of the candidate,
                    "cOccupation": [(String) Declared occupation in Chinese],
                    "eOccupation": [(String) Declared occupation in English],
                    "cAffiliation": [(String) Delcared political affliation in Chinese],
                    "eAffiliation": [(String) Delcared political affliation in English],
                    "vote": (Integer) Vote received,
                    "win": (Boolean) whether win or not
                }
            ]
        }, 
        "geometry": {
            "type": (String) GeometryCollection/Polygon,
            "geometries": [Coordinate Pairs]
        }
}]
```
