.. Put any comments here
   Be sure to indent at this level to keep it in comment.


< Nested View >
--------------------

.. toggle-header::
   :header: <Station>

   This is a station block

   .. toggle-header::
      :header: "           <Channel>"

         This is a channel block

      .. toggle-header::
         :header: <Response>

            This is a response block

Click below for nested tree

.. raw:: html
      :file: stn.html

< FDSNStationXML >
--------------------


   ::

      <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
      <FDSNStationXML xmlns="http://www.fdsn.org/xml/station/1" schemaVersion="1.1">
         <Source>IRIS-DMC</Source>
         <Module>IRIS converter | version: </Module>
         <ModuleURI>https://seiscode.iris.washington.edu/projects/stationxml-converter/wiki</ModuleURI>
         <Created>2019-12-14T23:20:56.779Z</Created>

< Source >
^^^^^^^^^^^

<Module>
^^^^^^^^^^^

<ModuleURI>
^^^^^^^^^^^^^

<Created>
^^^^^^^^^^^

< Network >
------------
   .. ^^^^^^^^^^^^

   ::

         <Network code="IU" endDate="2500-12-31T23:59:59.000000Z" restrictedStatus="open" startDate="1988-01-01T00:00:00.000000Z">
            <Description>Global Seismograph Network (GSN - IRIS/USGS)</Description>
            <TotalNumberStations>269</TotalNumberStations>
            <SelectedNumberStations>6</SelectedNumberStations>

Network attributes
^^^^^^^^^^^^^^^^^^^^^
code
""""""""
startDate
"""""""""""
endDate
""""""""
restrictedStatus
""""""""""""""""""

Network subelements
^^^^^^^^^^^^^^^^^^^^^
< Description >
"""""""""""""""""
< TotalNumberStations >
"""""""""""""""""""""""""""
< SelectedNumberStations >
"""""""""""""""""""""""""""


< Station >
----------------
   .. """"""""""""

   ::

            <Station code="ANMO" endDate="1995-07-14T00:00:00.000000Z" restrictedStatus="open" startDate="1989-08-29T00:00:00.000000Z">
               <Comment>
                  <Value>Time may be 1 minute slow.</Value>
                  <BeginEffectiveTime>1991-01-31T00:00:00.000000Z</BeginEffectiveTime>
                  <EndEffectiveTime>1991-02-16T00:00:00.000000Z</EndEffectiveTime>
               </Comment>
               <Comment>
                  <Value>Time correction does not include leap second.</Value>
                  <BeginEffectiveTime>1992-06-30T00:00:00.000000Z</BeginEffectiveTime>
                  <EndEffectiveTime>1993-03-22T18:50:00.000000Z</EndEffectiveTime>
               </Comment>
               <Comment>
                  <Value>TEST DATA:  Calibration, and testing in progress.</Value>
                  <BeginEffectiveTime>1993-02-08T23:00:00.000000Z</BeginEffectiveTime>
                  <EndEffectiveTime>1993-02-09T17:50:00.000000Z</EndEffectiveTime>
               </Comment>
               <Latitude unit="DEGREES">34.9459</Latitude>
               <Longitude unit="DEGREES">-106.4572</Longitude>
               <Elevation>1850.0</Elevation>
               <Site>
                  <Name>Albuquerque, New Mexico, USA</Name>
               </Site>
               <CreationDate>1989-08-29T00:00:00.000000Z</CreationDate>
               <TotalNumberChannels>121</TotalNumberChannels>
               <SelectedNumberChannels>121</SelectedNumberChannels>

< Channel >
------------
   .. '''''''''''''

   ::

               <Channel code="BHZ" endDate="2011-02-18T19:11:00.000000Z" locationCode="00" restrictedStatus="open" startDate="2008-0>
                  <Latitude unit="DEGREES">34.94598</Latitude>
                  <Longitude unit="DEGREES">-106.45713</Longitude>
                  <Elevation>1671.0</Elevation>
                  <Depth>145.0</Depth>
                  <Azimuth unit="DEGREES">0.0</Azimuth>
                  <Dip unit="DEGREES">-90.0</Dip>
                  <Type>CONTINUOUS</Type>
                  <Type>GEOPHYSICAL</Type>
                  <SampleRate unit="SAMPLES/S">20.0</SampleRate>
                  <ClockDrift unit="SECONDS/SAMPLE">0.0</ClockDrift>



< Response >
------------
   .. ..............

This is the Response element

   ::

               <Channel code="BHZ" endDate="2011-02-18T19:11:00.000000Z" locationCode="00" restrictedStatus="open" startDate="2008-0>
                  <Latitude unit="DEGREES">34.94598</Latitude>
                  <Longitude unit="DEGREES">-106.45713</Longitude>
                  <Elevation>1671.0</Elevation>
                  <Depth>145.0</Depth>
                  <Azimuth unit="DEGREES">0.0</Azimuth>
                  <Dip unit="DEGREES">-90.0</Dip>
                  <Type>CONTINUOUS</Type>
                  <Type>GEOPHYSICAL</Type>
                  <SampleRate unit="SAMPLES/S">20.0</SampleRate>
                  <ClockDrift unit="SECONDS/SAMPLE">0.0</ClockDrift>


