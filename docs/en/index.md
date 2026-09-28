# Principal - Guia de Implementação da Rede Nacional de Dados em Saúde (RNDS) v1.0.0-release

## Principal

### Introdução

 Este Guia de Implementação (IG) reúne as orientações gerais para a integração de sistemas de informação com a [Rede Nacional de Dados em Saúde (RNDS)](https://www.gov.br/saude/pt-br/composicao/seidigi/rnds) e apresenta os guias específicos dos modelos disponíveis. Destina-se a Estados, Municípios, Distrito Federal, estabelecimentos de saúde e empresas que desenvolvem soluções de tecnologia da informação em saúde. 

 Neste guia, os integradores encontram orientações sobre credenciamento e utilização dos serviços (*web services*) da RNDS. Nos guias de cada modelo, encontram as especificações para a estruturação das informações conforme o padrão [HL7 FHIR versão R4](https://hl7.org/fhir/R4/). As orientações gerais de integração e as especificações do modelo escolhido devem ser consultadas em conjunto. 

 `[Consultar os modelos e seus guias de implementação](#modelos)` | `[Conhecer o fluxo de integração](#flow)` | `[Acessar as orientações gerais](#walkthrough)` 

### Contextualização

 A RNDS é uma plataforma nacional de integração de dados em saúde que faz parte do [Meu SUS Digital](https://www.gov.br/saude/pt-br/composicao/seidigi/meu-sus-digital), um programa do Governo Federal que tem como principal missão materializar a [Estratégia de Saúde Digital do Brasil](https://bvsms.saude.gov.br/bvs/publicacoes/estrategia_saude_digital_Brasil.pdf). 

 A RNDS utiliza computação em nuvem e tecnologias emergentes para criar um repositório de documentos responsável por armazenar informações de saúde dos cidadãos, mantendo a privacidade, integridade e auditabilidade dos dados de maneira acessível e interoperável. Com isso, fornece aos profissionais de saúde acesso à história clínica do paciente, permitindo a transição e a continuidade do cuidado, além de possibilitar aos indivíduos acesso aos seus dados de saúde. 

 Dessa forma, os serviços (*web services*) permitirão que as entidades da área da saúde compartilhem as informações dos modelos computacionais com a RNDS de forma oportuna e confiável a quem precisa desta informação. 

### Interoperabilidade

 Para garantir a interoperabilidade entre as aplicações de Saúde Digital, em especial Prontuário(s) Eletrônico(s) do Paciente, portais e aplicações (*web e mobile*), a troca de informações ocorre por meio de serviços (*web services*) [RESTful](https://pt.wikipedia.org/wiki/REST), desenvolvidos de acordo com o padrão [FHIR R4](https://hl7.org/fhir/R4/). 

### Modelos disponíveis e Guias de Implementação

 Selecione o modelo correspondente às informações que deseja compartilhar com a RNDS. Cada link direciona para o respectivo Guia de Implementação, que deve ser consultado para conhecer os perfis FHIR, as terminologias, as regras e os exemplos aplicáveis ao modelo. 

| | | |
| :--- | :--- | :--- |
| **RIRA**Registro de Regulação Assistencial | Informações relativas à regulação do acesso à atenção em saúde. | `[Acessar o IG do RIRA](https://fhir.saude.gov.br/rira/)` |
| **RIA**Registro de Imunobiológico Administrado | Informações sobre a administração de imunobiológicos. | `[Acessar o IG do RIA](https://fhir.saude.gov.br/ria/)` |
| **RAC**Registro de Atendimento Clínico | Informações clínicas registradas durante o atendimento em saúde. | `[Acessar o IG do RAC](https://fhir.saude.gov.br/rac/)` |
| **SA**Sumário de Alta | Informações da alta hospitalar para apoiar a continuidade do cuidado. | `[Acessar o IG do SA](https://fhir.saude.gov.br/sa/)` |
| **REDFM**Registro Eletrônico de Dispensação ou Fornecimento de Medicamentos | Informações sobre a dispensação ou o fornecimento de medicamentos. | `[Acessar o IG do REDFM](https://fhir.saude.gov.br/redfm/)` |

### Fluxo para Integração com a RNDS

Abaixo você encontra um material com o fluxo oficial para integração com a RNDS.

<iframe src="https://mobileapps-prd.saude.gov.br/portal-servicos/files/f3bd659c8c8ae3ee966e575fde27eb58/0e3affbe4f1b86b50ae78ab652b2ebaa_pgst0fpqe.pdf" width="100%" title="Fluxo para integração com a RNDS" height="600px"> Seu navegador não suporta visualização de PDF.
    <a href="https://mobileapps-prd.saude.gov.br/portal-servicos/files/f3bd659c8c8ae3ee966e575fde27eb58/0e3affbe4f1b86b50ae78ab652b2ebaa_pgst0fpqe.pdf">Clique
      aqui para abrir</a>. </iframe>
 
### Roteiro para o integrador

Consulte as orientações gerais e, em seguida, as especificações do modelo que será integrado.

*  [Credenciamento](credenciamento.md): Saiba qual é o processo e requisitos a serem seguidos por um estabelecimento de saúde para a integração com a RNDS. 
*  [Integração](integracao.md): Define as operações a serem atendidas para integração com a RNDS. 
*  [Modelos e Guias de Implementação](#modelos): Acesse as especificações dos modelos da RNDS. 
*  [Downloads](downloads.md): Artefatos empregados pelos integradores. 
*  [Feedback](forms.md): Espaço para feedbacks, sugestões e melhorias. 
*  [Suporte da RNDS](suporte.md): Canal de suporte relacionado à RNDS. 

