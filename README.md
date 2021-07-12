
# MetadataExtended

CityJSON Extension to store ISO19115-compliant metadata, extends the few metadata properties of the core.

Works with CityJSON v1.1+

The v1.1 core has now only those 6 properties allowed:

  - citymodelIdentifier
  - datasetTitle
  - datasetReferenceDate
  - geographicalExtent
  - geographicLocation
  - referenceSystem

and the Extensions adds several ISO19115-compliant properties, see the paper [A metadata ADE for CityGML](http://dx.doi.org/10.1186/s40965-018-0057-4) for details.


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
            "url": "https://myurl.org/metadata-extended.ext.json",
            "version": "1.0"
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
