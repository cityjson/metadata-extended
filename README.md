
# MetadataExtended

CityJSON Extension to store ISO19115-compliant metadata, extends the few metadata properties of the core.
Works with CityJSON v1.1+

The CityJSON v1.1 core `"metadata"` has only those 6 properties allowed:

  - citymodelIdentifier
  - datasetPointOfContact
  - datasetTitle
  - datasetReferenceDate
  - geographicalExtent
  - referenceSystem

and the MetadataExtended Extension adds several ISO19115-compliant properties, see the paper [A metadata ADE for CityGML](http://dx.doi.org/10.1186/s40965-018-0057-4) for more details and justifications.


```json
  {
    "type": "CityJSON",
    "version": "1.1",
    "CityObjects": {},
    "vertices": [],
    "extensions":
    {
        "Metadata-Extended":
        {
            "url": "https://raw.githubusercontent.com/cityjson/metadata-extended/main/metadata-extended.ext.json",
            "version": "0.5"
        }        
    },
    "metadata":
    {
      "referenceSystem": "https://www.opengis.net/def/crs/0/7415",
      "citymodelIdentifier": "eaeceeaa-3f66-429a-b81d-bbc6140b8c1c",
      "geographicalExtent":
      [
        84616.468,
        447422.999,
        -0.452,
        85140.839,
        447750.636,
        16.846
      ],
      "datasetReferenceDate": "2019-01-13"
    },
    "+metadata-extended": {
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
    }
  }
```
