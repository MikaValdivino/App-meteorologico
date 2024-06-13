# Aplicativo Meteorológico

## Este código é um exemplo de uma aplicação web para exibir informações meteorológicas baseadas na localização fornecida pelo usuário. A aplicação inclui HTML, CSS e JavaScript. 

# HTML
O HTML define a estrutura básica da página web:

### Cabeçalho (head):

- Define o charset e o viewport.
- Inclui links para folhas de estilo externas, como Boxicons e uma folha de estilo local (style.css).

### Corpo (body):

- Contém um div com a classe container que agrupa todos os elementos.
- Dentro do container:
- Caixa de pesquisa (search-box): Inclui um ícone de mapa, um campo de entrada de texto para o usuário digitar a localização e um botão de pesquisa.
- Parágrafo oculto (city-hide): Armazena temporariamente o nome da cidade para comparação.
- Caixa de clima (weather-box): Exibe informações do tempo, incluindo uma imagem, temperatura e descrição.
- Detalhes do clima (weather-details): Exibe informações adicionais como umidade e velocidade do vento.
- Mensagem de erro (not-found): Exibe uma mensagem de erro caso a localização não seja encontrada.
- Inclui um script JavaScript (main.js) para funcionalidades interativas.


# CSS
O CSS estiliza a página e controla a visibilidade e animação dos elementos:

- Define estilos globais para margens, preenchimento e fonte.
- Estilos do corpo para centralizar o conteúdo e definir um fundo.
- Estilos específicos para container, search-box, weather-box, weather-details, e not-found:
- Transições e animações: Transições suaves para mostrar/ocultar elementos.
- Visibilidade: Elementos como weather-box, weather-details, e not-found são inicialmente ocultos e exibidos somente quando necessário.

  
# JavaScript
O JavaScript adiciona funcionalidade interativa para buscar e exibir dados meteorológicos:

1. Seleção de Elementos: Usa querySelector para obter referências aos elementos da página.
   
2. Evento de Clique no Botão de Pesquisa:
- Obtém a chave da API e o valor da cidade do campo de entrada.
- Faz uma solicitação à API do OpenWeatherMap usando fetch.

3. Manipulação da Resposta:
- Se a cidade não for encontrada (json.cod == "404"), mostra a mensagem de erro e oculta as informações do clima.
- Se a cidade for encontrada, atualiza os elementos da página com as informações do clima (imagem, temperatura, descrição, umidade e velocidade do vento).

4. Animações e Clonagem de Elementos:
- Adiciona classes CSS para transições suaves.
- Clona e insere elementos de informações para criar um efeito visual de animação.
- Remove clones antigos após um tempo para manter a interface limpa.

# Funcionamento Geral

- Quando o usuário digita uma localização e clica no botão de pesquisa, o JavaScript faz uma chamada à API para obter os dados do clima.
- Se a localização for encontrada, os dados são exibidos com uma animação suave.
- Se a localização não for encontrada, uma mensagem de erro é exibida.
- O CSS garante que as transições sejam suaves e que a interface seja visualmente agradável.
- A estrutura HTML organiza todos os elementos de forma lógica e semântica.


