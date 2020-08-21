# The DHuS Addon for CryoSat-2

## Introduction.

The DHuS addon is a Java package that contains the definitions and extraction rules and operations for the CryoSat-2 products. The central element of this package is the ontology definition file ([cryosat-2.owl](src/main/resources/META-INF/cryosat-2.owl)) located in the META-INF folder inside the resources directory.

The addon works in conjunction with the DRBX cortex definition (separate package), currently designed to support the following product types from the CryoSat-2 satellite mission:

- SIR\_FDM\_2\_
- SIR\_GOPM\_2
- SIR\_SAR\_2\_
- SIR\_GOPR\_2
- SIR\_LRM\_2\_
- SIR\_GOP\_2\_
- SIR\_SIN\_2\_
- SIR\_GDR\_2\_
- SIR\_GOPN\_2

## Metadata Attributes

All metadata that will be extracted and made available via DHuS is defined within the OWL file mentioned above. The following is a complete list of metadata attributes implemented with this addon. Sample outputs to demonstrate which values these attributes can take can be found in the [samples](src/main/resources/samples) folder inside the resources directory.

| OData Name                   | OpenSearch Name            | Description                                                                          | SIR\_FDM\_2\_ | SIR\_GOPM\_2 | SIR\_SAR\_2\_ | SIR\_GOPR\_2 | SIR\_LRM\_2\_ | SIR\_GOP\_2\_ | SIR\_SIN\_2\_ | SIR\_GDR\_2\_ | SIR\_GOPN\_2 |
|------------------------------|----------------------------|--------------------------------------------------------------------------------------|---------------|--------------|---------------|--------------|---------------|---------------|---------------|---------------|--------------|
| Satellite                    | -                          | Name of the satellite                                                                | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Instrument                   | -                          | Name of the instrument                                                               | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Date                         | -                          | Same as sensing start date                                                           | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Sensing start                | beginposition              | Sensing start date                                                                   | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Sensing stop                 | endposition                | Sensing stop date                                                                    | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Footprint                    | gmlfootprint               | GML footprint                                                                        | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| JTS footprint                | footprint                  | JTS footprint                                                                        | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Platform name                | platformname               | Name of the platform                                                                 | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Platform short name          | platformshortname          | Short name of the platform                                                           | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Platform serial identifier   | platformserialidentifier   | Identification number of the platform among the mission                              | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Platform NSSDC identifier    | platformnssdcidentifier    | The National Space Science Data Center (NSSDC) identification number of the platform | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Instrument name              | instrumentname             | Name of the instrument                                                               | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Instrument short name        | instrumentshortname        | Short name of the instrument                                                         | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Orbit number                 | orbitnumber                | Absolute orbit number                                                                | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Relative orbit number        | relativeorbitnumber        | Relative orbit number                                                                | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Cycle                        | cycle                      | Number of cycles                                                                     | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Phase                        | phase                      | Mission phase                                                                        | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Orbit direction              | orbitdirection             | Direction of the orbit (ascending or descending)                                     | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Processing level             | processinglevel            | The value of the last processing                                                     | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Processor version            | processorversion           | Version number of processing software                                                | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Generation time              | -                          | Product generation date                                                              | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Processing mode              | processingmode             | Full name of processing mode or file class                                           | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Processing mode abbreviation | processingmodeabbreviation | Abbreviated name of processing mode or file class                                    | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Product type                 | producttype                | Product type designation                                                             | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Product description          | productdescription         | One line description of the file                                                     | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Size                         | size                       | File size                                                                            | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Format                       | format                     | Product format description                                                           | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |
| Filename                     | filename                   | File name                                                                            | &#9745;       | &#9745;      | &#9745;       | &#9745;      | &#9745;       | &#9745;       | &#9745;       | &#9745;       | &#9745;      |


More information on the source of the respective attributes can be found directly by looking at the OWL file itself.

## Footprint Extraction

In contrast to all other attributes, the footprint coordinates are extracted from the binary data file (DBL) in case of the SIR\_FDM\_2\_ product and from the netCDF file for all other products. For the SIR\_FDM\_2\_ product, the cortex topic (separate package) uses an XML schema definition file to create a tree of nodes which is then navigable within the addon OWL. This functionality is already provided for netCDF files by using the DRB netCDF extension in the topic class definition.

### Latitudes and Longitudes

The generation of the footprints is based on the following sources:

- SIR\_FDM\_2\_: Latitude and Longitude of measurement (Section 8.27 in [CryoSat Product Handbook](https://earth.esa.int/documents/10174/125272/CryoSat_Product_Handbook))
- Others: 1 Hz Latitude (lat_01) and Longitude (lon_01) (Section 3.1 in [CryoSat Ice netCDF L2 Product Format Specification](https://earth.esa.int/documents/10174/125273/CryoSat-netCDF-L2-Product-Format-Specification.pdf))

The values are provided in the unit of 1e-1 microdegrees and need to be scaled accordingly. Furthermore, longitudes need to be converted from the (0-360) range to the (-180 to 180) range.

### Geometry

The coordinates provided are the orbit coordinates. A continuous polygon having a fictional width of 1 millidegree was chosen to represent the footprint (defined by the offset variable in the OWL).

The number of points per polygon needs to be small enough for the DHuS to be able to handle it. A total number of approximately 400 points was chosen.

