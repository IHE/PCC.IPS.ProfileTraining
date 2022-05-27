# IPS Header Sections

1. See: https://build.fhir.org/ig/HL7/fhir-ips/ipsStructure.html
2. List of header sections

|  Category    |  Section                     |
|--------------|------------------------------|
| Header       | Subject                      |
| Header       | Author                       |
| Header       | Attester                     |
| Header       | Custodian                    |

3. Open the file samples/EU_Giorgio_Cangioli_01.json
4. In the Composition resource, locate these:
 * type {  }
 * subject (References Patient later)
 * author (References Practitioner later)
 * title
 * confidentiality
 * section []
5. Not included in this sample:
 * Attester
 * Custodian

6. Open the file samples/IPS_IG-bundle-01.json
7. In the Composition resource, locate these:
 * confidentiality
 * **attester** (Note: Practitioner and Organization)
 * **custodian** (Note: Organization)
 * relatesTo

8. Open the file samples/NZ_Peter_Jordan_AAA1234.json
9. In the Composition resource, locate these:
 * confidentiality
 * **attester** (Note: PractitionerRole only)
 * **custodian** (Note: Organization)
 * relatesTo

## Notes
1. Follow up on attester (Practitioner, PractitionerRole, Organization)

## Pages to Read (In Order)
* [FHIR Bundle](01_FHIR_Bundle.md)
* [Composition](02_Composition.md)
* [IPS Sections](03_IPS_Sections.md)
* [Header Sections](04_Header_Sections.md)
* [&rarr; Required Sections](05_Required_Sections.md)
* [Full Resources](06_Full_Resources.md)
* [IPS_Document_Validation/README.md](../IPS_Document_Validation/README.md)