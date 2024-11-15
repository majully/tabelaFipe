# Consulta Veículo Tabela FIPE

Projeto implementado durante curso Alura posto como desafio. Aplicação para consultar o valor médio de veículos (carros, motos ou caminhões) de acordo com a tabela FIPE, que pode ser acessada através [desse site](https://veiculos.fipe.org.br/).

- A consulta aos valores dos veículos pelo site tem o seguinte fluxo:
- Primeiramente é necessário escolher o tipo do veículo: carro, moto ou caminhão.

1


- Depois disso, é necessário preencher a MARCA, MODELO e ANO para consulta.

2


- Por fim, é exibida a avaliação apenas daquele ano escolhido.

3



## 🚗 Projeto Tabela FIPE

- O objetivo do projeto é ter um fluxo similar ao que é feito no site, porém com algumas melhorias.
- Projeto Spring com linha de comando, utilizando a classe Scanner para fazer interações com o usuário via terminal.
- O usuário digita o tipo de veículo desejado (carro, caminhão ou moto).
- Listando todas as marcas daquele tipo de veículo, solicitando que o usuário escolha uma marca pelo código.
- Após escolha, lista todos os modelos de veículos daquela marca.
- O usuário digita um trecho do modelo que ele quer visualizar, por exemplo **PALIO**.
- Lista apenas os modelos que tiverem a palavra **PALIO** no nome.
- Usuário escolherá um modelo específico pelo código e, diferente do site, já listaremos as avaliações para **TODOS** os anos disponíveis daquele modelo, retornando uma lista de forma similar à imagem abaixo:

4



## Observações:

- API consumida, documentada [nesse link](https://deividfortuna.github.io/fipe/).

- Endpoints abaixo para buscar as marcas:

https://parallelum.com.br/fipe/api/v1/carros/marcas

https://parallelum.com.br/fipe/api/v1/motos/marcas

https://parallelum.com.br/fipe/api/v1/caminhoes/marcas

- O retorno dessa requisição será uma lista com código e marca desejada. Caso o usuário queira por exemplo fazer uma consulta a modelos de carros da Fiat, que possui o código 21, terá que fazer uma nova requisição para o endpoint:

https://parallelum.com.br/fipe/api/v1/carros/marcas/21/modelos

- Feito isso, irá escolher um código de modelo, por exemplo esse **Palio Weekend Stile 1.6 mpi 16V 4p**, representado pelo código 560. Então deverá fazer uma terceira requisição para o endpoint:

https://parallelum.com.br/fipe/api/v1/carros/marcas/21/modelos/560/anos

- Para saber a avaliação para cada ano disponível, e feita uma requisições pelo código por ano, retornando similar ao que é mostrado abaixo:

https://parallelum.com.br/fipe/api/v1/carros/marcas/21/modelos/560/anos/2003-1

5
