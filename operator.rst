.. role:: blue

.. role:: red

.. raw:: html

    <style> .red {color:red} </style>
    <style> .blue {color:blue} </style>

<Operator>
------------------

<Agency> :red:`required`
^^^^^^^^^^^^^^^^^^^^^^^^^

   type: :blue:`string`

   **Example:**
   <Agency> *Albuquerque Seismic Lab* </Agency>

<Contact>
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

<Website>
^^^^^^^^^^^^^^^^^^^^^

   type::blue:`anyURI`
