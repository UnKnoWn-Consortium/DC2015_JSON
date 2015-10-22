# Hong Kong <br>District Council Election 2015 <br>JSON Collection
This repository is a collection of JSONs for Hong Kong District Council Election 2015.

There are **two** versions avaiable: `districts.full.json` and `districts.json`

`districts.full.json` is the full version; and <br>
`districts.json` contains all fields in the full version except GeoJSON

A pure GeoJSON version will be added later. 

Logos for the 18 district councils can be found in `dc_logo`. All are formatted to 350px sqaure png with transparent background. 

# Source and Reference

District Info, Constituent Info, and Candidate Info: <br>http://www.elections.gov.hk/dc2015/chi/index.html <br>http://www.elections.gov.hk/dc2015/eng/index.html

District Council Election 2015 Constituent Boundary GeoJSON: <br>https://github.com/alanho/dc2015

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
            "type": String,
            "cacode": String,
            "cname": String,
            "ename": String,
            "population": Number,
            "electors": Number,
            "GeoJSON": GeoJSON,
            "finalized": Boolean,
            "candidates": [
                {
                    "number": Number,
                    "cname": String,
                    "ename": String,
                    "gender": String,
                    "alias": String,
                    "occupation": String,
                    "affiliation": String,
                    "vote": Number,
                    "win": Boolean
                }
            ]
        }
    ]
}]
```

`districts.json`
```
[{
    "region": String,
    "ename": String,
    "cname": String,
    "population": Number,
    "electors": Number,
    "iconSrc": String,
    "exOfficio": Number,
    "seats": [
        {
            "type": String,
            "cacode": String,
            "cname": String,
            "ename": String,
            "population": Number,
            "electors": Number,
            "finalized": Boolean,
            "candidates": [
                {
                    "number": Number,
                    "cname": String,
                    "ename": String,
                    "gender": String,
                    "alias": String,
                    "occupation": String,
                    "affiliation": String,
                    "vote": Number,
                    "win": Boolean
                }
            ]
        }
    ]
}]
```
