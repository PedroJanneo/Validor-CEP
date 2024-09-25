# README - Validação de CEP Automático

## Descrição

Este projeto é uma aplicação web para validar CEPs (Códigos de Endereçamento Postal) no Brasil. O usuário pode inserir um CEP e, ao clicar em "Consultar", as informações do endereço correspondente são exibidas nos campos apropriados.

## Estrutura do Projeto

A aplicação é composta pelos seguintes arquivos principais:

- `index.html`: Contém a estrutura HTML da página.
- `style.css` : Contém a estilização da página.
- `js/dados.js`: Contém dados fictícios de CEPs para simulação.
- `js/carregarDados.js`: Script que manipula a entrada do usuário e busca informações.

## Tecnologias Utilizadas

- HTML
- CSS
- JavaScript (ES6 Modules)

## Como Usar

1. **Abra o arquivo `index.html`** em um navegador.
2. **Insira um CEP** no campo designado.
3. **Clique no botão "Consultar"** para buscar as informações.
4. **Os dados do endereço** (logradouro, bairro, cidade, estado e complemento) serão preenchidos automaticamente se o CEP for válido.

## Funcionamento

### `dados.js`

Este arquivo contém um objeto chamado `dadosCep`, que possui um array de objetos com informações de CEPs. Cada objeto inclui:

- `cep`: O código postal.
- `logradouro`: O nome da rua ou logradouro.
- `complemento`: Informações adicionais sobre o endereço.
- `bairro`: O bairro correspondente ao CEP.
- `localidade`: A cidade.
- `uf`: A Unidade Federativa (Estado).
- Outros dados relevantes.

- Foi usado para entender a lógica de como funciona os input.

### `carregarDados.js`

Esse arquivo é responsável por:

- **Validar o CEP** inserido pelo usuário.
- **Buscar dados** tanto em um array local (do arquivo `dados.js`) quanto via API externa (`viacep.com.br`).
- **Preencher o formulário** com os dados correspondentes quando o CEP é encontrado.

### Funções Principais

- **validarDados()**: Verifica se o CEP está vazio ou se é inválido.
- **getBuscarCEP()**: Busca os dados do CEP no array local.
- **getBuscarCepAPI()**: Faz uma requisição à API para buscar dados de CEP.
- **setDadosForm(dadosCep)**: Preenche os campos do formulário com os dados recebidos.

## Exemplo de Uso

1. Insira um CEP válido, como `01001-000`.
2. Clique em "Consultar".
3. Os campos serão preenchidos com as informações do endereço correspondente.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

## Licença

Este projeto é de uso livre. Sinta-se à vontade para utilizá-lo e adaptá-lo conforme suas necessidades.
