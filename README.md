# Ficha Técnica: Projeto Análise de Dados 

## Titulo do projeto: Acomodações Airbnb em Nova York

### Objetivo 

Efetuar uma análise exploratória e utilizar técnicas avançadas de BI para visualizar tendências, identificar padrões e compreender os fatores que influenciam a ocupação do alojamento. Desde a sazonalidade elevada até as preferências regionais, diversos aspectos serão examinados para desvendar informações valiosas. O objetivo final é fornecer uma base sólida para a tomada de decisões informadas, permitindo que as partes interessadas adotem medidas estratégicas para aprimorar a eficiência operacional e lucratividade no dinâmico ecossistema do Airbnb.

<details>
  <summary><strong> Processamento e Análises: Avaliação das Tabelas HOSTS, REVIEWS e ROOMS para Garantir a Qualidade dos Dados e a Consistência da Análise no Projeto Airbnb</strong></summary>

### Tabela “HOSTS”:

- Identifiquei:
  - 18 nulos na variável “host_name”.
  - Optei pela exclusão dos 18 valores nulos, por entender que não irão comprometer a análise.
  
- Foram identificados 124 valores na coluna **host_id** que estavam incorretamente preenchidos como string. Esses dados foram excluídos para evitar inconsistências na análise.

### Tabela “REVIEWS”:

- 20 nulos na variável “number_of_reviews”.
- 10.039 nulos na variável “last_review”.
- 10.019 nulos na variável “reviews_per_month”.
- 156 nulos na variável “availability_365”.
- 136 valores preenchidos incorretamente como datas na variável “number_of_reviews”.

Os nulos das variáveis “number_of_reviews” e “availability_365” foram excluídos, por entender que são menos de 1% da base de dados, assim como os valores preenchidos como datas.

- Foram identificados 9 valores na coluna **id** que estão preenchidos como string. Esses IDs também foram excluídos para garantir a consistência da análise.

### Linhas da Tabela “REVIEWS”:
| **Linha** | **id**                |
|-----------|-----------------------|
| 1         | Midtown               |
| 2         | Nearby UN             |
| 3         | Central Park          |
| 4         | All included          |
| 5         | Crown Heights         |
| 6         | Astoria               |
| 7         | Window in NYC         |
| 8         | Spacious              |
| 9         | Medical personnel      |

Preenchi os valores ausentes da coluna “reviews_per_month” com 0, por entender que o cliente optou por não efetuar a review.

### Tabela “ROOMS”:

- Sem valores nulos.
- IDs duplicados foram removidos, deixando apenas os únicos.

### Linhas da Tabela “ROOMS”:
| **Linha** | **id**                     |
|-----------|----------------------------|
| 1         | Brownstone"                |
| 2         | AFFORDABLE PRICE"          |
| 3         | Mount Sinai"               |
| 4         | NEAR TO YANKE STADIUM"     |
| 5         | 15 min F Times Square"     |
| 6         | muy cercadetodo"           |
| 7         | Se habla Español"          |

Em seguida, transferi as 3 tabelas para o Power BI para criar o relacionamento entre elas e aplicar técnicas avançadas de análise.
</details>


<details>
  <summary><strong>Análise Exploratória e Novas Variáveis para Aprofundar a Compreensão das Acomodações do Airbnb em Nova York, Focando em Aspectos de Disponibilidade e Ganhos Potenciais</strong></summary>

### Power BI

- Fórmulas DAX
- Porcentagem de quartos por bairro
- Porcentagem de quartos indisponíveis
- Porcentagem de quartos disponíveis
- Coluna de ganhos possíveis, para calcular quanto o cliente poderia ganhar alugando o quarto todos os dias.
- Nova coluna de nomes limpos, pois os nomes estavam agrupados.
- Coluna de total de hóspedes por ano.
</details>



<details>
  <summary><strong> Resultados e Conclusões</strong></summary>

Temos um total de 49 mil hosts em Nova York.

O bairro com a maior porcentagem de acomodações é **Manhattan**.

Os quartos com as médias de preços mais altas estão localizados em **Manhattan** e **Brooklyn**.

**Manhattan** se destaca como o bairro mais caro para alugar no Airbnb.

Na base disponível, podemos observar que, ao longo dos anos, a média de avaliações dos hóspedes tende a aumentar.
</details>


<details>
  <summary><strong> Limitações e Próximos Passos</strong></summary>

- Número de dias que a acomodação esteve ocupada.

- Quantidade de hóspedes permitida.

- Número médio de noites que os hóspedes costumam alugar.
</details>

## Para uma ficha técnica mais detalhada e consultas SQL, consulte:
[Notion](https://www.notion.so/PROJETO-BI-FICHA-T-CNICA-111abd8a87ea80faad29e916c959754a)

