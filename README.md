# Devstage - Sistema de Inscrição e Convite

Este projeto é um sistema simples de inscrição em evento, com funcionalidade de convite e contagem de inscritos por referência.

## Estrutura dos Arquivos

- `index.html`: Estrutura principal da página, carrega o app e os estilos.
- `style.css`: Estilos visuais do sistema.
- `script.js`: Lógica de funcionamento do sistema (inscrição, convite, contagem).
- `logo.svg` e outros ícones: Imagens utilizadas na interface.

---

## Como funciona cada parte

### 1. Interface (index.html + style.css)

- O arquivo `index.html` define a estrutura da página, incluindo o cabeçalho com logo e título, e um container `#app` onde o conteúdo dinâmico é exibido.
- O arquivo `style.css` estiliza todos os elementos, garantindo responsividade e visual moderno.

### 2. Lógica de Inscrição e Convite (script.js)

#### a. Estrutura de Dados

- Os usuários são armazenados em um array `users`, cada um com `email`, `phone`, `ref` (código de referência) e `refBy` (quem convidou).

#### b. Fluxo de Inscrição

- Ao carregar a página, o formulário de inscrição é exibido.
- O usuário preenche email e telefone.
- Ao enviar, o sistema verifica se o email já está cadastrado:
  - Se sim, mostra a tela de convite e estatísticas daquele usuário.
  - Se não, cria um novo usuário, atribui um código de referência aleatório e mostra a tela de convite.

#### c. Tela de Convite

- Após inscrição, o usuário recebe um link único com seu código de referência.
- O sistema mostra quantas pessoas se inscreveram usando o código daquele usuário.

#### d. Contagem de Inscritos

- A função `getTotalSubscribers` retorna quantos usuários foram cadastrados com o código de referência do usuário atual.

#### e. Atualização de Imagens

- A função `updateImageLinks` garante que todos os ícones sejam carregados corretamente via URL.

#### f. Reinício

- Clicar no cabeçalho reinicia o app, voltando ao formulário de inscrição.

---

## Como rodar

1. Abra o arquivo `index.html` em seu navegador.
2. Preencha o formulário para simular inscrições e convites.
3. O sistema é totalmente front-end e não salva dados após recarregar a página.

---

## Licença

MIT License © João Felipe

