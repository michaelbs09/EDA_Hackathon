# Hackathon - EDA de Aluguéis no Brasil

****

## 🔍 Sobre o projeto

Essa competição foi proposta como forma de estimular o desenvolvimento dos participantes em relação aos princípios fundamentais até conhecimentos mais avançados de uma Análise Exploratória de Dados. O objetivo principal desta análise é identificar padrões e correlações relevantes que possam impactar no valor dos aluguéis. Ao responder às 18 perguntas fornecidas no contexto do hackathon, buscamos agregar valor ao negócio imobiliário, fornecendo informações que podem orientar decisões estratégicas.<br>
<br>
Os critérios de avaliação do Hackathon, foram:
- Qualidade e Profundidade da Análise de Dados
- Criatividade
- Apresentação e Visualização de Dados
- Aplicabilidade e Relevância no Mundo Real

## 🔍 Sobre o Dataset

O dataset em questão contém dados do setor imobiliário no Brasil, o qual tem sido objeto de interesse recorrente, especialmente no que diz respeito aos aluguéis de residências. Inicialmente, ele possuía 10.692 instâncias (imóveis) e 13 features (características), mas após o tratamento dos valores faltantes e duplicados, ficamos com 10.334 imóveis para serem analisados.

Relação das features:
<ul>
    <li><strong>city:</strong> Cidade onde o imóvel está localizado.</li>
    <li><strong>area:</strong> Área do imovel.</li>
    <li><strong>rooms:</strong> Número de quartos.</li>
    <li><strong>bathroom:</strong> Número de banheiros.</li>
    <li><strong>parking spaces:</strong> Número de vagas para estacionamento.</li>
    <li><strong>floor:</strong> Andar.</li>
    <li><strong>animal:</strong> Aceita animais?</li>
    <li><strong>furniture:</strong> Imóvel é mobilhado?</li>
    <li><strong>hoa (R$):</strong> Valor do condomínio.</li>
    <li><strong>rent amount (R$):</strong> Valor do Aluguel.</li>
    <li><strong>property tax (R$):</strong> Valor do IPTU.</li>
    <li><strong>fire insurance (R$):</strong> Valor do seguro contra incendio.</li>
    <li><strong>total (R$):</strong> Valor total.</li>
</ul>

## 🗺️ Análise Exploratória de Dados

Aqui, separei algumas das perguntas dispostas na competição.

1. Existe uma correlação significativa entre a área do imóvel (area) e o valor do aluguel (rent amount)?

<img src="https://i.ibb.co/5KnrgPy/q1-a.png">

Valor de correlação entre Área do Imóvel e Valor do Aluguel é de 0.18. Como é possível observar, existem alguns outliers tanto para área quanto para o valor do aluguel. Vamos filtrar os dados para observar melhor essa relação entre essas duas variáveis.

<img src="https://i.ibb.co/hDzRhMW/q1-b.png">

Observando agora a faixa com maior concentração dos dados, podemos notar que existe uma leve tendência no aumento do valor do aluguel à medida que a área aumenta. Contudo, como já calculado, essa é uma correlação fraca, pois, existe uma dispersão considerável indicando uma variabilidade significativa nos tamanhos dos imóveis e nos valores de aluguel, isso se agrava ainda mais com a presença dos outliers observados.<br><br>
Por fim, a correlação positiva fraca sugere que, em geral, imóveis maiores têm tendência a ter valores de aluguel mais altos. No entanto, a variabilidade nos dados e a presença de outliers indicam que outros fatores também podem influenciar os valores de aluguel.

3. Qual é a proporção de imóveis mobiliados (furniture) e não mobiliados? Existe diferença no valor do aluguel entre eles?

<img src="https://i.ibb.co/Bq1FXhf/q3.png">
<img src="https://i.ibb.co/6138Qt2/Captura-de-tela-de-2024-02-24-10-33-40.png">

Nesse conjunto de dados, podemos visualizar que mais de 75% dos imóveis não possuem mobília previamente disponível para os inquilinos enquanto que menos de 1/4 dos 10334 imóveis são mobíliados. Como já era presumível o valor do aluguel dessas residências com mobília é maior que o valor para residências não mobiliadas, em mediana 46.04%.

13. A localização (cidade) tem impacto significativo na taxa de HOA?

<img src="https://i.ibb.co/ww8QKQ7/q13.png">

Analisando a relação cidade X taxa HOA, podemos destacar os seguintes insights:

- Belo Horizonte é a cidade mais impactada por outliers (observa-se pela média, uma medida de tendência central sensível a valores atípicos, que se desprende da região da mediana). Entretanto é, em valor mediano, a cidade com menor taxa HOA;
- Campinas e Porto Alegre possuem uma variação menor no valor da taxa HOA;
- São Paulo e Rio de Janeiro são as cidades com maior taxa HOA (desconsiderando os outliers).

Como esperado, podemos concluir que as grandes capitais são as cidades mais caras em relação a taxa HOA. Isso provavelmente é um reflexo da própria economia da região, que possui um custo de vida elevado.

****
Essas foram apenas algumas questões abordadas na competição. Sugiro a leitura completa do projeto, pois ele possui mais questões investigadas que podem fornecer informações valiosas para a tomada de decisões estratégicas.
