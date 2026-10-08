# Catálogo de Mensagens e Erros da RNDS - Guia de Implementação da Rede Nacional de Dados em Saúde (RNDS) v1.0.0-release

## CodeSystem: Catálogo de Mensagens e Erros da RNDS 

This Code system is referenced in the definition of the following value sets:

* [Mensagens e Erros da RNDS](ValueSet-RNDSErros.md)

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "RNDSErros",
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
  "url" : "http://www.saude.gov.br/fhir/r4/CodeSystem/RNDSErros",
  "version" : "1.0.0-release",
  "name" : "RNDSErros",
  "title" : "Catálogo de Mensagens e Erros da RNDS",
  "status" : "active",
  "experimental" : false,
  "date" : "2026-10-08T19:34:48-03:00",
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
  "description" : "Códigos de mensagens e erros documentados pela RNDS, baseados na Lista de Mensagens e Erros Apresentados pela RNDS, versão 3.0, 20/09/2024. A publicação não implica que todos os códigos permaneçam implementados.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "caseSensitive" : true,
  "content" : "complete",
  "property" : [{
    "code" : "mensagem",
    "uri" : "http://www.saude.gov.br/fhir/r4/CodeSystem/RNDSErros#mensagem",
    "description" : "Mensagem sistêmica apresentada pela RNDS",
    "type" : "string"
  },
  {
    "code" : "orientacao",
    "uri" : "http://www.saude.gov.br/fhir/r4/CodeSystem/RNDSErros#orientacao",
    "description" : "Orientação ao integrador, quando explicitamente presente no documento",
    "type" : "string"
  },
  {
    "code" : "tipoDocumento",
    "uri" : "http://www.saude.gov.br/fhir/r4/CodeSystem/RNDSErros#tipoDocumento",
    "description" : "Tipo de documento associado ao código, quando informado",
    "type" : "string"
  },
  {
    "code" : "situacaoDocumentada",
    "uri" : "http://www.saude.gov.br/fhir/r4/CodeSystem/RNDSErros#situacaoDocumentada",
    "description" : "Situação de implementação declarada no documento de origem",
    "type" : "code"
  },
  {
    "code" : "grupo",
    "uri" : "http://www.saude.gov.br/fhir/r4/CodeSystem/RNDSErros#grupo",
    "description" : "Grupo do catálogo de origem",
    "type" : "string"
  }],
  "concept" : [{
    "code" : "MSG001",
    "display" : "O CNS {0} não foi encontrado na base.",
    "definition" : "Necessário validar o CNS informado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O CNS {0} não foi encontrado na base."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG002",
    "display" : "Tipo de documento inválido para pesquisa do tipo list.",
    "definition" : "O documento informado está inválido. Verifique o documento e os parâmetros de pesquisa.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tipo de documento inválido para pesquisa do tipo list."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG003",
    "display" : "Usuário sem consentimento para acessar o documento {0}.",
    "definition" : "O consentimento não foi dado para o acesso ao documento enviado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Usuário sem consentimento para acessar o documento {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG004",
    "display" : "Usuário sem consentimento para acessar a timeline.",
    "definition" : "O consentimento não foi dado para o acesso à timeline.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Usuário sem consentimento para acessar a timeline."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG005",
    "display" : "O documento {0} não foi encontrado na base.",
    "definition" : "Não existe este documento na base RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento {0} não foi encontrado na base."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG006",
    "display" : "O documento {0} não foi encontrado na base.",
    "definition" : "Confirmação de exclusão efetuada",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento {0} não foi encontrado na base."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG007",
    "display" : "O documento referenciado para substituição no campo 'relatesTo' possui um 'identifier' que não é o mesmo do documento que foi substituído.",
    "definition" : "Necessário validar o dado do relatesTo com o documento a ser substituído, pois, há divergência de dados.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento referenciado para substituição no campo 'relatesTo' possui um 'identifier' que não é o mesmo do documento que foi substituído."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG008",
    "display" : "O documento {0} referenciado para substituição no 'relatesTo' não foi encontrado na base.",
    "definition" : "Necessário validar o documento referenciado, pois, o mesmo não foi localizado na base da RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento {0} referenciado para substituição no 'relatesTo' não foi encontrado na base."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG009",
    "display" : "O documento {0} já foi substituído.",
    "definition" : "Confirmação da substituição de documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento {0} já foi substituído."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, AS, SAO)."
    }]
  },
  {
    "code" : "MSG010",
    "display" : "Identifier duplicado.",
    "definition" : "O identificador fornecido como identifier, já foi registrado anteriormente, é preciso fornecer um novo ou validar o registro enviado anteriormente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Identifier duplicado."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "MSG011",
    "display" : "O documento {0} já existe.",
    "definition" : "Necessário validar o CNS informado e o documento informado, pois o documento enviado para este CNS já existe na base RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento {0} já existe."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "MSG012",
    "display" : "Consentimento não localizado.",
    "definition" : "O consentimento para o documento acessado não foi localizado na base da RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Consentimento não localizado."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "MSG013",
    "display" : "O campo issued deve ter data posterior a {0}. MM/DD/AAAA",
    "definition" : "Necessário validar a data cadastrada no campo issued conforme mensagem.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo issued deve ter data posterior a {0}. MM/DD/AAAA"
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    }]
  },
  {
    "code" : "MSG014",
    "display" : "O campo effective deve ter data posterior a {0}.",
    "definition" : "Necessário validar a data cadastrada no campo effective conforme mensagem.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo effective deve ter data posterior a {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    }]
  },
  {
    "code" : "MSG015",
    "display" : "Tipo de documento \"{0}\" não suportado.",
    "definition" : "Necessário verificar o tipo de documento enviado, pois o tipo enviado não é suportado pela RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tipo de documento \"{0}\" não suportado."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    }]
  },
  {
    "code" : "MSG016",
    "display" : "Documento incluído a partir do documento com docId \"{0}\" não pode ser modificado.",
    "definition" : "Como o documento foi feito a partir de um docId, não há possibilidade de modificação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Documento incluído a partir do documento com docId \"{0}\" não pode ser modificado."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    }]
  },
  {
    "code" : "MSG017",
    "display" : "Documento já existe na Base de Dados.",
    "definition" : "O documento que está sendo enviado já consta na base da RNDS, portanto, não é permitido novo envio para que não gere duplicidade.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Documento já existe na Base de Dados."
    },
    {
      "code" : "grupo",
      "valueString" : "Mensagem RNDS"
    }]
  },
  {
    "code" : "ERR779",
    "display" : "O medicamento deve ser informado em texto livre no campo \"MedicationRequest.note\"",
    "definition" : "O erro ocorre quando o documento FHIR é enviado e o campo MedicationRequest.note no perfil http://hl7.org/fhir/StructureDefinition/MedicationRequest está vazio.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O medicamento deve ser informado em texto livre no campo \"MedicationRequest.note\""
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR780",
    "display" : "Os campos de periodicidade (MedicationRequest.dosageInstruction.timing.repeat.extension:period.extension:periodUnit e ou MedicationRequest.dosageInstruction.tim",
    "definition" : "A validação é realizada quando a extensão do perfil http://www.saude.gov.br/fhir/r4/StructureDefinition/BRIntervaloDoses e a combinação das extensões period e periodUnit indicam que, se a quantidade máxima for maior que 1, o intervalo entre as doses está incompleto.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Os campos de periodicidade (MedicationRequest.dosageInstruction.timing.repeat.extension:period.extension:periodUnit e ou MedicationRequest.dosageInstruction.timing.repeat.extension:period.extension:period) devem ser preenchidos em caso de dose periódica ou contínua (MedicationRequest.dosageInstruction.timing.repeat.countMax)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR781",
    "display" : "Os campos de periodicidade (MedicationRequest.dosageInstruction.timing.repeat.extension:period e ou MedicationRequest.dosageInstruction.timing.repeat.extension:",
    "definition" : "O erro ocorre quando os campos MedicationRequest.dosageInstruction.timing.repeat.extension:period e MedicationRequest.dosageInstruction.timing.repeat.extension:when do profile http://www.saude.gov.br/fhir/r4/StructureDefinition/BRIntervaloDoses estão preenchidas para medicamentos onde a dose é única.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Os campos de periodicidade (MedicationRequest.dosageInstruction.timing.repeat.extension:period e ou MedicationRequest.dosageInstruction.timing.repeat.extension:when) não devem ser preenchidos em caso de dose única (MedicationRequest.dosageInstruction.timing.repeat.countMax)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR782",
    "display" : "A descrição sobre o uso do medicamento deve ser preenchida no campo \"MedicationRequest.note\" em caso de necessidade (MedicationRequest.dosageInstruction.asNeede",
    "definition" : "Quando a tag MedicationRequest.dosageInstruction.asNeeded[x] do profile http://www.saude.gov.br/fhir/r4/StructureDefinition/BRIntervaloDoses vem preenchida com a quantidade, este campo torna-se obrigatório o seu preenchimento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A descrição sobre o uso do medicamento deve ser preenchida no campo \"MedicationRequest.note\" em caso de necessidade (MedicationRequest.dosageInstruction.asNeeded[x])."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR783",
    "display" : "O valor \"{0}\" informado para o atributo \"operator\" nas informações demográficas de indivíduos que não podem ser identificados (paciente ou indivíduo não identif",
    "definition" : "Este erro é lançado quando o CNS informado pelo FHIR não existe dentro do Indice Patient do Elastic, retornando assim a mensagem.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O valor \"{0}\" informado para o atributo \"operator\" nas informações demográficas de indivíduos que não podem ser identificados (paciente ou indivíduo não identificado, unidentifiedPatient.extension:operator) não corresponde a um número de CNS, CPF ou CNES válido ({1})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR784",
    "display" : "A modalidade (Encounter.class) \"Atenção à Urgência/Emergência\" ({0}) não pode ter como caráter de atendimento (Encounter.priority.coding) \"Eletivo\" ({1}) ({2}).",
    "definition" : "É uma validação de CodeSystem, http://www.saude.gov.br/fhir/r4/CodeSystem/BRCaraterAtendimento, onde o CodeSystem http://www.saude.gov.br/fhir/r4/CodeSystem/BRModalidadeAssistencial definido como 6 não pode ter o Encounter.priority.coding preenchido como 01.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A modalidade (Encounter.class) \"Atenção à Urgência/Emergência\" ({0}) não pode ter como caráter de atendimento (Encounter.priority.coding) \"Eletivo\" ({1}) ({2})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR785",
    "display" : "A modalidade do contato assistencial (Encounter.class) não permite utilizar a fonte de financiamento informada para o procedimento realizado (Encounter.diagnosi",
    "definition" : "No CodeSystem http://www.saude.gov.br/fhir/r4/StructureDefinition/BRFinanciamento-1.0 o campo Encounter.class quando vier preenchido como 01 - Atenção Básica, não pode haver financiamento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A modalidade do contato assistencial (Encounter.class) não permite utilizar a fonte de financiamento informada para o procedimento realizado (Encounter.diagnosis:procedure.condition.extension:financier) ({0})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR786",
    "display" : "Não podem existir CBOs (Procedure.performer.function) duplicados para um mesmo profissional de saúde (Procedure.performer.actor) no mesmo procedimento ({0}).",
    "definition" : "Não podem ser enviados CBOs duplicados de um mesmo profissional de saúde (identificado pelo CNS fornecido) nos campos Procedure.performer.function e Procedure.performer.actor no mesmo registro de procedimento ({0}).",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não podem existir CBOs (Procedure.performer.function) duplicados para um mesmo profissional de saúde (Procedure.performer.actor) no mesmo procedimento ({0})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR787",
    "display" : "Não pode ser informado o(s) mesmo(s) código(s) ({0}) do(s) diagnóstico(s) principal(ais) (Encounter.reasonReference:primaryDiagnosis) para diagnósticos secundár",
    "definition" : "Validação de Diagnóstico Principal e Secundários, quando a terminologia de diagnóstico possuir marcador de diagnóstico principal, os diagnósticos secundários devem ser diferentes do diagnóstico principal. Está mensagem era exibida para o Conjunto Mínimo de Dados antes da unificação dos profiles: http://www.saude.gov.br/fhir/r4/StructureDefinition/BRCID10Avaliado-1.0 e http://www.saude.gov.br/fhir/r4/StructureDefinition/BRCID10AvaliadoANS-1.0.0",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não pode ser informado o(s) mesmo(s) código(s) ({0}) do(s) diagnóstico(s) principal(ais) (Encounter.reasonReference:primaryDiagnosis) para diagnósticos secundários (Encounter.diagnosis:diagnosis) no mesmo contato assistencial ({1})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR788",
    "display" : "Diagnóstico secundário duplicado",
    "definition" : "Quando são enviados mais de um diagnóstico secundário Encounter.diagnosis:diagnosis, os códigos enviados não podem ser duplicados para o campo Condition.code.coding, caracterizando duplicidade de diagnóstico.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não podem existir vários diagnósticos secundários (Encounter.diagnosis:diagnosis) com o mesmo código (Condition.code.coding: {0}) no mesmo contato assistencial ({1})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR789",
    "display" : "Não podem existir vários procedimentos com o mesmo código (Procedure.code.coding: {0}) e data de realização (Procedure.performedDateTime: {1}) no mesmo contato",
    "definition" : "Validação de Procedimentos e data, em um registro de contato assistencial não será permitido informar procedimentos (ações) iguais para a mesma data de realização.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não podem existir vários procedimentos com o mesmo código (Procedure.code.coding: {0}) e data de realização (Procedure.performedDateTime: {1}) no mesmo contato assistencial ({2})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR790",
    "display" : "Para a fonte de financiamento informada (Encounter.diagnosis:procedure.condition.extension:financier) é obrigatório informar o profissional responsável (Procedu",
    "definition" : "Obrigatoriedade de identificação do profissional, informação do CNS do profissional deverá ser obrigatória para cada CBO informado quando o financiamento for selecionado para o SUS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Para a fonte de financiamento informada (Encounter.diagnosis:procedure.condition.extension:financier) é obrigatório informar o profissional responsável (Procedure.performer) pelo procedimento ({0})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR791",
    "display" : "Para a modalidade assistencial (Composition.category.coding.code) informada ({0}) o período entre datas de admissão (Encounter.period.start) e desfecho (Encount",
    "definition" : "Caso seja informado em modalidade assistencial “04 - Atenção Hospitalar” deve-se validar se a data do desfecho menos a data de admissão é maior ou igual a 1 dia, exceto nos casos em que o desfecho for igual a “06 - Óbito” ou “09 - Transferência.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Para a modalidade assistencial (Composition.category.coding.code) informada ({0}) o período entre datas de admissão (Encounter.period.start) e desfecho (Encounter.period.end) deve ser igual ou maior a 1 (um) dia {1}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR792",
    "display" : "Para a modalidade assistencial (Composition.category.coding.code) informada ({0}) o período entre datas de admissão (Encounter.period.start) e desfecho (Encount",
    "definition" : "Caso seja informado em modalidade assistencial “04 - Atenção Hospitalar” deve-se validar se a data do desfecho menos a data de admissão é maior ou igual a 1 dia, exceto nos casos em que o desfecho for igual a “06 - Óbito” ou “09 - Transferência.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Para a modalidade assistencial (Composition.category.coding.code) informada ({0}) o período entre datas de admissão (Encounter.period.start) e desfecho (Encounter.period.end) deve ser igual ou maior a 1 (um) dia {1}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR793",
    "display" : "Para a modalidade assistencial (Composition.category.coding.code) informada ({0}) as datas de admissão (Encounter.period.start) e desfecho (Encounter.period.end",
    "definition" : "Caso seja informada a modalidade assistencial “01 - Atenção básica” ou “07 - Ambulatorial especializado” a data de admissão e data do desfecho devem ser iguais.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Para a modalidade assistencial (Composition.category.coding.code) informada ({0}) as datas de admissão (Encounter.period.start) e desfecho (Encounter.period.end) devem ser iguais {1}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR794",
    "display" : "A data de realização do procedimento (Procedure.performedDateTime) deve ser igual a data de admissão (Encounter.period.start) para a modalidade (Encounter.class",
    "definition" : "A data de realização do procedimento Procedure.performedDateTime deve ser igual a data de admissão Encounter.period.start informada na modalidade do Contato Assistencial: [01 - Atenção básica | 07 - Ambulatorial Especializado].",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de realização do procedimento (Procedure.performedDateTime) deve ser igual a data de admissão (Encounter.period.start) para a modalidade (Encounter.class.code) {0}{1}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR795",
    "display" : "A data de desfecho (Encounter.period.end) não pode ser informada para o tipo de desfecho (Encounter.hospitalization.dischargeDisposition.coding) \"{0}\" ({1}).",
    "definition" : "Para os códigos: 01 - Atenção básica e 07 - Ambulatorial especializado",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de desfecho (Encounter.period.end) não pode ser informada para o tipo de desfecho (Encounter.hospitalization.dischargeDisposition.coding) \"{0}\" ({1})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR796",
    "display" : "A data de desfecho (Encounter.period.end) não pode ser inferior a data de realização do procedimento (Procedure.performedDateTime){0}.",
    "definition" : "Valida se a data de desfecho está inferior à data de realização do procedimento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de desfecho (Encounter.period.end) não pode ser inferior a data de realização do procedimento (Procedure.performedDateTime){0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR797",
    "display" : "A data de admissão (Encounter.period.start) não pode ser superior a data de realização do procedimento (Procedure.performedDateTime){0}.",
    "definition" : "Valida se a data de admissão está superior a data de realização do procedimento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de admissão (Encounter.period.start) não pode ser superior a data de realização do procedimento (Procedure.performedDateTime){0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR798",
    "display" : "A data de desfecho (Encounter.period.end) não pode ser superior a data de óbito do indivíduo (Encounter.subject, Patient.deceased).",
    "definition" : "Valida se existe data de óbito para o paciente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de desfecho (Encounter.period.end) não pode ser superior a data de óbito do indivíduo (Encounter.subject, Patient.deceased)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR799",
    "display" : "A data de desfecho (Encounter.period.end) não pode ser inferior a data de nascimento do indivíduo (Encounter.subject, Patient.birthDate).",
    "definition" : "Valida se o paciente não possui uma data de nascimento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de desfecho (Encounter.period.end) não pode ser inferior a data de nascimento do indivíduo (Encounter.subject, Patient.birthDate)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR800",
    "display" : "A data de admissão (Encounter.period.start) não pode ser superior a data de óbito do indivíduo (Encounter.subject, Patient.deceased).",
    "definition" : "Valida se a data de procedimento informada é superior a data de óbito do paciente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de admissão (Encounter.period.start) não pode ser superior a data de óbito do indivíduo (Encounter.subject, Patient.deceased)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR801",
    "display" : "A data de admissão (Encounter.period.start) não pode ser inferior a data de nascimento do indivíduo (Encounter.subject, Patient.birthDate).",
    "definition" : "Valida se a data de procedimento está anterior à data de nascimento do paciente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de admissão (Encounter.period.start) não pode ser inferior a data de nascimento do indivíduo (Encounter.subject, Patient.birthDate)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR802",
    "display" : "Código \"{0}#{1}\" não definido para a competência/versão {2} (\"{3}\").",
    "definition" : "Validação do código do procedimento não está de acordo com a competência.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Código \"{0}#{1}\" não definido para a competência/versão {2} (\"{3}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR803",
    "display" : "Combinação de tipo de exame (Observation.code) e interpretação (Observation.interpretation) não permitida (\"{0}\").",
    "definition" : "Necessário verificar se a combinação entre tipo de exame e interpretações está correta. Necessário ter: Um profile definido, ou seja, não pode ser padrão. Tipo de exame. Interpretação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Combinação de tipo de exame (Observation.code) e interpretação (Observation.interpretation) não permitida (\"{0}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR804",
    "display" : "Combinação de tipo de exame (Observation.code) e resultado (Observation.valueCodeableConcept) não permitida (\"{0}\").",
    "definition" : "Necessário verificar a combinação entre tipo de exame e tipo de resultado. Tem que ter um profile definido, ou seja, não pode ser padrão. Tipo de exame. Resultado qualitativo.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Combinação de tipo de exame (Observation.code) e resultado (Observation.valueCodeableConcept) não permitida (\"{0}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR805",
    "display" : "Combinação de tipo de exame (Observation.code) e patógeno (Observation.extension:pathogen) não permitida (\"{0}\").",
    "definition" : "Necessário verificar a combinação entre tipo de exame e patógeno é permitida. Tem que ter um profile definido, ou seja, não pode ser padrão. Tipo de exame. A extensão de patógeno.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Combinação de tipo de exame (Observation.code) e patógeno (Observation.extension:pathogen) não permitida (\"{0}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR806",
    "display" : "O campo \"Observation.interpretation\" não foi informado (\"{0}\").",
    "definition" : "Necessário verificar se foi informado o campo Observation#getValueQuantity() juntamente com o campo Observation#getInterpretation().",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo \"Observation.interpretation\" não foi informado (\"{0}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR807",
    "display" : "O campo \"timestamp\" do \"Bundle\" não pode ter data anterior à data atual.",
    "definition" : "Deve-se usar a data atual para o envio. Caso seja enviado datas no passado, a RNDS recusará.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo \"timestamp\" do \"Bundle\" não pode ter data anterior à data atual."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR808",
    "display" : "O campo \"timestamp\" do \"Bundle\" não pode ter data posterior à data atual.",
    "definition" : "Deve-se usar a data atual para o envio. Caso seja enviado datas no passado, a RNDS recusará.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo \"timestamp\" do \"Bundle\" não pode ter data posterior à data atual."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR809",
    "display" : "O campo \"Observation.effective\" deve ter data posterior a {0} (\"{1}\").",
    "definition" : "Necessário verificar a data mínima para o campo Observation#getEffectiveDateTimeType() ou Observation#getEffectiveInstantType()}.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo \"Observation.effective\" deve ter data posterior a {0} (\"{1}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR810",
    "display" : "O campo \"Observation.issued\" deve ter data posterior a {0} (\"{1}\").",
    "definition" : "Necessário verificar a data mínima para o campo Observation#getIssued().",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo \"Observation.issued\" deve ter data posterior a {0} (\"{1}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR811",
    "display" : "Apenas o Composition \"raiz\" (aquele que não é referenciado por outros elementos no Bundle) pode possuir o atributo relatesTo (referente ao item \"{0}\").",
    "definition" : "Necessário verificar se apenas o Composition \"raiz\" possui o atributo relatesTo.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Apenas o Composition \"raiz\" (aquele que não é referenciado por outros elementos no Bundle) pode possuir o atributo relatesTo (referente ao item \"{0}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR812",
    "display" : "O documento pode ter apenas um Composition \"raiz\" (aquele que não é referenciado por outros elementos no Bundle).",
    "definition" : "Necessário validar se o Composition possui mais que 1 id.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento pode ter apenas um Composition \"raiz\" (aquele que não é referenciado por outros elementos no Bundle)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR813",
    "display" : "O documento deve ter pelo menos um Composition \"raiz\" (aquele que não é referenciado por outros elementos no Bundle).",
    "definition" : "Necessário validar se o Composition está nulo ou vazio.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento deve ter pelo menos um Composition \"raiz\" (aquele que não é referenciado por outros elementos no Bundle)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR814",
    "display" : "O documento {0} possui um tipo de documento FHIR inválido e não pode ser processado: {1}.",
    "definition" : "Necessário validar se a informação está preenchida e é maior que 0.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento {0} possui um tipo de documento FHIR inválido e não pode ser processado: {1}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR815",
    "display" : "Code \"{0}\" inativo (referente ao item \"{1}\").",
    "definition" : "Necessário validar se o grupo de atendimento está inativo. Caso esteja inativo, a imunização é rejeitada.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Code \"{0}\" inativo (referente ao item \"{1}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR816",
    "display" : "Devem ser informados os dados da pesquisa clínica registrada na ANVISA que realizou a administração do imunobiológico (referente ao item \"{0}\").",
    "definition" : "Necessário validar se a imunização está relacionada a um estudo clínico para o desenvolvimento de imunobiológico e possui as informações para identificar a pesquisa clínica. Uma imunização está relacionada a um estudo clínico quando possuir o profile FhirProperties.Profile#BRImunobiologicoAdministrado_2_0 BRImunobiologicoAdministrado_2_0 e o valor da extensão FhirProperties.Extension#BREstrategiaVacinacao BREstrategiaVacinacao for \"pesquisa>\" (de acordo com o Code System FhirProperties.CodeSystem#BREstrategiaVacinacao BREstrategiaVacinacao}). Quando uma imunização está relacionada a um estudo clínico a extensão FhirProperties.Extension#BREstrategiaVacinacaoPesquisa BREstrategiaVacinacaoPesquisa tem que ter sido informada (os campos obrigatórios para a extensão são verificados pelo validador).",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Devem ser informados os dados da pesquisa clínica registrada na ANVISA que realizou a administração do imunobiológico (referente ao item \"{0}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR817",
    "display" : "Só é permitida no máximo {0} imunizações para o imunobiológico de código \"{1}\" por paciente e por UF.",
    "definition" : "De acordo com as regras estipuladas para cada imunobiológico de código \"{ }\" é definida a quantidade máxima de imunizações por paciente e por UF.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Só é permitida no máximo {0} imunizações para o imunobiológico de código \"{1}\" por paciente e por UF."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "orientacao",
      "valueString" : "Verifique se a imunização não extrapola o limite de imunizações por UF e por imunobiológico."
    }]
  },
  {
    "code" : "ERR818",
    "display" : "Configurações de validações FHIR inválidas.",
    "definition" : "Necessário validar os códigos possíveis com base no CodeSystem de cada tipo de Profile e Documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Configurações de validações FHIR inválidas."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR819",
    "display" : "Código de imunobiológico informado \"{0}\" é inválido (referente ao item \"{1}\").",
    "definition" : "Necessário validar se existem códigos secundários iguais para o tipo de documento de vacina.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Código de imunobiológico informado \"{0}\" é inválido (referente ao item \"{1}\")."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR820",
    "display" : "Profissional {0} não autorizado, pois não faz parte da equipe que atende ao paciente com CNS {1}. deve ser maior que zero ({0}).",
    "definition" : "Necessário validar se o índice Practitioner existe o Paciente na junção do índice Patient.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Profissional {0} não autorizado, pois não faz parte da equipe que atende ao paciente com CNS {1}. deve ser maior que zero ({0})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR821",
    "display" : "Profissional {0} não autorizado, pois não possui CRM.",
    "definition" : "Necessário validar se o índice Practitioner existe a tag CRM.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Profissional {0} não autorizado, pois não possui CRM."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR822",
    "display" : "O identifier pesquisado apresentou inconsistência de integridade na hierarquia de substituições de documentos (relatesTo) e não pode ser pesquisado.",
    "definition" : "Necessário validar a hierarquia na tag relatesTo.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O identifier pesquisado apresentou inconsistência de integridade na hierarquia de substituições de documentos (relatesTo) e não pode ser pesquisado."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR823",
    "display" : "Informação referente ao item \"{0}\" já existe no repositório. O ID existente é {1}.",
    "definition" : "A RNDS não permite registros duplicados. Desta forma, a mensagem de erro informa que a informação que está sendo inserida já está na RNDS e não poderá ser incluída novamente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Informação referente ao item \"{0}\" já existe no repositório. O ID existente é {1}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "orientacao",
      "valueString" : "O registo da informação já está cadastrado no banco de dados. Necessário validar se o registro está em duplicidade no sistema de origem."
    }]
  },
  {
    "code" : "ERR824",
    "display" : "Item \"{0}\" repetido na requisição.",
    "definition" : "Necessário validar se a informação está se repetindo dentro da imunização.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Item \"{0}\" repetido na requisição."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR825",
    "display" : "Para realizar a exclusão, o status do documento deve ser \"{0}\".",
    "definition" : "Necessário validar se o documento está com status de final. Em final não é possível a exclusão. É preciso alterar o status para DELETED.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Para realizar a exclusão, o status do documento deve ser \"{0}\"."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR826",
    "display" : "Você não possui autorização para excluir documentos desse sistema de origem: {0}.",
    "definition" : "Necessário verificar se o sistema solicitante tem permissão para realizar o Delete do documento FHIR.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Você não possui autorização para excluir documentos desse sistema de origem: {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR827",
    "display" : "Documento com o ID \"{0}\" não encontrado.",
    "definition" : "Necessário verificar se o documento possui uma auditoria para realizar o delete, pois, esta mensagem ocorre quando não é encontrado o documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Documento com o ID \"{0}\" não encontrado."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR828",
    "display" : "Ocorreu um erro ao tentar preparar a mensagem para agendamento de processamento (conversão doc FHIR original).",
    "definition" : "Este erro está inativado no código.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ocorreu um erro ao tentar preparar a mensagem para agendamento de processamento (conversão doc FHIR original)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR829",
    "display" : "Não encontrado.",
    "definition" : "Esse erro ocorre quando a aplicação apresenta um erro não catalogado na RNDS. Necessário acionar o suporte.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não encontrado."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR830",
    "display" : "Data futura inválida",
    "definition" : "A data informada no campo Immunization.occurrenceDateTime deve ser igual ou menor que a data atual, no momento do envio do registro.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data deve ser igual ou menor que a data atual ({0})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR831",
    "display" : "Tipo de referência inválida para profissional de saúde: {0}.",
    "definition" : "Necessário verificar se o Performer.actor é válido.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tipo de referência inválida para profissional de saúde: {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR832",
    "display" : "{0} não encontrado ({1}).",
    "definition" : "Caso não tenha sido informado o \"performer\" o \"reportOrigin\" tem que indicar se se trata de uma transcrição de caderneta de vacinação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "{0} não encontrado ({1})."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "orientacao",
      "valueString" : "Necessário verificar algum dado que é obrigatório apesar de ser definido como opcional no profile."
    }]
  },
  {
    "code" : "ERR833",
    "display" : "Os dados de autenticação informados são inválidos! Sistema solicitante {0} não autorizado!",
    "definition" : "Necessário verificar credenciais de INTEGRADORES na base do SCAB.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Os dados de autenticação informados são inválidos! Sistema solicitante {0} não autorizado!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR834",
    "display" : "Não foi possível ler o MANIFEST.MF",
    "definition" : "A aplicação não conseguiu ler arquivo de configuração denominada MANIFEST.MF.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível ler o MANIFEST.MF"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR835",
    "display" : "Token gov.br não autorizado! Usuário do token não possui todos os selos de confiabilidade cadastrais necessários.",
    "definition" : "Falha na verificação de selos gov.br. token.getSub(): {} | selosPrincipal: {} | audience.getSelos(): {}",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Token gov.br não autorizado! Usuário do token não possui todos os selos de confiabilidade cadastrais necessários."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "orientacao",
      "valueString" : "Verifique o perfil/selo do gov.br exigido e o utilizado."
    }]
  },
  {
    "code" : "ERR836",
    "display" : "Não foi possível validar o token gov.br. Resposta da API de Autenticação gov.br não condiz com contrato de serviço.",
    "definition" : "HTTP CODE não tratado devido a inconsistência entre requisição e tipo de requisições aprovada para o contrato RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível validar o token gov.br. Resposta da API de Autenticação gov.br não condiz com contrato de serviço."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR837",
    "display" : "Não foi possível validar o token gov.br. Erro ao processar resposta da API de Autenticação gov.br.",
    "definition" : "Erro de comunicação com o gov.br. Não se trata de erro RNDS, portanto, não é necessário acionar o suporte MS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível validar o token gov.br. Erro ao processar resposta da API de Autenticação gov.br."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR838",
    "display" : "Não foi possível validar o token gov.br. Tempo máximo de comunicação atingido ao tentar estabelecer comunicação com API de Autenticação gov.br.",
    "definition" : "Timeout de comunicação com o gov.br. Não se trata de erro RNDS, portanto, não é necessário acionar o suporte MS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível validar o token gov.br. Tempo máximo de comunicação atingido ao tentar estabelecer comunicação com API de Autenticação gov.br."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR839",
    "display" : "Não foi possível validar o token gov.br. A API de Autenticação gov.br não está disponível.",
    "definition" : "Falha de comunicação com o gov.br. Não se trata de erro RNDS, portanto, não é necessário acionar o suporte MS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível validar o token gov.br. A API de Autenticação gov.br não está disponível."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR840",
    "display" : "Não foi possível validar o token gov.br. Erro ao tentar estabelecer comunicação com a API de Autenticação gov.br.",
    "definition" : "Falha de comunicação com o gov.br. Não se trata de erro RNDS, portanto, não é necessário acionar o suporte MS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível validar o token gov.br. Erro ao tentar estabelecer comunicação com a API de Autenticação gov.br."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR841",
    "display" : "Identifier inválido: system=[{0}], value=[{1}]",
    "definition" : "Necessário validar se existe um identifier vindo do certificado gerado pelo SCAB.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Identifier inválido: system=[{0}], value=[{1}]"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR842",
    "display" : "Acesso à API de Validação de Perfis não autorizada.",
    "definition" : "Necessário validar a informação com base no identifier e verificar os dados com o índice do Elastic.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Acesso à API de Validação de Perfis não autorizada."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR843",
    "display" : "Resposta da API de Validação de Perfis não condiz com contrato de serviço",
    "definition" : "Trata-se de erro genérico gerado pelo serviço REST.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Resposta da API de Validação de Perfis não condiz com contrato de serviço"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR844",
    "display" : "Erro ao processar resposta da API de Validação de Perfis.",
    "definition" : "Necessário efetuar nova validação do bundle da credencial.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao processar resposta da API de Validação de Perfis."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR845",
    "display" : "Tempo máximo de comunicação atingido ao tentar comunicar com a API de Validação de Perfis",
    "definition" : "Timeout da comunicação por instabilidade ou lentidão da rede.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tempo máximo de comunicação atingido ao tentar comunicar com a API de Validação de Perfis"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR846",
    "display" : "API de Validação de Perfis não está disponível",
    "definition" : "Trata-se de indisponibilidade da API.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "API de Validação de Perfis não está disponível"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR847",
    "display" : "Erro ao tentar estabelecer comunicação com a API de Validação de Perfis",
    "definition" : "Trata-se de indisponibilidade da API.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao tentar estabelecer comunicação com a API de Validação de Perfis"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR848",
    "display" : "O parâmetro 'bookmark' utilizado para a pesquisa paginada é inválido ou expirou.",
    "definition" : "Necessário verificar a paginação utilizando o ElasticSearch.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O parâmetro 'bookmark' utilizado para a pesquisa paginada é inválido ou expirou."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR849",
    "display" : "Para realizar essa pesquisa é necessário informar uma das combinações mínimas de parâmetros: Opção A - dois parâmetros principais (name, mothers-name); Opção B",
    "definition" : "Necessário verificar se atende a necessidade de ter pelo menos 1 parâmetro principal presente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Para realizar essa pesquisa é necessário informar uma das combinações mínimas de parâmetros: Opção A - dois parâmetros principais (name, mothers-name); Opção B - um parâmetro principal (name, mothers-name) e um parâmetro secundário (birthdate, birthplace)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR850",
    "display" : "O parâmetro {0} é inválido, {1}.",
    "definition" : "Necessário atender os parâmetros do código IBGE que tem 6 caracteres, somente números.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O parâmetro {0} é inválido, {1}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR851",
    "display" : "O parâmetro {0} é inválido, pois não é permitido nenhum tipo de modificador ou qualificador.",
    "definition" : "Necessário atender à exigência de não usar modifier.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O parâmetro {0} é inválido, pois não é permitido nenhum tipo de modificador ou qualificador."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR852",
    "display" : "É obrigatório informar pelo menos os campos 'system' e 'code' para executar essa operação.",
    "definition" : "Necessário validar os filtros obrigatórios.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar pelo menos os campos 'system' e 'code' para executar essa operação."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR853",
    "display" : "Acesso à API de Notificação não autorizada",
    "definition" : "Necessário validar a permissão para acessar a API de Notificação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Acesso à API de Notificação não autorizada"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR854",
    "display" : "Resposta da API de Notificação não condiz com contrato de serviço",
    "definition" : "HTTP CODE não tratado devido a inconsistência entre requisição e tipo de requisições aprovada para o contrato RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Resposta da API de Notificação não condiz com contrato de serviço"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR855",
    "display" : "Erro ao processar resposta da API de Notificação",
    "definition" : "Erro de comunicação da API.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao processar resposta da API de Notificação"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR856",
    "display" : "Tempo máximo de comunicação atingido ao tentar comunicar com API de Notificação",
    "definition" : "Timeout da API de Notificação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tempo máximo de comunicação atingido ao tentar comunicar com API de Notificação"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR857",
    "display" : "API de Notificação não está disponível",
    "definition" : "Falha de comunicação com a API.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "API de Notificação não está disponível"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR858",
    "display" : "Erro ao tentar estabelecer comunicação com o API de Notificação",
    "definition" : "Falha de comunicação com a API Notificação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao tentar estabelecer comunicação com o API de Notificação"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR859",
    "display" : "Ocorreu um erro ao tentar notificar o paciente da geração do contexto de atendimento",
    "definition" : "Falha na hora de enviar uma notificação ao patient.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ocorreu um erro ao tentar notificar o paciente da geração do contexto de atendimento"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR860",
    "display" : "Parâmetro 'bookmark' para paginação é inválido",
    "definition" : "Falha na consulta paginada do Elastic.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Parâmetro 'bookmark' para paginação é inválido"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR861",
    "display" : "Operação inexistente ou não suportada.",
    "definition" : "Trata-se de um tratamento para Bad Request, tratamento de exceção usado para operação não aceita na RNDS - erro HTPP 400.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Operação inexistente ou não suportada."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR862",
    "display" : "O documento {0} possui um perfil inválido e não pode ser processado: {1}",
    "definition" : "Necessário validar se o perfil que está contido no documento FHIR, pois há alguma inconsistência impedindo o envio e a gravação na base.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento {0} possui um perfil inválido e não pode ser processado: {1}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR863",
    "display" : "Banco de dados de cache respondeu à pesquisa com erro, indicando que o índice não existe: {0}",
    "definition" : "Foi feita uma consulta de um índice no Elastic que não existe. Necessário validar o índice consultado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Banco de dados de cache respondeu à pesquisa com erro, indicando que o índice não existe: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR864",
    "display" : "Ocorreu um erro não esperado ao tentar acessar o banco de dados de cache.",
    "definition" : "Falha de comunicação com o Elastic.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ocorreu um erro não esperado ao tentar acessar o banco de dados de cache."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR865",
    "display" : "Ocorreu um erro ao tentar processar os dados do índice {0} do banco de dados de cache.",
    "definition" : "Falha de comunicação com o Elastic.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ocorreu um erro ao tentar processar os dados do índice {0} do banco de dados de cache."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR866",
    "display" : "O identifier informado já foi utilizado para cadastrar outro documento e não pode ser repetido. O id existente é {0}.",
    "definition" : "Necessário validar se o identifier já foi utilizado, pois, esta mensagem informa que há duplicidade dos dados.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O identifier informado já foi utilizado para cadastrar outro documento e não pode ser repetido. O id existente é {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR867",
    "display" : "O valor informado no campo 'targetReference' do atributo relatesTo é inválido.",
    "definition" : "Necessário validar as informações do documento FHIR dentro da tag relatesTo.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O valor informado no campo 'targetReference' do atributo relatesTo é inválido."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR868",
    "display" : "O valor informado no campo 'code' do atributo relatesTo é inválido. Só é permitido o uso do code 'replaces'.",
    "definition" : "Necessário validar o tipo de código do documento dentro da tag relatesTo",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O valor informado no campo 'code' do atributo relatesTo é inválido. Só é permitido o uso do code 'replaces'."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR869",
    "display" : "O atributo relatesTo permite apontar apenas 01 (um) documento para substituição.",
    "definition" : "Há um limite máximo de relatesTo. Necessário validar se este limite foi excedido.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O atributo relatesTo permite apontar apenas 01 (um) documento para substituição."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR870",
    "display" : "Documento referenciado no atributo 'relatesTo' já foi substituído em outra transação e não pode ser substituído novamente.",
    "definition" : "Só é permitido realizar uma substituição por um documento FHIR.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Documento referenciado no atributo 'relatesTo' já foi substituído em outra transação e não pode ser substituído novamente."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR872",
    "display" : "O documento referenciado para substituição no campo 'relatesTo' possui um 'identifier' que não é o mesmo do documento que o substitui. Para substituir um docume",
    "definition" : "O identifier tem que ser idêntico ao documento original para que ele consiga realizar a substituição do documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento referenciado para substituição no campo 'relatesTo' possui um 'identifier' que não é o mesmo do documento que o substitui. Para substituir um documento, o valor do campo 'identifier' do documento sendo substituído e do documento que o substitui devem ser iguais."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR875",
    "display" : "Documento para substituição, indicado no atributo relatesTo, não foi encontrado. Confira o id informado para o documento original, seu tipo e a UF onde este doc",
    "definition" : "Necessário validar as informações do campo relatesTo para substituição conforme o documento original a ser substituído.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Documento para substituição, indicado no atributo relatesTo, não foi encontrado. Confira o id informado para o documento original, seu tipo e a UF onde este documento está armazenado. Só é possível fazer substituição de documentos do mesmo tipo e na mesma UF."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR876",
    "display" : "O documento consultado referencia um paciente que não está presente na base de dados!",
    "definition" : "Necessário validar se o dado está contido no índice Patient.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento consultado referencia um paciente que não está presente na base de dados!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR877",
    "display" : "É obrigatório informar pelo menos um parâmetro de pesquisa, seja um identificador de Profissional ou um identificador de Organização.",
    "definition" : "Necessário validar os filtros para cruzamento de dados dentro do Elastic.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar pelo menos um parâmetro de pesquisa, seja um identificador de Profissional ou um identificador de Organização."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR878",
    "display" : "Configuração de GOV.BR Audience {0} inválida!",
    "definition" : "Validação do gov.br. Não se trata de erro RNDS. Este erro está relacionado ao gov.br.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Configuração de GOV.BR Audience {0} inválida!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR879",
    "display" : "Profissional {0} não autorizado, pois não possui vínculo CBO autorizado no CNES {1} solicitado.",
    "definition" : "Necessário validar o Practitioner e sua relação de CNES cadastrado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Profissional {0} não autorizado, pois não possui vínculo CBO autorizado no CNES {1} solicitado."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR880",
    "display" : "Você não possui autorização para enviar documentos para esta UF.",
    "definition" : "Necessário validar o índice cnes_acesso_idx, permissão por estado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Você não possui autorização para enviar documentos para esta UF."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR881",
    "display" : "Você não possui autorização para utilizar esse sistema de origem: {0}.",
    "definition" : "Necessário validar o índice cnes_acesso_idx, permissão por sistema.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Você não possui autorização para utilizar esse sistema de origem: {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR882",
    "display" : "O token de certificado usado para autorizar o acesso não é válido. {0}",
    "definition" : "Necessário validar o índice cnes_acesso_idx, permissão do token cadastrado vs o que foi enviado no login.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O token de certificado usado para autorizar o acesso não é válido. {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR883",
    "display" : "Os dados de autenticação informados são inválidos! Token com identificador {0} não possui sistemas autorizados!",
    "definition" : "Necessário validar o índice cnes_acesso_idx, permissão por sistema.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Os dados de autenticação informados são inválidos! Token com identificador {0} não possui sistemas autorizados!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR884",
    "display" : "Os dados de autenticação informados são inválidos! Token com identificador {0} não autorizado!",
    "definition" : "Necessário validar o índice cnes_acesso_idx, permissão utlizando a tag sistemaPermitido = true.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Os dados de autenticação informados são inválidos! Token com identificador {0} não autorizado!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR885",
    "display" : "Code System não encontrado: {0}",
    "definition" : "Necessário validar o CodeSystem do tipo de documento REL. Gera o sumário para RESULTADO_EXAME_LABORATORIAL.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Code System não encontrado: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR886",
    "display" : "Profile de organização inválido.",
    "definition" : "Esse código de profile de organização não foi encontrado da RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Profile de organização inválido."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR887",
    "display" : "É obrigatório informar o profile ao enviar um documento.",
    "definition" : "Necessário validar o documento, pois, não consta um profile válido.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar o profile ao enviar um documento."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR888",
    "display" : "O tipo de documento EHR é inválido.",
    "definition" : "Necessário validar se o tipo de documento está cadastrado na RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O tipo de documento EHR é inválido."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR889",
    "display" : "O tipo de lista é obrigatório.",
    "definition" : "Necessário validar a lista de códigos se está nula ou vazia.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O tipo de lista é obrigatório."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR890",
    "display" : "O tipo de lista informado é inválido: {0}",
    "definition" : "Necessário verificar a autorização para realizar consulta/pesquisa de lista.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O tipo de lista informado é inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR891",
    "display" : "Ocorreu um erro ao tentar gerar o sumário do documento.",
    "definition" : "Gerar sumário de acordo com tipo de documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ocorreu um erro ao tentar gerar o sumário do documento."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR892",
    "display" : "O documento {0} possui um sumário inválido e não pode ser processado.",
    "definition" : "Necessário validar se o sumário enviado está cadastrado dentro da RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento {0} possui um sumário inválido e não pode ser processado."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR893",
    "display" : "O tamanho da página deve ter um valor entre 1 e {0}",
    "definition" : "Necessário validar o tamanho da paginação dentro do Elastic.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O tamanho da página deve ter um valor entre 1 e {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR894",
    "display" : "Parâmetro para tamanho de página é inválido.",
    "definition" : "Trata-se de validação do Elastic.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Parâmetro para tamanho de página é inválido."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR895",
    "display" : "CNS {0} do paciente não foi encontrado na base do EHR Data Services!",
    "definition" : "Necessário validar na base de consentimento se o CNS está cadastrado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "CNS {0} do paciente não foi encontrado na base do EHR Data Services!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR896",
    "display" : "Erro de colisão de IDs ao gravar documento no EHR Data Services!",
    "definition" : "Necessário validar o envio de IDs que já existem na base.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro de colisão de IDs ao gravar documento no EHR Data Services!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR897",
    "display" : "Você não possui autorização para cadastrar documentos para os seguintes autores/estabelecimentos: {0}.",
    "definition" : "Necessário validar se o certificado enviado tem permissão com o sumário + listas de sistemas permitidos.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Você não possui autorização para cadastrar documentos para os seguintes autores/estabelecimentos: {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR898",
    "display" : "Só é permitido solicitar contexto de atendimento para o mesmo profissional de saúde que é operador dessa requisição.",
    "definition" : "Valida se o practitioner é o mesmo do usuário que está sendo atendido.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Só é permitido solicitar contexto de atendimento para o mesmo profissional de saúde que é operador dessa requisição."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR899",
    "display" : "Só é permitido solicitar contexto de atendimento para um dos estabelecimentos autorizados para a credencial {0}.",
    "definition" : "PROSUS pode gerar para qualquer CNES; demais ficam restritos aos estabelecimentos autorizados.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Só é permitido solicitar contexto de atendimento para um dos estabelecimentos autorizados para a credencial {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR900",
    "display" : "Estabelecimento de saúde não encontrado: {0}",
    "definition" : "Não existe o estabelecimento dentro do índice organization do Elastic.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Estabelecimento de saúde não encontrado: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR901",
    "display" : "Profissional não encontrado: {0}",
    "definition" : "Não existe o profissional dentro do índice Practitioner.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Profissional não encontrado: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR902",
    "display" : "O CNES do estabelecimento de saúde é obrigatório ao informar o contexto de atendimento.",
    "definition" : "Necessário verificar o estabelecimento de saúde.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O CNES do estabelecimento de saúde é obrigatório ao informar o contexto de atendimento."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR903",
    "display" : "O CNS do profissional é obrigatório ao informar o contexto de atendimento.",
    "definition" : "Necessário verificar se o profissional de saúde está cadastrado no CNES.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O CNS do profissional é obrigatório ao informar o contexto de atendimento."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR904",
    "display" : "O CNS do paciente é obrigatório ao informar o contexto de atendimento.",
    "definition" : "Verifica se o paciente existe.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O CNS do paciente é obrigatório ao informar o contexto de atendimento."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR905",
    "display" : "Ocorreu um erro não esperado!",
    "definition" : "Erro interno do servidor, erro genérico.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ocorreu um erro não esperado!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR906",
    "display" : "Profissional {0} não autorizado, pois não possui vínculo CBO autorizado em nenhum dos estabelecimentos autorizados para a credencial {1}.",
    "definition" : "Valida credenciais do server na base do SCAB – Portal de Serviços.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Profissional {0} não autorizado, pois não possui vínculo CBO autorizado em nenhum dos estabelecimentos autorizados para a credencial {1}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR907",
    "display" : "Token gov.br expirado! Gere um novo token gov.br e tente novamente.",
    "definition" : "Token de login expirou, necessário gerar um novo.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Token gov.br expirado! Gere um novo token gov.br e tente novamente."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR908",
    "display" : "Token gov.br inválido!",
    "definition" : "Token inválido com base na comunicação com o gov.br",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Token gov.br inválido!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR909",
    "display" : "Token gov.br não autorizado! Sistema solicitante do token não possui autorização: {0}.",
    "definition" : "O token gerado pelo gov.br não está cadastrado dentro do elastic para permitir o login e uso da RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Token gov.br não autorizado! Sistema solicitante do token não possui autorização: {0}."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR910",
    "display" : "Não foi possível validar o token gov.br. URL da chave pública está indisponível!",
    "definition" : "O token gerado pelo gov.br não está cadastrado dentro do elastic para permitir o login e uso da RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível validar o token gov.br. URL da chave pública está indisponível!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR911",
    "display" : "O token usado para identificar o contexto de atendimento está expirado! Gere um novo token de contexto de atendimento para tentar novamente.",
    "definition" : "Período de ativação e validação do token está expirado. Necessário novo acesso e geração de token.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O token usado para identificar o contexto de atendimento está expirado! Gere um novo token de contexto de atendimento para tentar novamente."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR913",
    "display" : "O documento de id {0} não pertence à instância RNDS requisitada. Para acessá-lo use o seguinte endereço: {1}",
    "definition" : "A busca feita pelo documento foi feita em instância incorreta ou com parâmetros incorretos.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O documento de id {0} não pertence à instância RNDS requisitada. Para acessá-lo use o seguinte endereço: {1}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR914",
    "display" : "Problema(s)/Diagnóstico(s) Secundário(s) sem existir um Problema/Diagnóstico Principal.",
    "definition" : "Não é possível o cadastramento de um secundário sem a existência de um principal.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Problema(s)/Diagnóstico(s) Secundário(s) sem existir um Problema/Diagnóstico Principal."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR915",
    "display" : "Não pode existir mais de um Problema/Diagnóstico Principal.",
    "definition" : "Somente é possível a existência de um Problema/Diagnóstico Principal.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não pode existir mais de um Problema/Diagnóstico Principal."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR916",
    "display" : "O identificador do sistema de origem é inválido: {0}",
    "definition" : "Identificador não cadastrado ou usando parâmetros inválidos.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O identificador do sistema de origem é inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR917",
    "display" : "Ao enviar um documento é obrigatório informar o identificador do documento no sistema de origem",
    "definition" : "Falta a informação “identificador do documento” na origem da informação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ao enviar um documento é obrigatório informar o identificador do documento no sistema de origem"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR918",
    "display" : "O Tipo de Resource FHIR utilizado para a referência transitória {0} não é suportado",
    "definition" : "Resource FHIR fora do padrão RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O Tipo de Resource FHIR utilizado para a referência transitória {0} não é suportado"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR919",
    "display" : "Referência transitória não encontrada: {0}",
    "definition" : "A referência transitória não foi cadastrada corretamente ou o campo está “null”.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Referência transitória não encontrada: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR920",
    "display" : "Referência transitória inválida: {0}",
    "definition" : "A referência transitória não foi cadastrada corretamente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Referência transitória inválida: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR921",
    "display" : "Referência transitória não corresponde à ordem estabelecida de resources FHIR: {0}",
    "definition" : "A referência transitória não foi cadastrada corretamente ou o campo está “null”.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Referência transitória não corresponde à ordem estabelecida de resources FHIR: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR922",
    "display" : "Ao enviar um documento é obrigatório utilizar um Composition como primeiro item da lista de resources FHIR",
    "definition" : "No documento enviado, não há o composition ou a ordem de envio não está como composition em primeiro no envio.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ao enviar um documento é obrigatório utilizar um Composition como primeiro item da lista de resources FHIR"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR923",
    "display" : "Ao enviar um documento é obrigatório utilizar o Bundle type: {0}",
    "definition" : "O Bundle type enviado está incorreto. Necessário validar.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ao enviar um documento é obrigatório utilizar o Bundle type: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR924",
    "display" : "Ao enviar um documento é obrigatório utilizar o status: {0}",
    "definition" : "O status utilizado está incorreto.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ao enviar um documento é obrigatório utilizar o status: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR926",
    "display" : "O token usado para identificar o contexto de atendimento é inválido!",
    "definition" : "O token está expirado ou não está autorizado para esta identificação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O token usado para identificar o contexto de atendimento é inválido!"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR927",
    "display" : "Erro ao tentar processar agendamento de mensagem com documento: {0}",
    "definition" : "O documento está inválido ou a RNDS apresenta alguma instabilidade.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao tentar processar agendamento de mensagem com documento: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR928",
    "display" : "Erro ao tentar agendar processamento de mensagem com documento",
    "definition" : "O documento está inválido ou a RNDS apresenta alguma instabilidade.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao tentar agendar processamento de mensagem com documento"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR929",
    "display" : "Erro ao preparar mensagem para processamento agendado",
    "definition" : "O documento está inválido ou a RNDS apresenta alguma instabilidade.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao preparar mensagem para processamento agendado"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR930",
    "display" : "Você não possui autorização para realizar esta operação",
    "definition" : "Validação do índice cnes_acesso_idx",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Você não possui autorização para realizar esta operação"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR931",
    "display" : "Os dados de autenticação informados são inválidos! {0}",
    "definition" : "Validação do índice cnes_acesso_idx",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Os dados de autenticação informados são inválidos! {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR932",
    "display" : "Você precisa estar autenticado para realizar esta operação",
    "definition" : "Validação do índice cnes_acesso_idx",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Você precisa estar autenticado para realizar esta operação"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR933",
    "display" : "Você não possui consentimento para visualizar os dados solicitados",
    "definition" : "Validação do índice cnes_acesso_idx",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Você não possui consentimento para visualizar os dados solicitados"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR934",
    "display" : "Esse paciente está inativo e não pode ser utilizado",
    "definition" : "Validar se o dado está contido no índice Patient.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Esse paciente está inativo e não pode ser utilizado"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "orientacao",
      "valueString" : "A situação do paciente está inativa no sistema. Verifique se os dados estão corretos e refaça o processo."
    }]
  },
  {
    "code" : "ERR935",
    "display" : "Só é permitido pesquisar profissionais usando os identificadores CPF ou CNS.",
    "definition" : "É preciso enviar a informação do CNS ou CPF do profissional de saúde para a consulta ser efetuada.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Só é permitido pesquisar profissionais usando os identificadores CPF ou CNS."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR936",
    "display" : "Só é permitido pesquisar organizações usando o identificador CNES para Estabelecimentos ou CNPJ/CPF para Pessoas Jurídicas ou Profissionais Liberais",
    "definition" : "Validação do Practitioner e sua relação de CNES cadastrado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Só é permitido pesquisar organizações usando o identificador CNES para Estabelecimentos ou CNPJ/CPF para Pessoas Jurídicas ou Profissionais Liberais"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR937",
    "display" : "Só é permitido pesquisar pacientes usando os identificadores CPF ou CNS",
    "definition" : "Validação da regra de negócio RNDS e CADSUS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Só é permitido pesquisar pacientes usando os identificadores CPF ou CNS"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR938",
    "display" : "O identificador do consentimento informado é inválido",
    "definition" : "Validar dentro da base de consentimento se o CNS está cadastrado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O identificador do consentimento informado é inválido"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR939",
    "display" : "Campo code da estrutura FHIR role inválido: {0}",
    "definition" : "FHIR fora do padrão RNDS",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo code da estrutura FHIR role inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR940",
    "display" : "Campo system da estrutura FHIR role inválido: {0}",
    "definition" : "FHIR fora do padrão RNDS",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo system da estrutura FHIR role inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR941",
    "display" : "É obrigatório preencher o campo system ao informar o papel usando a estrutura FHIR role",
    "definition" : "O campo está vindo vazio, é necessário informar o papel do autor, conforme a estrutura FHIR role",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo system ao informar o papel usando a estrutura FHIR role"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR942",
    "display" : "É obrigatório preencher o campo code ao informar o papel usando a estrutura FHIR role.",
    "definition" : "O campo está vindo vazio, é necessário informar o código, conforme a estrutura FHIR role.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo code ao informar o papel usando a estrutura FHIR role."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR943",
    "display" : "É obrigatório informar o papel do ator usando a estrutura de FHIR role",
    "definition" : "É obrigatório o preenchimento do campo, mas ele não está sendo enviado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar o papel do ator usando a estrutura de FHIR role"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR944",
    "display" : "Tipo de referência inválida para atores: {0}",
    "definition" : "Foi informado uma referência de ator que não consta na lista da CNS, por favor verifique e envie corretamente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tipo de referência inválida para atores: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR945",
    "display" : "É obrigatório informar pelo menos um ator para o qual se deseja conceder/retirar consentimento",
    "definition" : "É obrigatório enviar as informações de pelo menos um ator ao consultar, conceder ou retirar o consentimento do paciente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar pelo menos um ator para o qual se deseja conceder/retirar consentimento"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR946",
    "display" : "Ator não encontrado: {0}",
    "definition" : "É necessário enviar as informações do ator.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ator não encontrado: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR947",
    "display" : "Uso de consentimento por período ainda não suportado.",
    "definition" : "O período informado está fora do suportado.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Uso de consentimento por período ainda não suportado."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR948",
    "display" : "A política de consentimento implícita não pode ser aplicada a esse paciente pois ele se enquadra como VIP e seus dados devem obrigatoriamente passar por consent",
    "definition" : "Esta regra negocial não se aplica a paciente inseridos na lista VIP.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A política de consentimento implícita não pode ser aplicada a esse paciente pois ele se enquadra como VIP e seus dados devem obrigatoriamente passar por consentimento explícito"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR949",
    "display" : "Campo code da estrutura FHIR policyRule inválido: {0}",
    "definition" : "É necessário enviar as informações de consentimento implícitas e explícitas",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo code da estrutura FHIR policyRule inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR950",
    "display" : "Campo system da estrutura FHIR policyRule inválido: {0}",
    "definition" : "A informação de consentimento do sistema precisa ser enviada",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo system da estrutura FHIR policyRule inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR951",
    "display" : "É obrigatório preencher o campo System ao informar a política de consentimento usando a estrutura FHIR policyRule.",
    "definition" : "A informação da política de consentimento está vindo nula ou vazia, por favor informá-la.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo System ao informar a política de consentimento usando a estrutura FHIR policyRule."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR952",
    "display" : "É obrigatório preencher o campo code ao informar a política de consentimento usando a estrutura FHIR policyRule",
    "definition" : "A código da política de consentimento está vindo vazio, por favor informá-lo!",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo code ao informar a política de consentimento usando a estrutura FHIR policyRule"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR953",
    "display" : "Campo code da estrutura FHIR category inválido: {0}",
    "definition" : "No código categoria informada não se encontra dentro do rol de códigos de consentimento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo code da estrutura FHIR category inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR954",
    "display" : "Campo system da estrutura FHIR category inválido: {0}",
    "definition" : "A informação do sistema não se encontra dentro do rol de consentimentos.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo system da estrutura FHIR category inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR955",
    "display" : "É obrigatório preencher o campo system ao informar a categoria usando a estrutura FHIR category",
    "definition" : "O campo system é obrigatório, sendo que o mesmo se encontra vazio.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo system ao informar a categoria usando a estrutura FHIR category"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR956",
    "display" : "É obrigatório preencher o campo code ao informar a categoria usando a estrutura FHIR category",
    "definition" : "O campo do código do sistema é obrigatório, sendo que o mesmo se encontra vazio.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo code ao informar a categoria usando a estrutura FHIR category"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR957",
    "display" : "É obrigatório informar a categoria usando a estrutura de FHIR category",
    "definition" : "O campo categoria é obrigatório e se encontra vazio.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar a categoria usando a estrutura de FHIR category"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR958",
    "display" : "Campo code da estrutura FHIR scope inválido: {0}",
    "definition" : "O código do escopo do consentimento está vazio, e é obrigatório o preenchimento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo code da estrutura FHIR scope inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR959",
    "display" : "Campo system da estrutura FHIR scope inválido: {0}",
    "definition" : "O código do escopo do consentimento do sistema está fora do rol de consentimentos de sistema.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo system da estrutura FHIR scope inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR960",
    "display" : "É obrigatório preencher o campo system ao informar o escopo usando a estrutura FHIR scope",
    "definition" : "O código do escopo do consentimento do sistema está vazio, e é obrigatório o preenchimento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo system ao informar o escopo usando a estrutura FHIR scope"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR961",
    "display" : "É obrigatório preencher o campo code ao informar o escopo usando a estrutura FHIR scope",
    "definition" : "O código do escopo do consentimento está vazio, e é obrigatório o preenchimento",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo code ao informar o escopo usando a estrutura FHIR scope"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR962",
    "display" : "É obrigatório informar o escopo usando a estrutura de FHIR scope",
    "definition" : "O escopo do consentimento é obrigatório e está vazio",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar o escopo usando a estrutura de FHIR scope"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR963",
    "display" : "Status inválido: {0}",
    "definition" : "Status inexistente na RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Status inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR964",
    "display" : "É obrigatório informar o status do documento",
    "definition" : "Necessário efetuar o cadastramento do status.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar o status do documento"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR965",
    "display" : "Tipo do documento informado em sua estrutura interna deve condizer com o tipo informado na estrutura FHIR type: {0}",
    "definition" : "O tipo do documento não está seguindo o padrão FHIR.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tipo do documento informado em sua estrutura interna deve condizer com o tipo informado na estrutura FHIR type: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR966",
    "display" : "Campo system da estrutura FHIR type inválido: {0}",
    "definition" : "O tipo de código do sistema não foi enviado corretamente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Campo system da estrutura FHIR type inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR967",
    "display" : "É obrigatório preencher o campo system ao informar um tipo do documento usando a estrutura FHIR type",
    "definition" : "não está em uso. Sem implementação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo system ao informar um tipo do documento usando a estrutura FHIR type"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR968",
    "display" : "É obrigatório preencher o campo code ao informar um tipo do documento usando a estrutura FHIR type",
    "definition" : "*obs.: não está em uso. Sem implementação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório preencher o campo code ao informar um tipo do documento usando a estrutura FHIR type"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR969",
    "display" : "É obrigatório informar o tipo do documento usando a estrutura de FHIR type",
    "definition" : "*obs.: não está em uso. Sem implementação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar o tipo do documento usando a estrutura de FHIR type"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR970",
    "display" : "O conteúdo do documento é inválido ou não condiz com o contentType indicado",
    "definition" : "*obs.: não está em uso. Sem implementação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O conteúdo do documento é inválido ou não condiz com o contentType indicado"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR971",
    "display" : "É obrigatório informar o conteúdo do documento usando o campo FHIR attachment.data",
    "definition" : "*obs.: não está em uso. Sem implementação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar o conteúdo do documento usando o campo FHIR attachment.data"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR972",
    "display" : "ContentType inválido: {0}",
    "definition" : "*obs.: não está em uso. Sem implementação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "ContentType inválido: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR973",
    "display" : "É obrigatório informar o contentType do documento",
    "definition" : "*obs.: não está em uso. Sem implementação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar o contentType do documento"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR974",
    "display" : "A data deve ser igual ou menor que a data atual",
    "definition" : "A data informada é superior a data atual. É necessário enviar a data no período correto, isto é, menor ou igual a data atual.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data deve ser igual ou menor que a data atual"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR975",
    "display" : "É obrigatório informar a data do documento",
    "definition" : "É obrigatório informar a data do documento, mas a mesma se encontra vazia.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar a data do documento"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "para todos os documentos RNDS (RIA, REL, RAC, RA, RPM, RDM,ATM, CMD, SA, SAO)."
    }]
  },
  {
    "code" : "ERR976",
    "display" : "Tipo de referência inválida para autores: {0}",
    "definition" : "O tipo de referência não está de acordo com o autor {0}.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tipo de referência inválida para autores: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR977",
    "display" : "É obrigatório informar pelo menos um autor do documento",
    "definition" : "A quantidade de autores informado foi 0, é necessário informar pelo menos um autor.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "É obrigatório informar pelo menos um autor do documento"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR978",
    "display" : "Autor não encontrado: {0}",
    "definition" : "É necessário informar o autor, nenhum autor foi informado. A informação veio nula ou vazia.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Autor não encontrado: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "orientacao",
      "valueString" : "A informação referente ao autor está vazia ou em branco. Verifique, os dados e enviei novamente."
    }]
  },
  {
    "code" : "ERR979",
    "display" : "Não foi possível buscar o documento solicitado",
    "definition" : "O documento solicitado não foi encontrado, favor verificar a informação do documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível buscar o documento solicitado"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR980",
    "display" : "O identificador do documento informado é inválido",
    "definition" : "O identificador do documento foi enviado como nulo ou vazio.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O identificador do documento informado é inválido"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR981",
    "display" : "Tipo de referência inválida: {0}",
    "definition" : "A informação do tipo de profile informado não tem consta no rol de referência de profiles usando na RNDS.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tipo de referência inválida: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR982",
    "display" : "Não foi possível processar o documento de id {0} pois a referência para o documento original está inválida ou não existe",
    "definition" : "O documento de id não foi processado por não estar em conformidade com o FHIR.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível processar o documento de id {0} pois a referência para o documento original está inválida ou não existe"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR983",
    "display" : "Paciente não encontrado: {0}",
    "definition" : "O CPF ou CNS informado não foi encontrado na base.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Paciente não encontrado: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "orientacao",
      "valueString" : "O sistema não está encontrado os dados paciente na base de dados. Verifique se os dados do CPF ou CNS estão corretos. Refaça o processo novamente."
    }]
  },
  {
    "code" : "ERR984",
    "display" : "Não foram informados parâmetros válidos",
    "definition" : "O campo informado pode estar nulo ou vazio. Exemplo: paciente vazio ou nulo.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foram informados parâmetros válidos"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR985",
    "display" : "O registro de {0} referenciado possui um estado inválido: identificador não é único",
    "definition" : "Foi retornado mais de um registro para esse CNS ou CPF.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O registro de {0} referenciado possui um estado inválido: identificador não é único"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR986",
    "display" : "Não foi possível buscar os documentos do paciente",
    "definition" : "Ao buscar os documentos do paciente o sistema apresentou erro interno.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível buscar os documentos do paciente"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR987",
    "display" : "O registro do paciente referenciado possui um estado inválido: não há CNS definitivo",
    "definition" : "A informação do CNS enviada foi nula ou vazia.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O registro do paciente referenciado possui um estado inválido: não há CNS definitivo"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR988",
    "display" : "A referência ao profissional informada não é válida",
    "definition" : "*obs.: não está em uso. Sem implementação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A referência ao profissional informada não é válida"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "situacaoDocumentada",
      "valueCode" : "nao-implementado-ou-inativo"
    }]
  },
  {
    "code" : "ERR989",
    "display" : "Acesso ao EHR Data Services não autorizado",
    "definition" : "Sem permissão de acesso ao EHR data services. Http error 401.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Acesso ao EHR Data Services não autorizado"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR990",
    "display" : "Resposta do EHR Data Services não condiz com contrato de serviço",
    "definition" : "Erro não esperado de retorno pelo EHR Data Services.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Resposta do EHR Data Services não condiz com contrato de serviço"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR991",
    "display" : "Erro ao processar resposta do EHR Data Services",
    "definition" : "Mensagem com conteúdo incorreto enviado pelo EHR Data Services. O parse não foi possível.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao processar resposta do EHR Data Services"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR992",
    "display" : "Tempo máximo de comunicação atingido ao tentar comunicar com EHR Data Services",
    "definition" : "Timeout de comunicação do socket entre os sistemas.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tempo máximo de comunicação atingido ao tentar comunicar com EHR Data Services"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR993",
    "display" : "EHR Data Services não está disponível",
    "definition" : "EHR Data services indisponível. Problema técnico RNDS ou instabilidade de rede.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "EHR Data Services não está disponível"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR994",
    "display" : "Erro ao tentar estabelecer comunicação com o EHR Data Services",
    "definition" : "EHR Data services indisponível. Problema técnico RNDS ou instabilidade de rede.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro ao tentar estabelecer comunicação com o EHR Data Services"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR995",
    "display" : "Ordenação requisitada não é suportada",
    "definition" : "A ordenação da consulta solicitada não é suportada. Verifique a ordem das datas enviadas para a ordenação dos dados.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Ordenação requisitada não é suportada"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR996",
    "display" : "Documento enviado é inválido",
    "definition" : "O documento foi enviado vazio ou nulo.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Documento enviado é inválido"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR997",
    "display" : "A referência ao paciente informada não é válida: {0}",
    "definition" : "As informações do paciente foram enviadas incorretamente.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A referência ao paciente informada não é válida: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR998",
    "display" : "Não foi possível persistir o documento",
    "definition" : "Ações de continuidade como deletar, salvar ou criar consentimento não foi possível. Necessário efetuar novamente a ação feita no momento do erro ou fazer novo envio do documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não foi possível persistir o documento"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR999",
    "display" : "Não há conectividade com o banco de dados de cache",
    "definition" : "O Banco de dados de cache está inacessível. Este tipo de problema é temporário e é tratado em prioridade para a resolução técnica.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Não há conectividade com o banco de dados de cache"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "ERR1005",
    "display" : "Procedimentos do grupo 030101, é necessário o código CBO",
    "definition" : "Necessário informar o CBO para prosseguir com o envio.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Procedimentos do grupo 030101, é necessário o código CBO"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RA – Regulação Assistencial."
    }]
  },
  {
    "code" : "ERR1006",
    "display" : "A Data da Solicitação (ServiceRequest.AuthoredOn) deve ser menor ou igual a data do recebimento do documento.",
    "definition" : "Referente ao envio do doc RA, é necessário validar a data de atendimento e a data de recebimento do documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A Data da Solicitação (ServiceRequest.AuthoredOn) deve ser menor ou igual a data do recebimento do documento."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RA – Regulação Assistencial."
    }]
  },
  {
    "code" : "ERR1007",
    "display" : "A Data de Autorização (Appointment.created) deve ser maior ou igual a Data se Solicitação (ServiceRequest.AuthoredOn).",
    "definition" : "Referente ao envio do doc RA, é necessário validar a data de autorização do atendimento e a data de solicitação.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A Data de Autorização (Appointment.created) deve ser maior ou igual a Data se Solicitação (ServiceRequest.AuthoredOn)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RA – Regulação Assistencial."
    }]
  },
  {
    "code" : "ERR1008",
    "display" : "A Data de Agendamento (Appointment.start) deve ser maior ou igual a Data de Autorização (Appointment.created).",
    "definition" : "Referente ao envio do doc RA, é necessário validar a data de agendamento do atendimento e a data de autorização.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A Data de Agendamento (Appointment.start) deve ser maior ou igual a Data de Autorização (Appointment.created)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RA – Regulação Assistencial."
    }]
  },
  {
    "code" : "ERR1009",
    "display" : "A Data de Execução (ServiceRequest.occurrenceDateTime) deve ser maior ou igual a Data de Agendamento (Appointment.start).",
    "definition" : "Referente ao envio do doc RA, é necessário validar a data de execução do atendimento e a data de agendamento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A Data de Execução (ServiceRequest.occurrenceDateTime) deve ser maior ou igual a Data de Agendamento (Appointment.start)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RA – Regulação Assistencial."
    }]
  },
  {
    "code" : "ERR1010",
    "display" : "A data de Administração do Imunobiológico (Immunization.occurrenceDateTime) não possa ser maior que o dia vigente.",
    "definition" : "Necessário verificar a data de administração do Imunobiológico. A data está como data futura.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "A data de Administração do Imunobiológico (Immunization.occurrenceDateTime) não possa ser maior que o dia vigente."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RIA – Registro Imunobiológico Administrado."
    }]
  },
  {
    "code" : "ERR1011",
    "display" : "O campo de Contato Hanseníase (Immunization.extension:contatoHanseniase) deverá ser obrigatório quando o Imunobiológico Administrado (Immunization.vaccineCode.c",
    "definition" : "Trata-se de RIA utilizando o code 15, por isso, é necessár preencher o campo Contato Hanseníase.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo de Contato Hanseníase (Immunization.extension:contatoHanseniase) deverá ser obrigatório quando o Imunobiológico Administrado (Immunization.vaccineCode.coding.code) for code 15."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RIA – Registro Imunobiológico Administrado – Imuno code 15."
    }]
  },
  {
    "code" : "ERR1012",
    "display" : "O Campo Fabricante (Immunization.manufactor) deve ser obrigatório em todos os casos, exceto quando o Registro de Origem (Immunization.reportOrigin.coding.code)",
    "definition" : "Necessário validar o campo fabricante. O campo é obrigatório no envio do documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O Campo Fabricante (Immunization.manufactor) deve ser obrigatório em todos os casos, exceto quando o Registro de Origem (Immunization.reportOrigin.coding.code) for code 01."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RIA – Registro Imunobiológico Administrado – Imuno exceto code 1."
    }]
  },
  {
    "code" : "ERR1013",
    "display" : "O Campo Lote (Immunization.lotNumber) deve ser obrigatório em todos os casos, exceto quando o Registro de Origem (Immunization.reportOrigin.coding.code) for cod",
    "definition" : "Necessário validar o campo Lote. O campo é obrigatório no envio do documento.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O Campo Lote (Immunization.lotNumber) deve ser obrigatório em todos os casos, exceto quando o Registro de Origem (Immunization.reportOrigin.coding.code) for code 01."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RIA – Registro Imunobiológico Administrado – Imuno exceto code 1."
    }]
  },
  {
    "code" : "ERR1014",
    "display" : "O Campo Motivo de Indicação (Immunization.reasonReference) deve ser opcional, exceto quando a Estratégia de Vacinação (Immunization.protocolApplied.extension:st",
    "definition" : "Se o envio refere-se ao Imuno Code 2, é necessário informar o campo Motivo de Indicação. Para todos os demais códigos, o envio é opcional.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O Campo Motivo de Indicação (Immunization.reasonReference) deve ser opcional, exceto quando a Estratégia de Vacinação (Immunization.protocolApplied.extension:strategy) for Especial (code 2)."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    },
    {
      "code" : "tipoDocumento",
      "valueString" : "RIA – Registro Imunobiológico Administrado – Imuno exceto code 2."
    }]
  },
  {
    "code" : "ERROR_CONSUME_MESSAGE",
    "display" : "Falha ao tentar processar a mensagem: {0}",
    "definition" : "Falha ao tentar processar a mensagem: {0}",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Falha ao tentar processar a mensagem: {0}"
    },
    {
      "code" : "grupo",
      "valueString" : "Erro RNDS"
    }]
  },
  {
    "code" : "VIOLATION_CONSTRAINT",
    "display" : "Erro fatal de violação de restrição (constraints) de banco de dados.",
    "definition" : "Erro fatal de violação de restrição (constraints) de banco de dados.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Erro fatal de violação de restrição (constraints) de banco de dados."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro genérico do sistema"
    }]
  },
  {
    "code" : "VIOLATION_FK_CONSTRAINT",
    "display" : "O registro não pode ser excluído pois possui dependências na base de dados.",
    "definition" : "O registro não pode ser excluído pois possui dependências na base de dados.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O registro não pode ser excluído pois possui dependências na base de dados."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro genérico do sistema"
    }]
  },
  {
    "code" : "VIOLATION_UK_CONSTRAINT",
    "display" : "O registro já existe na base de dados.",
    "definition" : "O registro já existe na base de dados.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O registro já existe na base de dados."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro genérico do sistema"
    }]
  },
  {
    "code" : "VALIDATION_DOMINIO",
    "display" : "O valor informado para o campo é inválido.",
    "definition" : "O valor informado para o campo é inválido.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O valor informado para o campo é inválido."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro genérico do sistema"
    }]
  },
  {
    "code" : "REGISTRO_DELETADO",
    "display" : "O registro foi deletado com sucesso.",
    "definition" : "O registro foi deletado com sucesso.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O registro foi deletado com sucesso."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro genérico do sistema"
    }]
  },
  {
    "code" : "validation.required",
    "display" : "O campo {0} é de preenchimento obrigatório.",
    "definition" : "O campo {0} é de preenchimento obrigatório.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "O campo {0} é de preenchimento obrigatório."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro genérico do sistema"
    }]
  },
  {
    "code" : "validation.type.param",
    "display" : "Tipo de parâmetro incorreto para a requisição.",
    "definition" : "Tipo de parâmetro incorreto para a requisição.",
    "property" : [{
      "code" : "mensagem",
      "valueString" : "Tipo de parâmetro incorreto para a requisição."
    },
    {
      "code" : "grupo",
      "valueString" : "Erro genérico do sistema"
    }]
  }]
}

```
