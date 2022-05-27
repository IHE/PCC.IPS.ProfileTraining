# MustSupport Conformance Rule
1. See https://www.hl7.org/fhir/conformance-rules.html
 * Section 2.1.0.5 MustSupport
2. Annotated copy of text in that section.
 * Labeling an element **MustSupport** means that implementations that produce or consume resources SHALL provide "support" for the element in **some meaningful way**.
     * Meaningful way is not defined by the FHIR base specification.
 * Because the base FHIR specification is intended to be independent of any particular implementation context, **no elements are flagged as mustSupport=true as part of the base specification**.
 * This flag is intended for use in **profiles** that have a defined implementation context.
     ** The International Patient Summary is a profile.
 * For this reason, the specification itself never labels any elements as MustSupport.
 * This is done in StructureDefinitions, where the profile labels an element as mustSupport=true.
 * When a profile does this, it SHALL also make clear exactly what kind of "support" is required, as this could involve expectations around what a system must store, display, allow data capture of, include in decision logic, pass on to other data consumers, etc.
3. What does this mean for systems that produce an IPS document?
 * The group that manages the IPS Implementation Guide for HL7 is currently discussing if they need to make any changres in the wording in that profile.
4. What does this look like in the Implementaton Guide? We can use Immunization as an example. https://build.fhir.org/ig/HL7/fhir-ips/StructureDefinition-Immunization-uv-ips.html
 * In the upper tab: Select *Content*
 * In Section 14.3.1.1, select "Text Summary"
![Screenshot](../images/immunization-2.png)
 * There are now 13 *Must-Support* elements
 * IPS is working on the exact language for *Must-Support*
 * For today, assume: A system that creates an IPS document must be able to accept data tagged as MustSupport and include it when they produce a document.
5.  Select the *Differential Table* tab.
 * Note the red box with "S" inside. This stands for Must Support.
 * The screen capture shows several elements in this resource.
     * site remains cardinality 0..1
     * route has cardinality 0..1 but must be supported
     * performer has cardinality 0..* but must be supported
![Screenshot](../images/immunization-3.png)
 * In general, tools do not test for this today.
 * The way to test for this is to provide full clinical samples and ask the operator to import/enter the data and produce the relevant document.
     * Some systems may not have a way to record the data. They are not compliant.
     * In a testing session, I want to see the process used to collect the data to see if it matches a reasonable workflow.