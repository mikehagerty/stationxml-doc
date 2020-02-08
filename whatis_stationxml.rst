.. Put any comments here
   Be sure to indent at this level to keep it in comment.

What is StationXML ?
===========================================

StationXML from the top down
-------------------------------

<Preamble>
^^^^^^^^^^^^^^^^^

   ::

      <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
      <FDSNStationXML xmlns="http://www.fdsn.org/xml/station/1" schemaVersion="1.1">
         <Source>IRIS-DMC</Source>
         <Module>IRIS converter | version: </Module>
         <ModuleURI>https://seiscode.iris.washington.edu/projects/stationxml-converter/wiki</ModuleURI>
         <Created>2019-12-14T23:20:56.779Z</Created>

<Network>
^^^^^^^^^^^^^^^^^

   ::

         <Network code="IU" endDate="2500-12-31T23:59:59.000000Z" restrictedStatus="open" startDate="1988-01-01T00:00:00.000000Z">
            <Description>Global Seismograph Network (GSN - IRIS/USGS)</Description>
            <TotalNumberStations>269</TotalNumberStations>
            <SelectedNumberStations>6</SelectedNumberStations>


<Station>
^^^^^^^^^^^^^^^^^

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

<Channel>
^^^^^^^^^^^^^^^^^

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

<CalibrationUnits>
""""""""""""""""""""""""

   ::

                  <CalibrationUnits>
                     <Name>A</Name>
                     <Description>Amperes</Description>
                  </CalibrationUnits>

<Sensor>
""""""""""""""""""""""""

   ::

                  <Sensor>
                     <Description>Geotech KS-54000 Borehole Seismometer</Description>
                  </Sensor>


<Response>
^^^^^^^^^^^^^^^^^

<InstrumentSensitivity>
""""""""""""""""""""""""

<InstrumentPolynomial>
""""""""""""""""""""""""

<Stage>
""""""""""""""""""""""""

<PoleZeros>
'''''''''''''''''''''

<Coefficients>
'''''''''''''''''''''

StationXML tag element glossary
-------------------------------


==============================   ==============================================
                Element          Description
==============================   ==============================================
                        Agency    None
                     Amplitude    None
       ApproximationLowerBound    None
             ApproximationType    None
       ApproximationUpperBound    None
                      AreaCode    None
                        Author    None
                       Azimuth    Azimuth of the sensor in degrees from north, clockwise.
            BeginEffectiveTime    None
               CalibrationDate    None
              CalibrationUnits    None
        CfTransferFunctionType    None
                       Channel    None
                    ClockDrift    A tolerance value, measured in seconds per sample, used as a threshold for time error detection in data from the channel.
                   Coefficient    None
                  Coefficients    None
                       Comment    None
                       Contact    None
                    Correction    None
                       Country    None
                   CountryCode    None
                        County    None
                       Created    None
                  CreationDate    Date and time (UTC) when the station was first installed.
              DataAvailability    A description of time series data availability. This information should be considered transient and is primarily useful as a guide for generating time series data requests. The information for a DataAvailability:Span may be specific to the time range used in a request that resulted in the document or limited to the availability of data withing the request range. These details may or may not be retained when synchronizing metadata between data centers.
                    DataLogger    None
                    Decimation    None
                         Delay    None
                   Denominator    None
                         Depth    The local depth or overburden of the instrument's location. For downhole instruments, the depth of the instrument under the surface ground level. For underground vaults, the distance from the instrument to the local ground level above.
                   Description    None
                           Dip    Dip of the instrument in degrees, down from horizontal
                     Elevation    Elevation of the sensor.
                         Email    None
              EndEffectiveTime    None
                     Equipment    None
                        Extent    None
             ExternalReference    URI of any type of external report, such as data quality reports.
                FDSNStationXML    None
                           FIR    None
                        Factor    None
                     Frequency    None
          FrequencyDBVariation    Variation in decibels within the specified range.
                  FrequencyEnd    None
           FrequencyLowerBound    None
                FrequencyStart    None
           FrequencyUpperBound    None
                       Geology    Type of rock and/or geologic formation.
                    Identifier    None
                     Imaginary    None
               InputSampleRate    None
                    InputUnits    The units of the data as input from the perspective of data acquisition. After correcting data for this response, these would be the resulting units.
              InstallationDate    None
          InstrumentPolynomial    The total sensitivity for a channel, representing the complete acquisition system expressed as a polynomial. Equivalent to SEED stage 0 polynomial (blockette 62).
         InstrumentSensitivity    The total sensitivity for a channel, representing the complete acquisition system expressed as a scalar. Equivalent to SEED stage 0 gain with (blockette 58) with the ability to specify a frequency range.
                      Latitude    Latitude coordinate of this channel's sensor.
                     Longitude    Longitude coordinate of this channel's sensor.
                  Manufacturer    None
                  MaximumError    None
                         Model    None
                        Module    Name of the software module that generated this document.
                     ModuleURI    This is the address of the query that generated the document, or, if applicable, the address of the software that generated this document.
                          Name    Name of units, e.g. "M/S", "V", "PA".
                       Network    None
           NormalizationFactor    None
        NormalizationFrequency    None
                 NumberSamples    None
                 NumberSeconds    None
                     Numerator    None
          NumeratorCoefficient    None
                        Offset    None
                      Operator    An operator and associated contanct persons
                   OutputUnits    The units of the data as output from the perspective of data acquisition. These would be the units of the data prior to correcting for this response.
                         Phase    None
                         Phone    None
                   PhoneNumber    None
                          Pole    None
                    PolesZeros    None
                    Polynomial    None
                  PreAmplifier    None
        PzTransferFunctionType    None
                          Real    None
                        Region    The state, province, or region of this site.
                   RemovalDate    None
                      Response    None
                  ResponseList    None
           ResponseListElement    None
                    SampleRate    None
               SampleRateRatio    None
        SelectedNumberChannels    Number of channels recorded at this station and selected by the query that produced this document.
        SelectedNumberStations    The total number of stations in this network that were selected by the query that produced this document, even if the stations do not appear in the document. (This might happen if the user only wants a document that goes contains only information at the Network level.)
                        Sender    Name of the institution sending this message.
                        Sensor    None
                  SerialNumber    None
                          Site    These fields describe the location of the station using geopolitical entities (country, city, etc.).
                        Source    Network ID of the institution sending the message.
                          Span    None
                         Stage    None
                     StageGain    The gain at the stage of the encapsulating response element at a specific frequencey and corresponds to SEED blockette 58. In the SEED convention, stage 0 gain represents the overall sensitivity of the channel. In this schema, stage 0 gains are allowed but are considered deprecated. Overall sensitivity should be specified in the InstrumentSensitivity element.
                       Station    None
                      Symmetry    None
               TerminationDate    Date and time (UTC) when the station was terminated or will be terminated. A blank value should be assumed to mean that the station is still active.
           TotalNumberChannels    Total number of channels recorded at this station.
           TotalNumberStations    The total number of stations contained in this network, including inactive or terminated stations.
                          Town    The town or city closest to the station.
                          Type    None
                           URI    None
                         Value    None
                         Vault    Type of vault, e.g. WWSSN, tunnel, transportable array, etc.
                        Vendor    None
                    WaterLevel    Elevation of the water surface in meters for underwater sites, where 0 is sea level.
                       WebSite    None
                          Zero    None
==============================   ==============================================
