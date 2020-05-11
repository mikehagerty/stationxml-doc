.. Put any comments here
   Be sure to indent at this level to keep it in comment.

.. role:: blue

.. role:: red

.. raw:: html

    <style> .red {color:red} </style>
    <style> .blue {color:blue} </style>
    <style> .ital {font-style:italic} </style>

<Station> 
===============

      This type represents a Station epoch. It is common to only have a single station epoch with the 
      station's creation and termination dates as the epoch start and end dates.

      **Example**: <Station code="ANMO">


.. csv-table:: *Station attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 10, 20

    **code**, :blue:`string`, :red:`yes`, "3-5 char station code", "code=ANMO"
    **startDate**, :blue:`dateTime`, "no", "network start date", "startDate=1988-01-01T00:00:00"
    **endDate**, :blue:`dateTime`, "no", "network end date", "endDate=1988-01-01T00:00:00"
    **sourceID**, :blue:`anyURI`, "no", "A data source identifier in URI form", "sourceID='http://some/path'"
    **restrictedStatus**, :blue:`NMTOKEN`, "no", "open, closed, partial", "restrictedStatus=open"
    **alternateCode**, :blue:`string`, "no", "A code used for display or association, alternate to the SEED-compliant code.", "alternateCode=ANM"
    **historicalCode**, :blue:`string`, "no", "historical network code", "historicalCode=ALQ"

<Description>
--------------

   Description of the Station

   type::blue:`string`

   **Example:**
   <Description> *This is the station description* </Description>

<Identifier>
--------------

   Identifier values should be specified without a URI scheme (prefix), instead the identifer type is documented as an attribute.

   type::blue:`string`

   **Example:**
   <Identifier> *identifier* </Identifier>

.. csv-table:: *Identifier attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 10, 20

    **type**, :blue:`string`, no, "Type of identifier", "type=some_type"


.. include:: comment.rst
.. include:: dataavailability.rst
.. include:: operator.rst

<Latitude> :red:`required`
------------------------------

   Station latitude coordinate.

   type: :blue:`double` where: -90.0 <= Latitude < 90.0

   **Example:**
   <Latitude unit="DEGREES" datum="WGS84">34.9459</Latitude>

.. csv-table:: *Latitude attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 10, 20

    **unit**, :blue:`string`, no, "unit of latitude", "unit=DEGREES"
    **plusError**, :blue:`double`, no, "plus error in latitude", "plusError=0.1"
    **minusError**, :blue:`double`, no, "minus error in latitude", "minusError=0.1"
    **measurementMethod**, :blue:`string`, no, "method of measurement",
    **datum**, :blue:`NMTOKEN`, no, "datum used", "datum=WGS84"


<Longitude> :red:`required`
------------------------------

   Station longitude coordinate.

   type: :blue:`double` where: -180.0 <= Longitude < 180.0

   **Example:**
   <Longitude unit="DEGREES" datum="WGS84">-106.4572</Longitude>

.. csv-table:: *Longitude attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 10, 20

    **unit**, :blue:`string`, no, "unit of latitude", "unit=DEGREES"
    **plusError**, :blue:`double`, no, "plus error in latitude", "plusError=0.1"
    **minusError**, :blue:`double`, no, "minus error in latitude", "minusError=0.1"
    **measurementMethod**, :blue:`string`, no, "method of measurement",
    **datum**, :blue:`NMTOKEN`, no, "datum used", "datum=WGS84"

<Elevation> :red:`required`
------------------------------

   Station elevation

   type: :blue:`double` 

   **Example:**
   <Elevation unit="METERS">1850.0</Elevation>

.. csv-table:: *Elevation attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 10, 20

    **unit**, :blue:`string`, no, "unit of latitude", "unit=DEGREES"
    **plusError**, :blue:`double`, no, "plus error in latitude", "plusError=0.1"
    **minusError**, :blue:`double`, no, "minus error in latitude", "minusError=0.1"
    **measurementMethod**, :blue:`string`, no, "method of measurement",

<Site>
------------------

   These fields describe the location of the station using geopolitical entities (country, city, etc.)

<Name> :red:`required`
^^^^^^^^^^^^^^^^^^^^^^^^^^

   type::blue:`string`

   **Example:**
   <Site> *Albuquerque, New Mexico* </Site>

<Description>
^^^^^^^^^^^^^^^^

   type::blue:`string`

   **Example:**
   <Description> *A hot and desolate place* </Description>

<Town>
^^^^^^^^^^^^^^^^

   type::blue:`string`

   **Example:**
   <Town> *Albuquerque* </Town>

<County>
^^^^^^^^^^^^^^^^

   type::blue:`string`

   **Example:**
   <County> *Bernalillo County* </County>

<Region>
^^^^^^^^^^^^^^^^

   type::blue:`string`

   **Example:**
   <Region> *Southwest* </Region>

<Country>
^^^^^^^^^^^^^^^^

   type::blue:`string`

   **Example:**
   <Country> *U.S.A.* </Country>

<WaterLevel>
------------------

   Elevation of the water surface in meters for underwater sites, where 0 is sea level.

   type: :blue:`double`

.. csv-table:: *WaterLevel attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 10, 20

    **unit**, :blue:`string`, no, "unit of latitude", "unit=DEGREES"
    **plusError**, :blue:`double`, no, "plus error in latitude", "plusError=0.1"
    **minusError**, :blue:`double`, no, "minus error in latitude", "minusError=0.1"
    **measurementMethod**, :blue:`string`, no, "method of measurement",

<Vault>
------------------

   Description of station vault.

   type: :blue:`string`

<Geology>
------------------

   Description of station geology.

   type: :blue:`string`


<Equipment>
------------------

   Equipment used by all channels at a station.

.. csv-table:: *Equipment attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 10, 20

    **resourceId**, :blue:`string`, no, "This field contains a string that should serve as a unique resource identifier. This identifier can be interpreted differently depending on the datacenter/software that generated the document. Also, we recommend to use something like GENERATOR:Meaningful ID. As a common behaviour equipment with the same ID should contains the same information/be derived from the same base instruments.",


<Type>
^^^^^^^^^^^^^

   Type of equipment

   type: :blue:`string`

<Description>
^^^^^^^^^^^^^

   Description of equipment

   type: :blue:`string`


<Manufacturer>
^^^^^^^^^^^^^^^

   Manufacturer of equipment

   type: :blue:`string`

<Vendor>
^^^^^^^^^^^^^^^

   Vendor of equipment

   type: :blue:`string`

<SerialNumber>
^^^^^^^^^^^^^^^

   Serial number of equipment

   type: :blue:`string`


<InstallationDate>
^^^^^^^^^^^^^^^^^^^

   Installation date of equipement

   type: :blue:`dateTime`


<RemovalDate>
^^^^^^^^^^^^^^^^^^^

   Removal date of equipement

   type: :blue:`dateTime`

<CalibrationDate>
^^^^^^^^^^^^^^^^^^^

   Calibration date of equipement

   type: :blue:`dateTime`


<CreationDate>
----------------------

<TerminationDate>
----------------------

<TotalNumberChannels>
-------------------------

<SelectedNumberChannels>
-------------------------

<ExternalReference>
-------------------------

   URI of any type of external report, such as IRIS data reports or dataless SEED volumes

<URI> :red:`required`
^^^^^^^^^^^^^^^^^^^^^
   type: :blue:`anyURI`

<Description> :red:`required`
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   type: :blue:`string`

