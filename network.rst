.. Put any comments here
   Be sure to indent at this level to keep it in comment.

.. role:: blue

.. role:: red

.. raw:: html

    <style> .red {color:red} </style>
    <style> .blue {color:blue} </style>
    <style> .ital {font-style:italic} </style>

<Network>         :red:`required`
==================================

      This type represents the Network layer, all station metadata is contained within this element. The official name
      of the network or other descriptive information can be included in the Description element. The Network can
      contain 0 or more Stations.

      **Example**: <Network code="IU" startDate=2016-01-27T13:00:00>

..
  Turn this line and line below into a comment
  .. csv-table:: attributes

.. csv-table:: *Network attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 10, 20

    **code**, :blue:`string`, :red:`yes`, "2-char network code", "code=IU"
    **startDate**, :blue:`dateTime`, "no", "network start date", "startDate=1988-01-01T00:00:00"
    **endDate**, :blue:`dateTime`, "no", "network end date", "endDate=1988-01-01T00:00:00"
    **sourceID**, :blue:`anyURI`, "no", "A data source identifier in URI form", "sourceID='http://some/path'"
    **restrictedStatus**, :blue:`NMTOKEN`, "no", "open, closed, partial", "restrictedStatus=open"
    **alternateCode**, :blue:`string`, "no", "A code used for display or association, alternate to the SEED-compliant code.", "alternateCode=IX"
    **historicalCode**, :blue:`string`, "no", "historical network code", "historicalCode=IX"

<Description>
--------------

   Description of the Network

   type::blue:`string`

   **Example:**
   <Description> *This is the network description* </Description>

<Identifier>
--------------

   A type to document persistent identifiers. Identifier values should be specified without a URI scheme (prefix), instead the identifer type is documented as an attribute.

   type::blue:`string`

   **Example:**
   <Identifier> *identifier* </Identifier>

.. include:: comment.rst

.. include:: dataavailability.rst

.. include:: operator.rst

<TotalNumberStations>
----------------------

<SelectedNumberStations>
-------------------------

   ::

      <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
      <FDSNStationXML xmlns="http://www.fdsn.org/xml/station/1" schemaVersion="1.1">
         <Source>IRIS-DMC</Source>
         <Module>IRIS converter | version: </Module>
         <ModuleURI>https://seiscode.iris.washington.edu/projects/stationxml-converter/wiki</ModuleURI>
         <Created>2019-12-14T23:20:56.779Z</Created>

