File structure use to rename the input to boolean
```
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified" xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="AnalogDigitalCompressConfig">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="PortConnections">
          <xs:complexType>
            <xs:sequence>
              <xs:element maxOccurs="unbounded" name="PortConnection">
                <xs:complexType>
                  <xs:attribute name="portId" type="xs:unsignedInt" use="required" />
                  <xs:attribute name="patternName" type="xs:string" use="required" />
                </xs:complexType>
              </xs:element>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="AnalogDigitalCompressPatterns">
          <xs:complexType>
            <xs:sequence>
              <xs:element maxOccurs="unbounded" name="AnalogDigitalCompressPattern">
                <xs:complexType>
                  <xs:sequence>
                    <xs:element name="digital">
                      <xs:complexType>
                        <xs:attribute name="index" type="xs:unsignedInt" use="required" />
                        <xs:attribute name="label" type="xs:string" use="required" />
                        <xs:attribute name="inverse" type="xs:boolean" use="optional" />
                      </xs:complexType>
                    </xs:element>
                    <xs:element name="analog">
                      <xs:complexType>
                        <xs:attribute name="index" type="xs:unsignedInt" use="required" />
                        <xs:attribute name="label" type="xs:string" use="required" />
                        <xs:attribute name="from" type="xs:short" use="required" />
                        <xs:attribute name="to" type="xs:short" use="required" />
                        <xs:attribute name="inverse" type="xs:boolean" use="optional" />
                      </xs:complexType>
                    </xs:element>
                  </xs:sequence>
                  <xs:attribute name="name" type="xs:string" use="required" />
                  <xs:attribute name="docUrl" type="xs:string" use="required" />
                </xs:complexType>
              </xs:element>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```


Example:
```
<?xml version="1.0" encoding="utf-8"?>

<AnalogDigitalCompressConfig>

  <PortConnections>
    <PortConnection portId="20" patternName="Custom" />
  </PortConnections>
  <AnalogDigitalCompressPatterns>
    <AnalogDigitalCompressPattern name="Left Hand Pad V1" docUrl="">
      <analog index="0" label="PTR" from="5" to="9" />
      <analog index="1" label="PTL" from="5" to="9"/>
      <analog index="2" label="PDR" from="5" to="9"/>
      <analog index="3" label="PDL" from="5" to="9"/>
      <analog index="4" label="FingerDown" from="5" to="9"/>
      <analog index="5" label="FingerTop" from="5" to="9"/>
      <analog index="6" label="FingerMiddle" from="6" to="9"/>
      <analog index="7" label="ThumbDown" from="8" to="9"/>
      <analog index="8" label="ThumbUp" from="5" to="9"/>
      <analog index="9" label="Hand" from="5" to="9"/>
    </AnalogDigitalCompressPattern>
    <AnalogDigitalCompressPattern name="Wood Adaptator" docUrl="">
      <analog index="0" label="WAPin0" from="5" to="9" />
      <analog index="1" label="WAPin1" from="5" to="9"/>
      <analog index="2" label="WAPin2" from="5" to="9"/>
      <analog index="3" label="WAPin3" from="5" to="9"/>
      <analog index="4" label="WAPin4" from="5" to="9"/>
      <analog index="5" label="WAPin5" from="5" to="9"/>
      <analog index="6" label="WAPin6" from="5" to="9"/>
    </AnalogDigitalCompressPattern>
    <AnalogDigitalCompressPattern name="Footboard Left Foot" docUrl="">
      <digit index="0" label="FootLeftTopMiddle" />
      <digit index="1" label="FootLeftTop" />
      <digit index="2" label="FootLeftDown" />
      <digit index="3" label="FootLeftDownMiddle" />
      <digit index="4" label="FootLeftTop" />
      <digit index="5" label="FootLeftDown" />
    </AnalogDigitalCompressPattern> 
 <AnalogDigitalCompressPattern name="Foot 4 Simple Buttons" docUrl="">
      <digit index="5" label="Foot4PadRD" />
      <digit index="2" label="Foot4PadLT" />
      <digit index="7" label="Foot4PadRT" />
      <digit index="4" label="Foot4PadLD" />
    </AnalogDigitalCompressPattern>
<AnalogDigitalCompressPattern name="Foot 4+5 Simple Buttons" docUrl="">
      <digit index="0" label="Foot45RD" />
      <digit index="1" label="Foot45LT" />
      <digit index="2" label="Foot45RT" />
      <digit index="3" label="Foot45LD" />
      <digit index="5" label="Foot45BLeft" />
      <digit index="8" label="Foot45BRight" />
      <digit index="6" label="Foot45BCenterTop" />
      <digit index="4" label="Foot45BCenter" />
      <digit index="7" label="Foot45BCenterDown" />
      </AnalogDigitalCompressPattern>
  </AnalogDigitalCompressPatterns>
 <AnalogDigitalCompressPattern name="Custom" docUrl="">
      <digit index="10" label="CustomRD" />
      <digit index="9" label="CustomLT" />
      <digit index="7" label="CustomRT" />
      <digit index="8" label="CustomLD" />
      <digit index="3" label="CustomAltLeft" />
      <digit index="1" label="CustomAltRight" />
      <digit index="2" label="CustomLeft" />
      <digit index="0" label="CustomMidLeft" />
      <digit index="6" label="CustomMidRight" />
      <digit index="4" label="CustomRight" />
    </AnalogDigitalCompressPattern>
</AnalogDigitalCompressConfig>
```