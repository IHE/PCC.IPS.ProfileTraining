# Coded Values Overview

1. References
 * https://www.snomed.org/snomed-ct/Other-SNOMED-products/international-patient-summary-terminology
 * https://www.snomed.org/news-and-events/articles/hl7-snomed-international-patient-summary-(1)

2. See https://build.fhir.org/ig/HL7/fhir-ips/principles.html
 * Section 2.1 of the ***principles*** page has relevant text.

3. Selected text from Section 2.1 concerning SNOMED
 * To be universally exchangeable and understood, a patient summary must rely as much as possible on structured data and multilingual international reference terminologies that are licensed at no cost for global use in the International Patient Summary.
 * In the case of SNOMED CT, SNOMED International has created an [open and free specification for the International Patient Summary](https://www.snomed.org/snomed-ct/Other-SNOMED-products/international-patient-summary-terminology) that references a core set of globally accessible and usable clinical concepts licensed at no-cost with the aim to serve the public good called the [IPS Free set](https://www.snomed.org/news-and-events/articles/hl7-snomed-international-patient-summary-(1)).
 * This free set is maintained in collaboration with HL7 International and CEN and updated annually. SNOMED International has also produced a freely available resource called the IPS Terminology, a sub-ontology of SNOMED CT based on the IPS Free set, which will provide minimal ontological features for IPS implementations.
 * In this spirit, this version of the International Patient Summary defines SNOMED CT as a primary terminology and it is used in many of the value sets.
 * It is worth noting that current SNOMED CT users, those located in a SNOMED International Member region or those with an Affiliate license to a complete SNOMED CT edition, should avoid use of the IPS Terminology or Freeset and instead, implement their IPS solutions using a full edition of SNOMED CT. To share IPS data with non-Affiliates, licensed users may choose to refer to the IPS Terminology which includes access to the IPS Free set.

4. Further text in Section 2.1 concerning other code systems
 * Other primary terminologies used in this specification are
      * LOINC for observations (e.g., laboratory tests) and document sections,
      * UCUM for units of measure,
      * EDQM Standard Terms for dose forms and routes and
      * ISO 3166 for countries [this ISO code system can be used for free in «lists» (e.g. value sets) or software].
  * Looking at the availability of other globally usable reference terminologies, in selected cases FHIR-defined terminologies are recommended.