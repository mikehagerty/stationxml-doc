.. Put any comments here
   Be sure to indent at this level to keep it in comment.

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
