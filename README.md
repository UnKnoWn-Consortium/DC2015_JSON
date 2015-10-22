# Hong Kong District Council Election 2015 JSON Collection
This repository is a collection of JSONs for Hong Kong District Council Election 2015.

There are **two** versions avaiable: `districts.full.json` and `districts.json`

`districts.full.json` is the full version; and <br>
`districts.json` contains all fields in the full version except GeoJSON

A pure GeoJSON version will be added later. 

# Schema
[{
    "region": String,
    "ename": String,
    "cname": String,
    "population": Number,
    "electors": Number,
    "iconSrc": String,
    "exOfficio": Number,
    "GeoJSON": GeoJSON,
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
