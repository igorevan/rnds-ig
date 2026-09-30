# CapabilityStatement do EHR-Services da RNDS - Guia de Implementação da Rede Nacional de Dados em Saúde (RNDS) v1.0.0-release

## CapabilityStatement: CapabilityStatement do EHR-Services da RNDS 

 [Raw OpenAPI-Swagger Definition file](../CapabilityStatement-EHRServices.openapi.json) | [Download](../CapabilityStatement-EHRServices.openapi.json) 



## Resource Content

```json
{
  "resourceType" : "CapabilityStatement",
  "id" : "CapabilityStatement-EHRServices",
  "language" : "pt-BR",
  "extension" : [{
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-wg",
    "valueCode" : "ehr"
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-fmm",
    "valueInteger" : 1,
    "_valueInteger" : {
      "extension" : [{
        "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-conformance-derivedFrom",
        "valueCanonical" : "https://fhir.saude.gov.br/rnds/ImplementationGuide/br.gov.saude.rnds.fhir"
      }]
    }
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
    "valueCode" : "normative",
    "_valueCode" : {
      "extension" : [{
        "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-conformance-derivedFrom",
        "valueCanonical" : "https://fhir.saude.gov.br/rnds/ImplementationGuide/br.gov.saude.rnds.fhir"
      }]
    }
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-normative-version",
    "valueCode" : "4.0.1"
  }],
  "url" : "https://fhir.saude.gov.br/rnds/CapabilityStatement/CapabilityStatement-EHRServices",
  "version" : "1.0.0-release",
  "name" : "CapabilityStatement-EHRServices",
  "title" : "CapabilityStatement do EHR-Services da RNDS",
  "status" : "active",
  "date" : "2026-09-28T17:50:50.596-03:00",
  "publisher" : "Ministério da Saúde do Brasil",
  "contact" : [{
    "name" : "Ministério da Saúde do Brasil",
    "telecom" : [{
      "system" : "url",
      "value" : "http://www.saude.gov.br"
    },
    {
      "system" : "email",
      "value" : "cgiis.datasus@saude.gov.br"
    }]
  }],
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "kind" : "instance",
  "software" : {
    "name" : "RNDS FHIR R4 HML Server",
    "version" : "5.6.0"
  },
  "implementation" : {
    "description" : "HAPI FHIR",
    "url" : "https://ehr-services-hmg.saude.gov.br/1.15/api/fhir/r4"
  },
  "fhirVersion" : "4.0.1",
  "format" : ["application/fhir+xml", "xml", "application/fhir+json", "json"],
  "rest" : [{
    "mode" : "server",
    "resource" : [{
      "type" : "Bundle",
      "profile" : "http://hl7.org/fhir/StructureDefinition/Bundle",
      "interaction" : [{
        "code" : "create"
      },
      {
        "code" : "delete"
      },
      {
        "code" : "read"
      }],
      "searchInclude" : ["*"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"]
    },
    {
      "type" : "CodeSystem",
      "profile" : "http://hl7.org/fhir/StructureDefinition/CodeSystem",
      "searchInclude" : ["*"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"],
      "operation" : [{
        "name" : "lookup",
        "definition" : "https://ehr-services-hmg.saude.gov.br/1.15/api/fhir/r4/OperationDefinition/CodeSystem-t-lookup"
      }]
    },
    {
      "type" : "Composition",
      "profile" : "http://hl7.org/fhir/StructureDefinition/Composition",
      "interaction" : [{
        "code" : "read"
      },
      {
        "code" : "search-type"
      }],
      "searchInclude" : ["Composition:author", "Composition:subject"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"],
      "searchParam" : [{
        "name" : "subject",
        "type" : "reference",
        "documentation" : "Who and/or what the composition is about"
      },
      {
        "name" : "_bookmark",
        "type" : "string"
      },
      {
        "name" : "_count",
        "type" : "number"
      }],
      "operation" : [{
        "name" : "document",
        "definition" : "https://ehr-services-hmg.saude.gov.br/1.15/api/fhir/r4/OperationDefinition/Composition-i-document"
      }]
    },
    {
      "type" : "Consent",
      "profile" : "http://hl7.org/fhir/StructureDefinition/Consent",
      "interaction" : [{
        "code" : "read"
      },
      {
        "code" : "create"
      }],
      "searchInclude" : ["*"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"]
    },
    {
      "type" : "List",
      "profile" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRListaTimeline-1.0",
      "interaction" : [{
        "code" : "search-type"
      }],
      "searchInclude" : ["*", "List:subject"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"],
      "searchParam" : [{
        "name" : "code",
        "type" : "token",
        "documentation" : "What the purpose of this list is"
      },
      {
        "name" : "subject",
        "type" : "reference",
        "documentation" : "If all resources have the same subject"
      }]
    },
    {
      "type" : "OperationDefinition",
      "profile" : "http://hl7.org/fhir/StructureDefinition/OperationDefinition",
      "interaction" : [{
        "code" : "read"
      }],
      "searchInclude" : ["*"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"]
    },
    {
      "type" : "Organization",
      "profile" : "http://hl7.org/fhir/StructureDefinition/Organization",
      "interaction" : [{
        "code" : "read"
      },
      {
        "code" : "search-type"
      }],
      "searchInclude" : ["*"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"],
      "searchParam" : [{
        "name" : "identifier",
        "type" : "token",
        "documentation" : "Any identifier for the organization (not the accreditation issuer's identifier)"
      }]
    },
    {
      "type" : "Patient",
      "profile" : "http://rnds.saude.gov.br/fhir/r4/StructureDefinition/rnds-patient-1.0",
      "interaction" : [{
        "code" : "read"
      },
      {
        "code" : "search-type"
      }],
      "searchInclude" : ["*"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"],
      "searchParam" : [{
        "name" : "_bookmark",
        "type" : "string"
      },
      {
        "name" : "_count",
        "type" : "number"
      },
      {
        "name" : "birthdate",
        "type" : "date",
        "documentation" : "The patient's date of birth"
      },
      {
        "name" : "birthplace",
        "type" : "string"
      },
      {
        "name" : "gender",
        "type" : "string",
        "documentation" : "Gender of the patient"
      },
      {
        "name" : "mothers-name",
        "type" : "string"
      },
      {
        "name" : "name",
        "type" : "string",
        "documentation" : "A server defined search that may match any of the string fields in the HumanName, including family, give, prefix, suffix, suffix, and/or text"
      },
      {
        "name" : "identifier",
        "type" : "token",
        "documentation" : "A patient identifier"
      }]
    },
    {
      "type" : "Practitioner",
      "profile" : "http://rnds.saude.gov.br/fhir/r4/StructureDefinition/rnds-practitioner-1.0",
      "interaction" : [{
        "code" : "read"
      },
      {
        "code" : "search-type"
      }],
      "searchInclude" : ["*"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"],
      "searchParam" : [{
        "name" : "identifier",
        "type" : "token",
        "documentation" : "A practitioner's Identifier"
      }]
    },
    {
      "type" : "PractitionerRole",
      "profile" : "http://rnds.saude.gov.br/fhir/r4/StructureDefinition/rnds-practitionerrole-1.0",
      "interaction" : [{
        "code" : "read"
      },
      {
        "code" : "search-type"
      }],
      "searchInclude" : ["PractitionerRole:organization",
      "PractitionerRole:practitioner"],
      "searchRevInclude" : ["Composition:subject",
      "List:subject",
      "PractitionerRole:organization",
      "PractitionerRole:practitioner"],
      "searchParam" : [{
        "name" : "organization",
        "type" : "reference",
        "documentation" : "The identity of the organization the practitioner represents / acts on behalf of"
      },
      {
        "name" : "practitioner",
        "type" : "reference",
        "documentation" : "Practitioner that is able to provide the defined services for the organization"
      }]
    }]
  }]
}

```
