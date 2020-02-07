.. Put any comments here
   Be sure to indent at this level to keep it in comment.

What is XML ?
===========================================


Extensible Markup Language (XML) is a markup language that defines a set of 
rules for encoding documents in a format that is both human-readable and machine-readable.

Summary of some key xml components
-------------------------------------

* Markup and content
   The characters making up an XML document are divided into markup and content, which may be distinguished by the application of simple syntactic rules. Generally, strings that constitute markup either begin with the character < and end with a >, or they begin with the character & and end with a ;. Strings of characters that are not markup are content. However, in a CDATA section, the delimiters <![CDATA[ and ]]> are classified as markup, while the text between them is classified as content. In addition, whitespace before and after the outermost element is classified as markup.

* Tag
   A tag is a markup construct that begins with < and ends with >. Tags come in three flavors:
   start-tag, such as <section>;
   end-tag, such as </section>;
   empty-element tag, such as <line-break />.

* Element
   An element is a logical document component that either begins with a start-tag and ends with a matching end-tag or consists only of an empty-element tag. The characters between the start-tag and end-tag, if any, are the element's content, and may contain markup, including other elements, which are called child elements. An example is <greeting>Hello, world!</greeting>. Another is <line-break />.

* Attribute
   An attribute is a markup construct consisting of a name–value pair that exists within a start-tag or empty-element tag. An example is <img src="madonna.jpg" alt="Madonna" />, where the names of the attributes are "src" and "alt", and their values are "madonna.jpg" and "Madonna" respectively. Another example is <step number="3">Connect A to B.</step>, where the name of the attribute is "number" and its value is "3". An XML attribute can only have a single value and each attribute can appear at most once on each element. In the common situation where a list of multiple values is desired, this must be done by encoding the list into a well-formed XML attribute[i] with some format beyond what XML defines itself. Usually this is either a comma or semi-colon delimited list or, if the individual values are known not to contain spaces,[ii] a space-delimited list can be used. <div class="inner greeting-box">Welcome!</div>, where the attribute "class" has both the value "inner greeting-box" and also indicates the two CSS class names "inner" and "greeting-box".

* XML declaration
   XML documents may begin with an XML declaration that describes some information about themselves. An example is <?xml version="1.0" encoding="UTF-8"?>.


XML schema vs XML file
-------------------------------------

An XML schema is a file, often ending in '.xsd' that defines the valid structure of XML documents
that adhere to the schema.
The XML Schema language is also referred to as XML Schema Definition (XSD).
The format of an xsd schema is very similar to an xml file.

StationXML Example
^^^^^^^^^^^^^^^^^^^^^^


XSD Example
^^^^^^^^^^^^

    ::

      <?xml version="1.0"?>
      <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

      <xs:element name="note">
      <xs:complexType>
         <xs:sequence>
            <xs:element name="to" type="xs:string"/>
            <xs:element name="from" type="xs:string"/>
            <xs:element name="heading" type="xs:string"/>
            <xs:element name="body" type="xs:string"/>
         </xs:sequence>
      </xs:complexType>
      </xs:element>

      </xs:schema>


What kind of information is contained in the StationXML schema ?
-------------------------------------------------------------------

The stationxml schema (https://www.fdsn.org/xml/station/fdsn-station-1.1.xsd)
specifies what a valid stationxml file looks like -- what elements must be present,
what attributes are mandatory or optional, etc.
In addition, it specifies what type of value each element may have,and in some cases,
the allowable values.
For instance, both <Station> and <Channel> elements must contain <Latitude> and <Longitude>
elements, among others, that specify where they are located.
We can see how the <Latitude> element is specified in the code block below, which
presents pieces of the xsd file, not necessarily in any order, that are relevant to this field.


Stationxml <Latitude> specification in the xsd
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

    ::

      <xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" xmlns:fsx="http://www.fdsn.org/xml/station/1" ..>
      ...
      <xs:element name="Latitude" type="fsx:LatitudeType">
      ...

      ...
      <xs:complexType name="LatitudeType">
         <xs:annotation>
            <xs:documentation>Type for latitude coordinate.</xs:documentation>
         </xs:annotation>
         <xs:simpleContent>
            <xs:extension base="fsx:LatitudeBaseType">
            <xs:attribute name="datum" type="xs:NMTOKEN" use="optional" default="WGS84"/>
            </xs:extension>
         </xs:simpleContent>
      </xs:complexType>
      ...

      ...
      <xs:complexType name="LatitudeBaseType">
         <xs:annotation>
            <xs:documentation>Base latitude type. Because of the limitations of schema, defining
            this type and then extending it to create the real latitude type is the only way to
            restrict values while adding datum as an attribute.</xs:documentation>
         </xs:annotation>
         <xs:simpleContent>
            <xs:restriction base="fsx:FloatType">
            <xs:minInclusive value="-90"/>
            <xs:maxExclusive value="90"/>
            <xs:attribute name="unit" type="xs:string" use="optional" fixed="DEGREES"/>
            <xs:attributeGroup ref="fsx:uncertaintyDouble"/>
            </xs:restriction>
         </xs:simpleContent>
      </xs:complexType>

      </xs:schema>


From this, we see that <Latitude> is of type <LatitudeType> which in turn extends LatitudeBaseType.
In addition, we can see that the value of LatitudeBaseType, and hence the value of the <Latitude> element,
must be a float between :math:`\pm 90`. However, note that the lower range (:math:`-90`) is included (allowed),
while the upper range (:math:`+90`) is not.

e.g., we must have :math:`-90\le` latitude :math:`\lt90`.

So a stationxml file that contains:

    ::

      <Latitude>
         89.9
      </Latitude>

will be valid, while a stationxml file containing:

    ::

      <Latitude>
         90.0
      </Latitude>

will not be valid
