# Festivite — Formulário de Convite Digital

Projeto prático desenvolvido durante o curso **Fullstack** da [Rocketseat](https://www.rocketseat.com.br/), com foco em estruturação semântica de formulários HTML e estilização avançada de campos com CSS puro.

## Sobre o projeto

A **Festivite** é uma interface de criação de convites digitais para eventos. O usuário preenche um formulário completo com informações do evento, opções de personalização visual e dados de contato, e ao final gera o convite clicando em **"Gerar convite"**.

## Layout

A interface é dividida em dois painéis principais:

- **Aside** — painel lateral com logo, nome da aplicação e imagem de fundo temática.
- **Main** — painel principal com o formulário de criação do convite, com scroll independente.

## Funcionalidades

O formulário é organizado em três seções:

### Sobre o evento
- Título do evento
- Data e hora de início e fim (`datetime-local`)
- Tipo do evento: **Presencial** ou **Online** (radio buttons customizados com ícones)
- Local (link ou endereço)
- Descrição

### Personalização
- **Cor principal** — seleção via color swatches (radio buttons estilizados com cores CSS variables)
- **Tema do evento** — cards com imagens para: Aniversário, Infantil, Formatura, Casamento, Chá de bebê, Chá de panela, Carnaval, Páscoa, São João, Halloween, Natal, Outro
- **Estilo** — toggle switch Escuro/Claro (checkbox customizado)
- **Foto de capa** — upload de imagem com campo de arquivo estilizado

### Dados para contato
- Nome completo (com validação e mensagem de erro acessível)
- E-mail
- Telefone

### Rodapé do formulário
- Aceite de Termos e Condições e Política de Privacidade (checkbox)
- Aceite de comunicações por e-mail e SMS (checkboxes opcionais)
- Botão de envio: **Gerar convite**

## Tecnologias utilizadas

- **HTML5** — marcação semântica, atributos de acessibilidade (`aria-hidden`, `aria-describedby`), campos nativos (`datetime-local`, `file`, `radio`, `checkbox`, `textarea`)
- **CSS3** — layout com CSS Grid e Flexbox, variáveis CSS (`custom properties`), pseudo-classes de estado (`:hover`, `:focus-visible`, `:checked`)
- **Google Fonts** — Leckerli One, Baloo 2, Open Sans

## Estrutura de arquivos

```
invite-form/
├── index.html
├── assets/
│   ├── icons/          # Ícones SVG do formulário
│   └── images/         # Imagens dos temas e background
└── styles/
    ├── index.css        # Importa todos os estilos
    ├── globals.css      # Reset, variáveis CSS e utilitários
    ├── layout.css       # Grid principal (aside + main)
    ├── form.css         # Estrutura geral do formulário
    └── fields/
        ├── index.css          # Importa os estilos dos campos
        ├── input.css          # Inputs, textarea e file upload
        ├── radio.css          # Radio buttons com ícones
        ├── color-radio.css    # Swatches de cor
        ├── style-radio.css    # Toggle switch de estilo
        ├── theme-card-radio.css  # Cards de tema do evento
        └── checkbox.css       # Checkboxes customizados
```

## Como executar

Por ser um projeto estático (HTML + CSS), basta abrir o arquivo `index.html` diretamente no navegador ou utilizar uma extensão como o **Live Server** no VS Code.

---

Desenvolvido com dedicação durante a trilha Fullstack da Rocketseat.
