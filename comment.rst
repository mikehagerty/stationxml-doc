.. role:: blue

.. role:: red

.. raw:: html

    <style> .red {color:red} </style>
    <style> .blue {color:blue} </style>

<Comment>
--------------

      Container for a comment or log entry. Corresponds to SEED blockettes 31, 51 and 59.

.. csv-table:: *Comment attributes*
    :header: "attribute", "type", "required", "description", "example"
    :widths: 20, 20, 10, 20, 20

    "id", :blue:`CounterType`, "no", "An id for this comment", "id=12345"
    "subject", :blue:`string`, "no", "A subject for this comment", "subject='Routine maintenance'"


::

      Sample
      <Comment id=12345 subject="Routine maintenance">
         <Value>This is a comment</Value>
         <BeginEffectiveTime></BeginEffectiveTime>
         <EndEffectiveTime></EndEffectiveTime>
         <Author>
         </Author>
      </Comment


<Value> :red:`required`
^^^^^^^^^^^^^^^^^^^^^^^^^

   type: :blue:`string`

   **Example:**
   <Value> *The actual comment goes here.* </Value>

<BeginEffectiveTime>
^^^^^^^^^^^^^^^^^^^^^

   type: :blue:`dateTime`

   **Example:**
   <BeginEffectiveTime> *1998-02-27T13:00:00* </BeginEffectiveTime>

<EndEffectiveTime>
^^^^^^^^^^^^^^^^^^^^^

   type: :blue:`dateTime`

   **Example:**
   <EndEffectiveTime> *2016-01-27T13:00:00* </EndEffectiveTime>

<Author>
^^^^^^^^^^^^^^^^^^^^^

   Representation of a person's contact information. A person can belong to multiple agencies and have multiple email addresses and phone numbers.

<Name>
'''''''

   type::blue:`string`

   **Example:**
   <Name> *Alfred E. Neuman* </Name>

<Agency>
'''''''''

   type::blue:`string`

   **Example:**
   <Agency> *Mad Magazine, Inc.* </Agency>

<Email>
'''''''''

   type::blue:`string`

   **Example:**
   <Email> *a.neuman@gmail.com* </Email>


<Phone>
''''''''

   Contact phone number

<CountryCode>
"""""""""""""""

   type::blue:`integer`

<AreaCode>  :red:`required`
"""""""""""""""""""""""""""""""

   type::blue:`integer`

<PhoneNumber>  :red:`required`
"""""""""""""""""""""""""""""""

   type::blue:`string`

