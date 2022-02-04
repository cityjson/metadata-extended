
# MetadataExtended

CityJSON Extension to store ISO19115-compliant metadata, extends the few metadata properties of the core.
Works with CityJSON v1.1+ only.

The CityJSON v1.1 core `"metadata"` has only those 6 properties ([see specifications for more details](https://www.cityjson.org/specs/#metadata):

  - geographicalExtent
  - identifier
  - pointOfContact
  - referenceDate
  - referenceSystem
  - title

and the MetadataExtended Extension adds several ISO19115-compliant properties, those are documented in the paper [A metadata ADE for CityGML](http://dx.doi.org/10.1186/s40965-018-0057-4).


## Integrated in cjio 

The easiest way to use the MetadataExtended is by using the [software cjio](https://github.com/cityjson/cjio).
Those 4 operators are related:

```bash
metadata_create   Add the +metadata-extended properties.
metadata_get      Shows the metadata and +metadata-extended of this dataset.
metadata_remove   Remove the +metadata-extended properties.
metadata_update   Update the +metadata-extended.
```

and most operators (eg `subset`, `lod_filter`, etc.) will update the `"+metadata-extended"` property.

If the `"+metadata-extended"` is not present in the file, then nothing will be done. 
But if it is present then it'll be automatically updated.

To start use the `"+metadata-extended"`:

```bash
cjio myfile.city.json metadata_create save myfile.city.json
```

To remove the `"+metadata-extended"` property (but keep `"metadata"`):

```bash
cjio myfile.city.json metadata_remove save myfile.city.json
```


## Example of a CityJSON file using the +metadata-extended

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
