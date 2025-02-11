<!DOCTYPE timeTable [
  <!ELEMENT timeTable (complexes, lessons)>
<!ELEMENT complexes (complex+)>
<!ELEMENT lessons (lesson+)>
<!ELEMENT complex (name, address)>
<!ELEMENT lesson (date, time)>
<!ELEMENT name (#PCDATA)>
<!ELEMENT address (#PCDATA)>
<!ELEMENT date (#PCDATA)>
<!ELEMENT time (#PCDATA)>

<!ATTLIST complex code ID #REQUIRED>
<!ATTLIST lesson no CDATA #REQUIRED>
<!ATTLIST lesson complex IDREF #REQUIRED>
]>
<timeTable>
  <complexes>
    <complex code="c1">
      <name>Комплекс 1</name>
      <address>Улица А, дом 10</address>
    </complex>
    <complex code="c2">
      <name>Комплекс 2</name>
      <address>Улица Б, дом 20</address>
    </complex>
  </complexes>
  <lessons>
    <lesson no="1" complex="c1">
      <date>2023-10-01</date>
      <time>10:00</time>
    </lesson>
    <lesson no="2" complex="c2">
      <date>2023-10-02</date>
      <time>12:00</time>
    </lesson>
  </lessons>
</timeTable>
