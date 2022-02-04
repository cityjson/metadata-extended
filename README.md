
# MetadataExtended

CityJSON Extension to store ISO19115-compliant metadata, extends the few metadata properties of the core.
Works with CityJSON v1.1+

The CityJSON v1.1 core `"metadata"` has only those 6 properties allowed:

  - geographicalExtent
  - identifier
  - pointOfContact
  - referenceDate
  - referenceSystem
  - title

and the MetadataExtended Extension adds several ISO19115-compliant properties, see the paper [A metadata ADE for CityGML](http://dx.doi.org/10.1186/s40965-018-0057-4) for more details and justifications.


```json
  {
    "type": "CityJSON",
    "version": "1.1",
    "extensions":
    {
        "Metadata-Extended":
        {
            "url": "https://raw.githubusercontent.com/cityjson/metadata-extended/0.6/metadata-extended.ext.json",
            "version": "0.6"
        }        
    },
    "metadata":
    {
      "geographicalExtent": [ 84710.1, 446846.0, -5.3, 84757.1, 446944.0, 40.9 ],
      "identifier": "eaeceeaa-3f66-429a-b81d-bbc6140b8c1c",
      "pointOfContact": {
        "contactName": "3D geoinformation group, Delft University of Technology",
        "contactType": "organization",
        "role": "owner",
        "phone": "+31-6666666666",
        "emailAddress": "3dgeoinfo-bk@tudelft.nl",
        "website": "https://3d.bk.tudelft.nl",
        "address": "Julianalaan 134, Delft 2628BL, the Netherlands"
      },
      "referenceDate": "1977-02-28",
      "referenceSystem": "https://www.opengis.net/def/crs/EPSG/0/2355",
      "title": "Buildings in LoD2.3 of Chibougamau, Québec"
    },
    "+metadata-extended": {
        "isTriangulated": false,
        "metadataDateStamp": "2021-07-12",
        "datasetTopicCategory": "geoscientificInformation",
        "spatialRepresentationType": "vector",
        "fileIdentifier": "delft.json",
        "metadataStandard": "ISO 19115 - Geographic Information - Metadata",
        "metadataStandardVersion": "ISO 19115:2014(E)",
        "metadataCharacterSet": "UTF-8",
        "datasetCharacterSet": "UTF-8",
        "textures": "absent",
        "materials": "absent"
    },
    "CityObjects": {},
    "vertices": []
  }
```
