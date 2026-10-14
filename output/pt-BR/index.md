# Principal - Guia de Implementação da Rede Nacional de Dados em Saúde (RNDS) v1.0.0-release

## Principal

### Introdução

 Este Guia de Implementação (IG) reúne as orientações gerais para a integração de sistemas de informação com a [Rede Nacional de Dados em Saúde (RNDS)](https://www.gov.br/saude/pt-br/composicao/seidigi/rnds) e apresenta os guias específicos dos modelos disponíveis. Destina-se a Estados, Municípios, Distrito Federal, estabelecimentos de saúde e empresas que desenvolvem soluções de tecnologia da informação em saúde. 

 Neste guia, os integradores encontram orientações sobre credenciamento e utilização dos serviços (*web services*) da RNDS. Nos guias de cada modelo, encontram-se as especificações para a estruturação das informações conforme o padrão [HL7 FHIR versão R4](https://hl7.org/fhir/R4/). As orientações gerais de integração e as especificações do modelo escolhido devem ser consultadas em conjunto. 

 ` [Consultar os modelos e seus guias](#modelos) ` | ` [Conhecer o fluxo de integração](#flow) ` | ` [Acessar as orientações gerais](#walkthrough) ` 

### Contextualização

A Rede Nacional de Dados em Saúde (RNDS), instituída pela [Portaria GM/MS nº 1.434](https://www.in.gov.br/en/web/dou/-/portaria-n-1.434-de-28-de-maio-de-2020-259143327), de 28 de maio de 2020, e posteriormente disciplinada pelo [Decreto nº 12.560, de 23 de julho de 2025](https://www.in.gov.br/en/web/dou/-/decreto-n-12.560-de-23-de-julho-de-2025-643871577), é a plataforma nacional de interoperabilidade do ecossistema de dados do Sistema Único de Saúde (SUS), alinhada à [Estratégia de Saúde Digital para o Brasil](https://bvsms.saude.gov.br/bvs/publicacoes/estrategia_saude_digital_Brasil.pdf), destinada à integração e ao compartilhamento seguro e padronizado de informações em saúde.

A RNDS contribui para a continuidade do cuidado, a vigilância e a gestão em saúde, observando os requisitos de segurança, privacidade e integridade dos dados. As informações compartilhadas podem ser disponibilizadas por meio das Plataformas SUS Digital, incluindo o [Meu SUS Digital](https://www.gov.br/saude/pt-br/composicao/seidigi/meu-sus-digital), observadas as regras de acesso e de proteção de dados pessoais.

Nesse contexto, os serviços de integração (*web services*) permitem o envio dos registros à RNDS, conforme os modelos informacionais e computacionais e as especificações técnicas estabelecidas nos Guias de Implementação.

### Interoperabilidade

 Para garantir a interoperabilidade entre as aplicações de Saúde Digital, em especial Prontuário(s) Eletrônico(s) do Paciente, portais e aplicações (*web e mobile*), a troca de informações ocorre por meio de serviços (*web services*) [RESTful](https://pt.wikipedia.org/wiki/REST), desenvolvidos de acordo com o padrão [FHIR R4](https://hl7.org/fhir/R4/). 

### Modelos disponíveis e Guias de Implementação

 Selecione o modelo correspondente às informações que deseja compartilhar com a RNDS. Cada link direciona para o respectivo Guia de Implementação, que deve ser consultado para conhecer os perfis FHIR, as terminologias, as regras e os exemplos aplicáveis ao modelo. 

| | | |
| :--- | :--- | :--- |
| ` **RIRA** `Registro de Regulação Assistencial | [Portaria Conjunta SAES/SEIDIGI nº 3, de 18 de abril de 2023](https://www.in.gov.br/en/web/dou/-/portaria-conjunta-saes/seidigi-n-3-de-18-de-abril-de-2023-478301026) | ` [https://fhir.saude.gov.br/rira/](https://fhir.saude.gov.br/rira/) ` |
| ` **RIA** `Registro de Imunobiológico Administrado | [Portaria SAES/SVSA/SEIDIGI nº 25, de 27 de novembro de 2023](https://bvsms.saude.gov.br/bvs/saudelegis/Saes/2023/poc0025_30_11_2023.html) | ` [https://fhir.saude.gov.br/ria/](https://fhir.saude.gov.br/ria/) ` |
| ` **RAC** `Registro de Atendimento Clínico | [Portaria GM/MS nº 8.347, de 8 de outubro de 2025](https://www.in.gov.br/web/dou/-/portaria-gm/ms-n-8.347-de-8-de-outubro-de-2025-661591512) | ` [https://fhir.saude.gov.br/rac/](https://fhir.saude.gov.br/rac/) ` |
| ` **REL** `Resultado de Exame Laboratorial | [Portaria GM/MS nº 8.276, de 29 de setembro de 2025](https://www.in.gov.br/en/web/dou/-/portaria-gm/ms-n-8.276-de-29-de-setembro-de-2025-659605663) | ` [https://fhir.saude.gov.br/rel/](https://fhir.saude.gov.br/rel/) ` |
| ` **SA** `Sumário de Alta | [Portaria GM/MS nº 8.026, de 27 de agosto de 2025](https://www.in.gov.br/en/web/dou/-/portaria-gm/ms-n-8.026-de-27-de-agosto-de-2025-651423099) | ` [https://fhir.saude.gov.br/sa/](https://fhir.saude.gov.br/sa/) ` |
| ` **REDFM** `Registro Eletrônico de Dispensação ou Fornecimento de Medicamentos | [Portaria GM/MS nº 6100, de 17 de Dezembro de 2024](https://bvsms.saude.gov.br/bvs/saudelegis/gm/2024/prt6100_18_12_2024.html) | ` [https://fhir.saude.gov.br/redfm/](https://fhir.saude.gov.br/redfm/) ` |

| | | |
| :--- | :--- | :--- |
| ` **OBM** ` | Ontologia Brasileira de Medicamentos (OBM) | ` [https://portal-obm.saude.gov.br/](https://portal-obm.saude.gov.br/) ` |
| ` **OCL** ` | Open Concept Lab (OCL) das terminologias da RNDS | ` [https://terminologia.saude.gov.br/](https://terminologia.saude.gov.br/) ` |
| ` **BRTerminologia** ` | IG das Terminologias utilizadas pela RNDS | ` [ https://terminologia.saude.gov.br/fhir/](https://terminologia.saude.gov.br/fhir/) ` |
| ` **IPS Brasil** ` | IG do Sumário Internacional do Paciente do Brasil (International Patient Summary - IPS) | ` [https://hl7.org.br/fhir/ips/](https://hl7.org.br/fhir/ips/) ` |
| ` **BRCore** ` | IG do núcleo de implementação do padrão HL7 FHIR adaptado ao contexto brasileiro | ` [https://hl7.org.br/fhir/core/](https://hl7.org.br/fhir/core/) ` |

### Fluxo para Integração com a RNDS

Abaixo você encontra um material com o fluxo oficial para integração com a RNDS.

<iframe src="https://mobileapps-prd.saude.gov.br/portal-servicos/files/f3bd659c8c8ae3ee966e575fde27eb58/0e3affbe4f1b86b50ae78ab652b2ebaa_pgst0fpqe.pdf" width="100%" title="Fluxo para integração com a RNDS" height="600px"> Seu navegador não suporta
    visualização de PDF. <a href="https://mobileapps-prd.saude.gov.br/portal-servicos/files/f3bd659c8c8ae3ee966e575fde27eb58/0e3affbe4f1b86b50ae78ab652b2ebaa_pgst0fpqe.pdf">Clique
      aqui para abrir</a>. </iframe>
 
### Roteiro para o integrador

Consulte as orientações gerais e, em seguida, as especificações do modelo que será integrado.

*  [Credenciamento](credenciamento.md): Saiba qual é o processo e requisitos a serem seguidos por um estabelecimento de saúde para a integração com a RNDS. 
*  [Integração](integracao.md): Define as operações a serem atendidas para integração com a RNDS. 
*  [ *CapabilityStatement* ](CapabilityStatement-CapabilityStatement-EHRServices.md): Capacidades/catálogo da API da RNDS 
*  [Erros](CodeSystem-RNDSErros.md): Códigos de mensagens e erros documentados pela RNDS. 
*  [Modelos e Guias de Implementação](#modelos): Acesse as especificações dos modelos da RNDS. 
*  [Downloads](downloads.md): Artefatos empregados pelos integradores. 
*  [Feedback](forms.md): Espaço para feedbacks, sugestões e melhorias. 
*  [Suporte da RNDS](suporte.md): Canal de suporte relacionado à RNDS. 

