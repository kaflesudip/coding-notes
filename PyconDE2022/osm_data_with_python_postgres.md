# Processing Open Street Map Data with Python and PostgreSQL

- Author: Travis Hathway
- Talk page: https://2022.pycon.de/program/AKCLEP/
- Blog about the talk: https://travishathaway.com/posts/2022-04-02-processing-osm-data-with-postgresql-and-python/ 



## Topics

- What is OSM?
- How to use OSM with Posgres / postGIS?
- How to structure a Python project for these use cases?



## OSM

- Huge community
- Contribued by:
  - Individual
  - organizations
  - Government

### Data types:

1. Node --> Point
2. Ways --> Collection of points. e.g. street, river
3. Closed ways
4. areas --> parks
5. Relations --> Lakes with island

### Tagging features

- Community has some standards of tagging
- e.g of tags Cinema, restaurant etc.

### OSM Mirrors

- Most common geofabrik mirror

### Formats in OSM:

- Supports multiple formats for exporting
- Preferred: Protocolbuffer Binary Format (PBF)



## OSM with Postgres:

- PostGIS: Postgres extension for GIS
- Data type --> Geometry which can be classified into
  1. Point  [OSM Nodes]
  2. LineString   [Ways, Open Ways]
  3. Polygon [Closed ways, relations]
  4. Geometry Collection  [Closed ways, relations]
     1. Multipoint
     2. Multiline
     3. Multipolygon

- Check PostGis tutorial for Geospatial queries.

## How to get data to database:

1. OSmimum
2. OSM2psql
   1. Can use Lua scripts

## Structure of Python project

![img](https://travishathaway.com/posts/2022-04-02-processing-osm-data-with-postgresql-and-python/img/data-pipeline.png)



**Summary:**

```mermaid
graph LR
Download --> Extract --> Import --> Report

```