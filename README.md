# Hong Kong <br>District Council Election 2015 <br>JSON Collection
This repository is a collection of JSONs (plus relevant materials) for Hong Kong District Council Election 2015.

There are **two** versions avaiable: `districts.full.json` and `districts.json`

`districts.full.json` is the full version; and <br>
`districts.json` contains all fields in the full version except GeoJSON

A pure GeoJSON version will be added later. 

Logos for the 18 district councils can be found in `dc_logo`. All are formatted to 350px sqaure png with transparent background. 

# Source and Reference

District Info, Constituent Info, and Candidate Info: <br>http://www.elections.gov.hk/dc2015/chi/index.html <br>http://www.elections.gov.hk/dc2015/eng/index.html

District Council Election 2015 Constituent Boundary GeoJSON: <br>https://github.com/alanho/dc2015

Hong Kong District Council Boundary: <br>
GADM database of Global Administrative Areas ver. 2.7: <br>
http://www.gadm.org/

P.S. The shapefile for these district council boundaries is based on District Council Election 2011, and thus outdated.

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
                    "gender": (String),
                    "cAlias": (String),
                    "eAlias": (String),
                    "cOccupation": [(String)],
                    "eOccupation": [(String)],
                    "cAffiliation": [(String) Delcared political affliation in Chinese],
                    "eAffiliation": [(String) Delcared political affliation in English],
                    "vote": (Number),
                    "win": (Boolean)
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
    "population": (Number) Projected Population as at 30 June 2015,
    "electors": (Number) Number of Electors in the 2015 Final Register,
    "iconSrc": (String) Icon link of the respective District Council,
    "exOfficio": (Number) Ex Officio seats,
    "seats": [
        {
            "type": (String) constutuent/exofficio,
            "cacode": (String) Constituent code,
            "cname": (String) Chinese name of the constituent,
            "ename": (String) English name of the constituent,
            "population": (Number) Projected Population as at 30 June 2015,
            "electors": (Number) Number of Electors in the 2015 Final Register,
            "finalized": (Boolean) ,
            "candidates": [
                {
                    "number": (Number) Candidate number,
                    "cname": (String) Chinese name of the candidate,
                    "ename": (String) English name of the candidate,
                    "gender": (String),
                    "cAlias": (String),
                    "eAlias": (String),
                    "cOccupation": [(String)],
                    "eOccupation": [(String)],
                    "cAffiliation": [(String) Delcared political affliation in Chinese],
                    "eAffiliation": [(String) Delcared political affliation in English],
                    "vote": (Number),
                    "win": (Boolean)
                }
            ]
        }
    ]
}]
```
