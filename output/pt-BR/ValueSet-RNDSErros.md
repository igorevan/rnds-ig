# Mensagens e Erros da RNDS - Guia de Implementação da Rede Nacional de Dados em Saúde (RNDS) v1.0.0

## ValueSet: Mensagens e Erros da RNDS 

 **References** 

Este conjunto de valores não é utilizado aqui; pode ser utilizado noutro local (por exemplo, especificações e/ou implementações que utilizem este conteúdo)

### Definição lógica (CLD)

 

### Expansão

-------

 [Descrição do(s) quadro(s) acima](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "ValueSet",
  "id" : "RNDSErros",
  "language" : "pt-BR",
  "url" : "http://www.saude.gov.br/fhir/r4/ValueSet/RNDSErros",
  "version" : "1.0.0",
  "name" : "RNDSErrosVS",
  "title" : "Mensagens e Erros da RNDS",
  "status" : "active",
  "experimental" : false,
  "date" : "2026-11-25T15:07:17-03:00",
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
  "description" : "Conjunto de códigos de mensagens e erros apresentados pela RNDS.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "compose" : {
    "include" : [{
      "system" : "http://www.saude.gov.br/fhir/r4/CodeSystem/RNDSErros"
    }]
  }
}

```
