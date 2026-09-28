# Integração - Guia de Implementação da Rede Nacional de Dados em Saúde (RNDS) v1.0.0-release

## Integração

### Integração com a RNDS

 Para garantir a interoperabilidade entre as aplicações de Saúde Digital, em especial Prontuário(s) Eletrônico(s) do Paciente (PEP), portais e aplicações (*web e mobile*), a troca de informações ocorre por meio de serviços (*web services*) RESTful, desenvolvidos de acordo com o padrão [FHIR R4](https://hl7.org/FHIR/). 

### Identificadores do Registro Enviado a RNDS

 Vale ressaltar que os registros são documentos computacionais, em formato JSON, compostos por perfis (*profiles*) do padrão FHIR R4. Cada registro enviado à RNDS possui dois identificadores: 

* **Identificador atribuído pelo sistema de origem**: também chamado de identificador local, é o ID criado pelo sistema de origem para identificar univocamente o registro em sua base.


   No arquivo JSON, o identificador local deve ser informado no profile *Bundle*, propriedade `identifier.value`. 


   Em "*system*", deve-se completar a URI ` http://www.saude.gov.br/fhir/r4/NamingSystem/BRRNDS-` com o número do identificador do solicitante (ver Identificador solicitante / *NamingSystem*). 
*  **Identificador atribuído pela RNDS**: também denominado de ID RNDS. Quando o registro é enviado com sucesso (*header* de resposta 201) à RNDS, no *header* `location` é gerada uma URL que é o identificador do registro na RNDS (ver Exemplos de consumo dos serviços). 


   **IMPORTANTE**: os *softwares* integradores DEVEM SALVAR o identificador local e o ID RNDS para que possam realizar ações futuras como: pesquisa, substituição (ver Substituição de registro na RNDS) e exclusão. 

### Segurança

 Somente com uma solicitação de acesso aprovada será possível realizar o consumo dos serviços (*web services*) do *EHR Services*. 

 Após a aprovação, o primeiro passo para realizar o consumo dos serviços é realizar a autenticação utilizando o serviço `POST@/token` no componente *EHR Auth*. Durante o processo de autenticação é verificado se o certificado digital está dentro do período de vigência e se ele, ou um de seus superiores na cadeia, foi revogado. 

 Caso não ocorra nenhum destes problemas, a operação de autenticação será realizada com sucesso e será retornado um *token* (`access_token`) com tempo de vida de 30 minutos. Este *token* deverá ser utilizado como token de autenticação nas chamadas dos serviços (*web services*) do *EHR Services*. A estrutura do *token* retornado é a seguinte: 

```
{
      "access_token": "eyJraWQiOiJybmRzIGF...",
      "scope": "read write",
      "token_type": "jwt",
      "expires_in": 1800000
}
```

A autenticação com certificado digital da RNDS utiliza a técnica chamada “*Two-way SSL*”. No “*Two-way SSL*”, além do certificado do servidor, o cliente também deve utilizar um certificado válido e que será conferido. Por outro lado, na autenticação SSL (ou “*One-way SSL*”) somente o certificado digital do servidor deve ser válido e será conferido. 

 Vale ressaltar que o certificado digital deve ser usado somente para realizar a autenticação e obter o *token*. 

A partir desse momento, o token é seu "*ticket*" de passe e todas as chamadas devem ser usadas utilizando somente este, não gerando a degradação de performance relacionada ao uso do certificado digital. Por isso, recomenda-se reutilizar o "*ticket*" ao máximo durante seu tempo de vida e só então obter um novo token repetindo a operação de autenticação com “*Two-way SSL*”.

Na página da RNDS no [Portal de Serviços do DATASUS](https://servicos-datasus.saude.gov.br/detalhe/urB3hXWTee) há um projeto de exemplo para obtenção do *token* utilizando a linguagem [ *Java* ](https://www.java.com/). 

### Ambientes de Integração

Seguindo as boas práticas serão disponibilizados dois ambientes para a integração: homologação e produção.

#### Ambiente de Homologação

O ambiente de homologação tem como finalidade validar a integração, seus parâmetros de entradas, saídas e comportamentos negociais, permitindo a realização de testes antes da efetiva comunicação com o ambiente de produção. O ambiente de homologação é único, ou seja, todos os interessados em realizar o consumo dos serviços (*web services*) utilizarão o mesmo ambiente. Porém, mesmo usando o mesmo ambiente, as informações trafegadas (incluídas ou consultadas) estarão restritas aos estabelecimentos de saúde (CNES) elencados na etapa de credenciamento. Os endereços dos componentes de integração, no ambiente de homologação, são:

* Utilizado para obtenção do token em ambiente de homologação:
*  Utilizado para comunicação com demais serviços do ambiente de Homologação: 

#### Evidências da Homologação

A partir dos testes realizados e da implementação local, serão aceitas como evidências dos testes em homologação um arquivo com:

* 1 print do validador com sucesso;
* 1 print do *header* de resposta de criação do registro na RNDS;
* 1 print do *Bundle* enviado.

Com essas evidências, o solicitante pode solicitar acesso ao ambiente de produção no [Portal de Serviços](https://servicos-datasus.saude.gov.br/).

### Ambiente de Produção

O ambiente de produção é o ambiente estável e real que provê os serviços (*web services*) a serem consumidos. Para o ambiente produtivo, os integradores deverão acessar os endereços dos seus estados (UF). Durante o credenciamento, a credencial de acesso (Certificado Digital) será associada a um estabelecimento de saúde (CNES) (ou conjunto de estabelecimentos de saúde) no Portal de Serviços do DATASUS. Com isso, a credencial de acesso pertencerá a um estado (UF) específico. Acessos a estados diferentes não são permitidos e serão bloqueados automaticamente pelos serviços (*web services*). Os endereços dos componentes de integração, no ambiente de produção, por estado, são:

| | |
| :--- | :--- |
| Acre | `https://ac-ehr-services.saude.gov.br/api/` |
| Alagoas | `https://al-ehr-services.saude.gov.br/api/` |
| Amapá | `https://ap-ehr-services.saude.gov.br/api/` |
| Amazonas | `https://am-ehr-services.saude.gov.br/api/` |
| Bahia | `https://ba-ehr-services.saude.gov.br/api/` |
| Ceará | `https://ce-ehr-services.saude.gov.br/api/` |
| Distrito Federal | `https://df-ehr-services.saude.gov.br/api/` |
| Espírito Santo | `https://es-ehr-services.saude.gov.br/api/` |
| Goiás | `https://go-ehr-services.saude.gov.br/api/` |
| Maranhão | `https://ma-ehr-services.saude.gov.br/api/` |
| Mato Grosso | `https://mt-ehr-services.saude.gov.br/api/` |
| Mato Grosso do Sul | `https://ms-ehr-services.saude.gov.br/api/` |
| Minas Gerais | `https://mg-ehr-services.saude.gov.br/api/` |
| Pará | `https://pa-ehr-services.saude.gov.br/api/` |
| Paraíba | `https://pb-ehr-services.saude.gov.br/api/` |
| Paraná | `https://pr-ehr-services.saude.gov.br/api/` |
| Pernambuco | `https://pe-ehr-services.saude.gov.br/api/` |
| Piauí | `https://pi-ehr-services.saude.gov.br/api/` |
| Rio de Janeiro | `https://rj-ehr-services.saude.gov.br/api/` |
| Rio Grande do Norte | `https://rn-ehr-services.saude.gov.br/api/` |
| Rio Grande do Sul | `https://rs-ehr-services.saude.gov.br/api/` |
| Rondônia | `https://ro-ehr-services.saude.gov.br/api/` |
| Roraima | `https://rr-ehr-services.saude.gov.br/api/` |
| Santa Catarina | `https://sc-ehr-services.saude.gov.br/api/` |
| São Paulo | `https://sp-ehr-services.saude.gov.br/api/` |
| Sergipe | `https://se-ehr-services.saude.gov.br/api/` |
| Tocantins | `https://to-ehr-services.saude.gov.br/api/` |

### Mensagens e Erros da RNDS

 Ao enviar registros para as APIs da RNDS, a plataforma pode retornar diferentes respostas com alguns códigos. O documento abaixo tem como objetivo listar e descrever os erros **(ERRXXX)** e as mensagens **(MSG)** da RNDS, ajudando a identificar e corrigir inconsistências. 

`[Link para o documento da lista de erros](https://mobileapps-prd.saude.gov.br/portal-servicos/files/f3bd659c8c8ae3ee966e575fde27eb58/fb46e2bf9dd140ecfd74424aee49a0a2_jdpiqrqwx.pdf)`
 
Sendo: 

* A **mensagem sistêmica** é o texto cadastrado no sistema para que seja exposto aos integradores no momento de envio do documento na RNDS.
* A **descrição do erro** é uma explicação mais detalhada sobre a mensagem sistêmica apresentada pela RNDS.

