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

==============================   ===============================     ==============
                   Element                     Type                   Description
==============================   ===============================     ==============
                        Agency                         xs:string     None
                     Amplitude                     fsx:FloatType     None
       ApproximationLowerBound                         xs:double     None
             ApproximationType                              None     None
       ApproximationUpperBound                         xs:double     None
                      AreaCode                        xs:integer     None
                        Author                    fsx:PersonType     None
                       Azimuth                   fsx:AzimuthType     Azimuth of the sensor in degrees from north, clockwise.
            BeginEffectiveTime                       xs:dateTime     None
               CalibrationDate                       xs:dateTime     None
              CalibrationUnits                     fsx:UnitsType     None
        CfTransferFunctionType                              None     None
                       Channel                   fsx:ChannelType     None
                    ClockDrift                              None     A tolerance value, measured in seconds per sample, used as a threshold for time error detection in data from the channel.
                   Coefficient                              None     None
                  Coefficients              fsx:CoefficientsType     None
                       Comment                   fsx:CommentType     None
                       Contact                    fsx:PersonType     None
                    Correction                     fsx:FloatType     None
                       Country                         xs:string     None
                   CountryCode                        xs:integer     None
                        County                         xs:string     None
                       Created                       xs:dateTime     None
                  CreationDate                       xs:dateTime     Date and time (UTC) when the station was first installed.
              DataAvailability          fsx:DataAvailabilityType     A description of time series data availability. This information should be considered transient and is primarily useful as a guide for generating time series data requests. The information for a DataAvailability:Span may be specific to the time range used in a request that resulted in the document or limited to the availability of data withing the request range. These details may or may not be retained when synchronizing metadata between data centers.
                    DataLogger                 fsx:EquipmentType     None
                    Decimation                fsx:DecimationType     None
                         Delay                     fsx:FloatType     None
                   Denominator                              None     None
                         Depth                  fsx:DistanceType     The local depth or overburden of the instrument's location. For downhole instruments, the depth of the instrument under the surface ground level. For underground vaults, the distance from the instrument to the local ground level above.
                   Description                         xs:string     None
                           Dip                       fsx:DipType     Dip of the instrument in degrees, down from horizontal
                     Elevation                  fsx:DistanceType     Elevation of the sensor.
                         Email                     fsx:EmailType     None
              EndEffectiveTime                       xs:dateTime     None
                     Equipment                 fsx:EquipmentType     None
                        Extent    fsx:DataAvailabilityExtentType     None
             ExternalReference         fsx:ExternalReferenceType     URI of any type of external report, such as data quality reports.
                FDSNStationXML                      fsx:RootType     None
                           FIR                       fsx:FIRType     None
                        Factor                        xs:integer     None
                     Frequency                 fsx:FrequencyType     None
          FrequencyDBVariation                         xs:double     Variation in decibels within the specified range.
                  FrequencyEnd                         xs:double     None
           FrequencyLowerBound                 fsx:FrequencyType     None
                FrequencyStart                         xs:double     None
           FrequencyUpperBound                 fsx:FrequencyType     None
                       Geology                         xs:string     Type of rock and/or geologic formation.
                    Identifier                fsx:IdentifierType     None
                     Imaginary               fsx:FloatNoUnitType     None
               InputSampleRate                 fsx:FrequencyType     None
                    InputUnits                     fsx:UnitsType     The units of the data as input from the perspective of data acquisition. After correcting data for this response, these would be the resulting units.
              InstallationDate                       xs:dateTime     None
          InstrumentPolynomial                fsx:PolynomialType     The total sensitivity for a channel, representing the complete acquisition system expressed as a polynomial. Equivalent to SEED stage 0 polynomial (blockette 62).
         InstrumentSensitivity               fsx:SensitivityType     The total sensitivity for a channel, representing the complete acquisition system expressed as a scalar. Equivalent to SEED stage 0 gain with (blockette 58) with the ability to specify a frequency range.
                      Latitude                  fsx:LatitudeType     Latitude coordinate of this channel's sensor.
                     Longitude                 fsx:LongitudeType     Longitude coordinate of this channel's sensor.
                  Manufacturer                         xs:string     None
                  MaximumError                         xs:double     None
                         Model                         xs:string     None
                        Module                         xs:string     Name of the software module that generated this document.
                     ModuleURI                         xs:anyURI     This is the address of the query that generated the document, or, if applicable, the address of the software that generated this document.
                          Name                         xs:string     Name of units, e.g. "M/S", "V", "PA".
                       Network                   fsx:NetworkType     None
           NormalizationFactor                         xs:double     None
        NormalizationFrequency                 fsx:FrequencyType     None
                 NumberSamples                        xs:integer     None
                 NumberSeconds                        xs:integer     None
                     Numerator                              None     None
          NumeratorCoefficient                              None     None
                        Offset                        xs:integer     None
                      Operator                  fsx:OperatorType     An operator and associated contanct persons
                   OutputUnits                     fsx:UnitsType     The units of the data as output from the perspective of data acquisition. These would be the units of the data prior to correcting for this response.
                         Phase                     fsx:AngleType     None
                         Phone               fsx:PhoneNumberType     None
                   PhoneNumber                              None     None
                          Pole                  fsx:PoleZeroType     None
                    PolesZeros                fsx:PolesZerosType     None
                    Polynomial                fsx:PolynomialType     None
                  PreAmplifier                 fsx:EquipmentType     None
        PzTransferFunctionType                              None     None
                          Real               fsx:FloatNoUnitType     None
                        Region                         xs:string     The state, province, or region of this site.
                   RemovalDate                       xs:dateTime     None
                      Response                  fsx:ResponseType     None
                  ResponseList              fsx:ResponseListType     None
           ResponseListElement       fsx:ResponseListElementType     None
                    SampleRate                fsx:SampleRateType     None
               SampleRateRatio           fsx:SampleRateRatioType     None
        SelectedNumberChannels                   fsx:CounterType     Number of channels recorded at this station and selected by the query that produced this document.
        SelectedNumberStations                   fsx:CounterType     The total number of stations in this network that were selected by the query that produced this document, even if the stations do not appear in the document. (This might happen if the user only wants a document that goes contains only information at the Network level.)
                        Sender                         xs:string     Name of the institution sending this message.
                        Sensor                 fsx:EquipmentType     None
                  SerialNumber                         xs:string     None
                          Site                      fsx:SiteType     These fields describe the location of the station using geopolitical entities (country, city, etc.).
                        Source                         xs:string     Network ID of the institution sending the message.
                          Span      fsx:DataAvailabilitySpanType     None
                         Stage             fsx:ResponseStageType     None
                     StageGain                      fsx:GainType     The gain at the stage of the encapsulating response element at a specific frequencey and corresponds to SEED blockette 58. In the SEED convention, stage 0 gain represents the overall sensitivity of the channel. In this schema, stage 0 gains are allowed but are considered deprecated. Overall sensitivity should be specified in the InstrumentSensitivity element.
                       Station                   fsx:StationType     None
                      Symmetry                              None     None
               TerminationDate                       xs:dateTime     Date and time (UTC) when the station was terminated or will be terminated. A blank value should be assumed to mean that the station is still active.
           TotalNumberChannels                   fsx:CounterType     Total number of channels recorded at this station.
           TotalNumberStations                   fsx:CounterType     The total number of stations contained in this network, including inactive or terminated stations.
                          Town                         xs:string     The town or city closest to the station.
                          Type                         xs:string     None
                           URI                         xs:anyURI     None
                         Value                         xs:string     None
                         Vault                         xs:string     Type of vault, e.g. WWSSN, tunnel, transportable array, etc.
                        Vendor                         xs:string     None
                    WaterLevel                     fsx:FloatType     Elevation of the water surface in meters for underwater sites, where 0 is sea level.
                       WebSite                         xs:anyURI     None
                          Zero                  fsx:PoleZeroType     None
==============================   ===============================     ==============
