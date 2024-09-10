# Documentação do Código HTML: Vili Brûlée - Doces Artesanais

## Sumário
1. [Visão Geral](#visão-geral)
2. [Estrutura do Documento](#estrutura-do-documento)
3. [Estilo e Layout](#estilo-e-layout)
4. [Funcionalidades JavaScript](#funcionalidades-javascript)
5. [Considerações Especiais](#considerações-especiais)

## 1. Visão Geral

O código fornecido é um documento HTML que cria uma página de apresentação para "Vili Brûlée - Doces Artesanais". Esta página inclui um card estilizado que destaca o nome da empresa, slogan, e oferece botões para acessar o cardápio, localização, e informações sobre a empresa. Além disso, há botões para redes sociais e funcionalidades de compartilhamento.

## 2. Estrutura do Documento

### 2.1 Cabeçalho (`<head>`)

- **Meta Tags**:
  - `charset="UTF-8"`: Define a codificação de caracteres como UTF-8.
  - `viewport`: Ajusta o layout para diferentes tamanhos de tela.

- **Título**: 
  - `<title>`: Define o título da página como "Vili Brûlée - Doces Artesanais".

- **Links para Estilos**:
  - `leaflet.css`: Biblioteca CSS para mapas (Leaflet).
  - `font-awesome.css`: Biblioteca de ícones Font Awesome.
  - `Playfair Display` e `Lora`: Fontes do Google Fonts.

- **Estilos Internos**:
  - Definem o estilo da página, incluindo o layout, aparência dos botões e modais, e responsividade para dispositivos móveis.

### 2.2 Corpo (`<body>`)

- **Card Principal**:
  - `<div class="card">`: Contém o conteúdo principal, incluindo o fundo, título, slogan e botões.

- **Botões**:
  - **Cardápio**: Redireciona para o cardápio online.
  - **Localização**: Abre um modal com o mapa.
  - **Sobre Nós**: Abre um modal com informações sobre a empresa.
  - **Instagram**: Redireciona para o perfil no Instagram.
  - **WhatsApp**: Abre o WhatsApp para uma mensagem pré-definida.

- **Modais**:
  - **Mapa**: Modal com um mapa incorporado e botões para abrir em Waze ou Google Maps.
  - **Sobre Nós**: Modal com uma breve descrição da empresa.

## 3. Estilo e Layout

O CSS define a aparência da página, com as seguintes características principais:

- **Body**:
  - Centraliza o card na tela com flexbox.
  - Define a fonte e cor de fundo.

- **Card**:
  - Aplica um fundo com uma imagem, bordas arredondadas, e sombra.
  - Ajusta o layout com flexbox para centralizar o conteúdo.

- **Título e Slogan**:
  - Estilizados com uma fonte serifada e sombra de texto para melhorar a legibilidade.

- **Botões**:
  - Estilizados como círculos com gradiente radial.
  - Mudam de cor e escala ao serem clicados.

- **Modais**:
  - São ocultos por padrão e aparecem sobre um fundo escuro quando ativados.
  - Contêm um botão de fechamento e estilo específico para cada tipo de modal.

- **Responsividade**:
  - Ajusta o tamanho e layout dos elementos para telas menores.

## 4. Funcionalidades JavaScript

### 4.1 Funções Principais

- **`openWhatsApp()`**:
  - Abre o WhatsApp com uma mensagem predefinida para encomendas.

- **`initMap()`**:
  - Inicializa o mapa Leaflet com um marcador na localização da empresa.

- **`openMap(mapType)`**:
  - Abre a localização em Waze ou Google Maps com base no tipo de mapa selecionado.

- **`openInstagram()`**:
  - Tenta abrir o aplicativo Instagram e, se não conseguir, redireciona para o site.

- **`openAboutModal()`**:
  - Abre o modal com informações sobre a empresa.

- **`closeModal(modalId)`**:
  - Fecha o modal especificado.

- **`shareCard()`**:
  - Usa a API de compartilhamento do navegador para compartilhar a página.

### 4.2 Eventos

- **Botão "Compartilhar"**: Aciona a função `shareCard()` para compartilhar a página.
- **Botão "Localização"**: Abre o modal do mapa e inicializa o mapa.
- **Botão "Sobre Nós"**: Abre o modal com informações sobre a empresa.
- **Botão "Instagram"**: Tenta abrir o aplicativo Instagram ou redireciona para o site.
- **Botão "WhatsApp"**: Abre o WhatsApp com uma mensagem predefinida.

## 5. Considerações Especiais

- **Compatibilidade com Navegadores**: O código utiliza a API de compartilhamento, que pode não ser suportada em todos os navegadores.
- **Mapas**: O mapa utiliza a biblioteca Leaflet e é carregado dinamicamente quando o modal é aberto.
- **Instagram**: O comportamento para abrir o aplicativo pode variar entre dispositivos e navegadores.
