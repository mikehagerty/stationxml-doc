.. Put any comments here
   Be sure to indent at this level to keep it in comment.

1. Introduction
===========================================


.. include metadata.rst::

Introducing StationXML 
----------------------

StationXML is an XML representation of metadata that describes the data collected by 
geophysical instrumentation.

-------

metadata
   - Information that describes how/where/when data was collected
   - Data that describes data

XML = eXtensible Markup Language
   - Designed to be self-descriptive
   - Commonly used to distribute data over the internet

-------

StationXML is defined by a schema that specifies the allowable format of StationXML files.

StationXML Example
^^^^^^^^^^^^^^^^^^^^^^

.. toggle-header:: 
    :header: Example of stationxml **Show/Hide Code**

    ::

      <?xml version='1.0' encoding='UTF-8'?>
         <FDSNStationXML xmlns="http://www.fdsn.org/xml/station/1" schemaVersion="1.1">
            <Source>IRIS-DMC</Source>
            <Sender>IRIS-DMC</Sender>
            <Module>IRIS WEB SERVICE: fdsnws-station | version: 1.1.35</Module>
            <ModuleURI>http://service.iris.edu/fdsnws/station/1/query?starttime=1990-01-27T06&network=IU;level=response</ModuleURI>
            <Created>2018-11-08T14:57:56.000000Z</Created>
            <Network code="IU" endDate="2500-12-31T23:59:59.000000Z" restrictedStatus="open" startDate="1988-01-01T00:00:00.000000Z">
               <Description>Global Seismograph Network (GSN - IRIS/USGS)</Description>
               <TotalNumberStations>269</TotalNumberStations>
               <SelectedNumberStations>6</SelectedNumberStations>
               <Station code="ANMO" endDate="1995-07-14T00:00:00.000000Z" restrictedStatus="open" startDate="1989-08-29T00:00:00.000000Z">
                  <Channel>
                     <Response>
                        ...
                     </Response>
                  </Channel>
                  <Channel>
                     <Response>
                        ...
                     </Response>
                  </Channel>
               </Station>
               <Station code="CCM" endDate="1998-05-26T00:00:00.000000Z" restrictedStatus="open" startDate="1989-08-29T00:00:00.000000Z">
               </Station>
            </Network>
         </FDSNStationXML>


Note that each XML element must have a start tag (e.g., <Station>) and an end tag (</Station>)
and the element hierarchy must be maintained (e.g., a <Channel> may not exist outside
of a <Station> and a <Station> may not exist outside of a <Network>, etc.).


The FDSN and StationXML schema
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
StationXML was developed through the International Federation of Digital Seismograph Networks
(FDSN) to provide a standardized format for geophysical metadata.

Notice that the example stationXML excerpt above contains the following line::

   <FDSNStationXML xmlns="http://www.fdsn.org/xml/station/1" schemaVersion="1.1">

This specifies the location and version of the schema 
to which the stationxml example must conform.


The FDSN maintains the several versions of the stationxml schema at:

   `<https://www.fdsn.org/xml/station/>`_

For instance, at the time of this writing, the latest schema version is v1.1 and is
located at:

   `<https://www.fdsn.org/xml/station/fdsn-station-1.1.xsd>`_

Some History - SEED
----------------------

For many years, the Standard for the Exchange of Earthquake Data 
(`SEED <https://www.fdsn.org/publications/>`_) was the standard
format for archiving and distributing metadata within the seismological community.

StationXML was developed through the FDSN (International Federation of Digital Seismograph Networks)
as a replacement and extension of the SEED standard.

The purpose of the FDSN StationXML schema (`fdsn-station.xsd <https://www.fdsn.org/xml/station/>`_)
is to define an XML representation of the most important and 
commonly used structures of SEED 2.4 metadata with enhancements.

The goal is to allow mapping between SEED 2.4 dataless SEED volumes and this schema with as little 
transformation or loss of information as possible while at the same time simplifying station 
metadata representation when possible. Also, content and clarification has been added where 
lacking in the SEED standard.


ChangeLog
----------------------

   ::

      Changes from version 1.0 to 1.1 (2019-5-3)
      (Edited 2019-12-18 for small clarifications)

      * Add (persistent) <Identifier> element to all base nodes (Network, Station, Channel)

      * Unify response elements, allow "number" and disallow "unit" attribute to <Numerator> and <Denominator>

      * Allow <CreationDate> to be optional

      * Use xs:double for <ApproximationLowerBound>, <ApproximationUpperBound> and <MaximumError>

      * Include data availability elements described in the fdsn-station+availability-1.0.xsd extension schema as optional elements of the main schema

      * Remove <StorageFormat> from <Channel>

      * Limit each <Operator> to a single <Agency>

      * Allow more than a single <Equipment> occurrence in <Channel>, same as in <Station>

      * Allow <Operator> at the <Network> level, same as in <Station>

      * Add "sourceID" attribute, with URI value, to the base node type for <Network>,<Station>,<Channel>

      * Do not require and disallow <StageGain> and <Decimation> for <Polynomial> response stages

      * Add "measurementMethod" attribute to "uncertaintyDouble" attribute group used by azimuth, dip, distance, latitude, longitude, elevation, etc. types

      * Add <WaterLevel> within <Station> and <Channel>

      * Add "subject" attribute to <Comment> to allow relating comments, make "id" attribute optional.

