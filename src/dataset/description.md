# Dataset: Microdados ENEM 2023

Este projeto utiliza os microdados oficiais do Exame Nacional do Ensino Médio (ENEM) referentes ao ano de 2023. O conjunto de dados é mantido e publicado anualmente pelo Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP).

---

## 1. Origem e Acesso

Os dados brutos foram extraídos do Portal de Dados Abertos do Governo Federal.

- **Fonte:** INEP - Microdados do ENEM (https://download.inep.gov.br/microdados/microdados_enem_2023.zip) (obs: não conseguimos upar o dataset no github devido ao seu tamanho)
- **Licença:** Dados abertos de uso público, em conformidade com a Lei Geral de Proteção de Dados (LGPD), com dados anonimizados.

---

## 2. Dicionário de Variáveis


| Variável | Descrição |
|---|---|
| NU_INSCRICAO | Número de inscrição do participante |
| TP_FAIXA_ETARIA | Faixa etária do participante |
| TP_SEXO | Sexo do participante |
| TP_ESTADO_CIVIL | Estado civil |
| TP_COR_RACA | Cor/raça autodeclarada |
| TP_NACIONALIDADE | Nacionalidade |
| TP_ST_CONCLUSAO | Situação de conclusão do ensino médio |
| TP_ANO_CONCLUIU | Ano de conclusão do ensino médio |
| TP_ESCOLA | Tipo de escola |
| TP_ENSINO | Tipo de ensino |
| IN_TREINEIRO | Indica se o participante é treineiro |
| CO_MUNICIPIO_ESC | Código do município da escola |
| NO_MUNICIPIO_ESC | Nome do município da escola |
| CO_UF_ESC | Código da UF da escola |
| SG_UF_ESC | Sigla da UF da escola |
| TP_DEPENDENCIA_ADM_ESC | Dependência administrativa da escola |
| TP_LOCALIZACAO_ESC | Localização da escola |
| TP_SIT_FUNC_ESC | Situação de funcionamento da escola |
| TP_PRESENCA_CN | Presença em Ciências da Natureza |
| TP_PRESENCA_CH | Presença em Ciências Humanas |
| TP_PRESENCA_LC | Presença em Linguagens e Códigos |
| TP_PRESENCA_MT | Presença em Matemática |
| NU_NOTA_CN | Nota de Ciências da Natureza |
| NU_NOTA_CH | Nota de Ciências Humanas |
| NU_NOTA_LC | Nota de Linguagens e Códigos |
| NU_NOTA_MT | Nota de Matemática |
| NU_NOTA_REDACAO | Nota da Redação |
| Q001 | Escolaridade do pai |
| Q002 | Escolaridade da mãe |
| Q005 | Quantidade de pessoas na residência |
| Q006 | Faixa de renda familiar |
| Q024 | Possui computador em casa |
| Q025 | Possui acesso à internet |

## Observações

- As variáveis iniciadas com `TP_` representam categorias/tipos definidos pelo INEP.
- As variáveis iniciadas com `NU_` representam valores numéricos, como notas.
- As variáveis iniciadas com `Q` correspondem ao questionário socioeconômico do ENEM.

