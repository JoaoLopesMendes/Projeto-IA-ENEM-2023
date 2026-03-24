# 📊 Dataset: Microdados ENEM 2023

Este projeto utiliza os microdados oficiais do Exame Nacional do Ensino Médio (ENEM) referentes ao ano de 2023. O conjunto de dados é mantido e publicado anualmente pelo Instituto Nacional de Estudos e Pesquisas Educacionais Anísio Teixeira (INEP).

---

## 1. 📥 Origem e Acesso

Os dados brutos foram extraídos do Portal de Dados Abertos do Governo Federal.

- **Fonte:** INEP - Microdados do ENEM (https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem) 
- **Licença:** Dados abertos de uso público, em conformidade com a Lei Geral de Proteção de Dados (LGPD), com dados anonimizados.

---

## 2. ⚙️ Estratégia de Amostragem e Compactação

Devido à volumetria do arquivo original (~2GB e ~3,9 milhões de registros), foi aplicado um pipeline de engenharia de dados para gerar o arquivo `amostra_enem_n1.csv` disponível neste repositório:

- **Filtragem de Presença:**  
  Foram mantidos apenas candidatos presentes em todos os dias de prova:  
  `TP_PRESENCA_CN`, `TP_PRESENCA_CH`, `TP_PRESENCA_LC`, `TP_PRESENCA_MT` == 1

- **Redução de Dimensionalidade:**  
  Seleção apenas das colunas relevantes ao estudo socioeconômico (questionário + notas)

- **Amostragem Aleatória:**  
  Extração de 100.000 registros  
  → Mantém representatividade estatística  
  → Reduz tamanho para < 25MB (melhor portabilidade)

---

## 3. 📚 Dicionário de Atributos

| Atributo           | Descrição                          | Observação |
|------------------|----------------------------------|----------|
| NU_INSCRICAO     | Identificador da inscrição       | Anonimizado |
| TP_ESCOLA        | Tipo de escola do Ensino Médio   | 1: Não informado; 2: Pública; 3: Privada |
| Q001             | Escolaridade do pai              | A (Nenhuma) a H (Pós-graduação) |
| Q002             | Escolaridade da mãe              | A (Nenhuma) a H (Pós-graduação) |
| Q006             | Renda mensal familiar            | A (Sem renda) a Q (> R$ 26.400) |
| Q025             | Acesso à internet em casa        | A: Não; B: Sim |
| NU_NOTA_CN       | Nota em Ciências da Natureza     | 0 a 1000 |
| NU_NOTA_CH       | Nota em Ciências Humanas         | 0 a 1000 |
| NU_NOTA_LC       | Nota em Linguagens e Códigos     | 0 a 1000 |
| NU_NOTA_MT       | Nota em Matemática               | 0 a 1000 |
| NU_NOTA_REDACAO  | Nota da redação                  | 0 a 1000 |
| NOTA_MEDIA       | Média das 5 notas                | Variável calculada |

---

## 4. 🧹 Pré-processamento e Limpeza

Para análise exploratória (EDA) e modelagem preditiva, foram aplicadas as seguintes transformações:

- **Tratamento de Nulos:**  
  Remoção de registros com notas ausentes ou dados socioeconômicos incompletos

- **Mapeamento de Categorias:**  
  Conversão das variáveis categóricas (letras) para valores descritivos e monetários (BRL)

- **Normalização:**  
  Preparação dos dados para algoritmos de machine learning (Scikit-Learn)

---

## 📌 Notas de Versão

- **Versão:** 1.0 (Entrega N1)  
- **Estado:** Amostra compactada para desenvolvimento  
- **Observação:**  
  O pipeline completo para processamento do dataset integral está disponível no diretório `/scripts`

---
