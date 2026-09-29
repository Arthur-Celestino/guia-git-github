# Ciclo de Vida de um Projeto com Git e GitHub

## 🚀 Sessão 1: O Passo a Passo da Criação e Envio

O GitHub é uma plataforma que permite armazenar projetos na nuvem, acompanhar alterações e compartilhar códigos com outras pessoas. Para utilizá-lo, podemos criar um repositório online e conectá-lo a uma pasta do nosso computador.

### 1. Criando um repositório no GitHub

Primeiramente, acesso o site do [GitHub](https://github.com/) e entro na minha conta. Em seguida, clico em **New repository** para criar um novo repositório.

Depois, realizo as seguintes configurações:

* **Repository name:** escolho um nome para o projeto.
* **Description:** escrevo uma breve descrição do projeto.
* **Public ou Private:** escolho se o repositório será público ou privado.
* **Add a README:** deixo desmarcado para criar um repositório vazio, caso já tenha os arquivos no computador.

Por fim, clico em **Create repository**. Assim, o repositório é criado na nuvem.

### 2. Conectando a pasta local ao GitHub

Para conectar uma pasta do meu computador ao repositório, abro o terminal na pasta do projeto e utilizo os seguintes comandos:

```bash
git init
```

Esse comando inicia o Git na pasta, permitindo acompanhar as alterações dos arquivos.

```bash
git branch -M main
```

Esse comando define o nome da branch principal como `main`.

Em seguida, conecto a pasta ao repositório remoto:

```bash
git remote add origin URL_DO_REPOSITORIO
```

Substituo `URL_DO_REPOSITORIO` pelo endereço do repositório criado no GitHub.

### 3. Realizando o primeiro envio

Depois de conectar a pasta, preciso preparar e enviar os arquivos para o GitHub. Para isso, sigo esta sequência:

**1. Adicionar os arquivos**

```bash
git add .
```

Esse comando prepara os arquivos da pasta para serem registrados.

**2. Criar o commit**

```bash
git commit -m "Primeiro commit"
```

O commit registra as alterações realizadas, acompanhado de uma mensagem que explica o que foi feito.

**3. Enviar os arquivos**

```bash
git push -u origin main
```

Esse comando envia os arquivos e o commit para o repositório remoto no GitHub.

Após concluir essas etapas, os arquivos ficam disponíveis na página do repositório. Caso seja solicitado, preciso autenticar minha conta do GitHub para autorizar o envio.

---

## 📖 Sessão 2: A Anatomia do README Perfeito

### 1. Propósito do README

O arquivo `README.md` é um documento que apresenta as principais informações de um projeto. Ele funciona como um guia para explicar o objetivo do projeto, suas funcionalidades e como utilizá-lo.

Seu público-alvo são outros desenvolvedores, professores, colegas de equipe, recrutadores e qualquer pessoa interessada em conhecer o projeto.

Um README bem organizado facilita o entendimento do código e demonstra cuidado e organização por parte do desenvolvedor.

### 2. Informações essenciais de um README profissional

Um README deve apresentar informações importantes para que qualquer pessoa consiga entender e utilizar o projeto.

1. **Título:** apresenta o nome do projeto e facilita sua identificação.
2. **Descrição:** explica o objetivo do projeto, o problema que ele busca resolver e suas principais funcionalidades.
3. **Tecnologias utilizadas:** informa quais linguagens, ferramentas e tecnologias foram utilizadas no desenvolvimento, como HTML, CSS, JavaScript e Git.
4. **Instalação e execução:** apresenta as instruções necessárias para baixar, configurar e executar o projeto no computador.
5. **Funcionalidades:** descreve os principais recursos disponíveis e o que o usuário pode fazer com o sistema.
6. **Status do projeto:** informa se o projeto está em desenvolvimento, concluído ou se ainda existem melhorias planejadas.
7. **Licença:** explica as condições de uso, modificação e distribuição do projeto, quando houver uma licença definida.
8. **Autor:** identifica quem desenvolveu o projeto e pode incluir links para o GitHub ou outros perfis profissionais.

### 3. O poder do Markdown

O Markdown é uma linguagem de marcação simples utilizada para formatar textos. Ela permite organizar as informações sem precisar utilizar códigos complexos de formatação.

No arquivo README.md, podemos utilizar:

* `#` para criar títulos.
* `**texto**` para deixar o texto em negrito.
* `*texto*` para deixar o texto em itálico.
* `-` para criar listas.
* `` `código` `` para destacar comandos e trechos de código.
* `[Texto](URL)` para inserir links.

A principal vantagem do Markdown é facilitar a criação de documentos organizados e fáceis de ler. Além disso, o GitHub interpreta essa formatação e apresenta o README de maneira visualmente organizada na página do projeto.

---

## 🔄 Sessão 3: O Mapa das Atualizações (Commits e Pushes)

Depois de criar um repositório, é importante mantê-lo atualizado. Existem diferentes maneiras de realizar alterações e enviá-las para o GitHub.

### 1. GitHub Online

O GitHub permite editar arquivos diretamente pelo navegador, sem precisar abrir o terminal ou instalar programas adicionais.

Para isso, acesso o arquivo desejado no repositório, clico no ícone de edição, realizo as alterações e finalizo criando um commit.

**Quando utilizar:** para corrigir pequenos erros, atualizar o README ou modificar informações simples.

**Limitações:** não é tão prático para projetos grandes, alterações em vários arquivos ou tarefas que exigem testes e execução do código localmente.

### 2. Git via Linha de Comando (Terminal)

O Git pelo terminal permite controlar as versões do projeto por meio de comandos. É uma forma tradicional e bastante utilizada por desenvolvedores, pois oferece controle sobre as alterações e facilita a automação de tarefas.

O fluxo de atualização funciona da seguinte maneira:

```bash
git status
git add .
git commit -m "Descrição da alteração"
git push
```

* `git status`: mostra os arquivos modificados.
* `git add .`: prepara as alterações para o commit.
* `git commit -m`: registra as alterações com uma mensagem.
* `git push`: envia os commits para o GitHub.

Essa forma é bastante utilizada porque permite trabalhar com diferentes projetos, controlar versões e integrar o Git a outras ferramentas de desenvolvimento.

### 3. IDEs (Exemplo: Visual Studio Code)

O Visual Studio Code possui uma interface gráfica integrada ao Git, permitindo acompanhar as alterações e realizar commits e pushes sem precisar digitar todos os comandos no terminal.

Na aba **Source Control (Controle do Código-Fonte)**, consigo visualizar os arquivos modificados, selecionar quais serão incluídos no commit, escrever uma mensagem e confirmar as alterações.

Depois, utilizo a opção de sincronização ou envio para publicar os commits no GitHub.

Essa ferramenta facilita o trabalho porque reúne a edição do código e o controle de versões no mesmo ambiente. Também permite utilizar o terminal integrado quando necessário.

### 4. GitHub Desktop

O GitHub Desktop é um programa que facilita o uso do Git por meio de uma interface gráfica.

Com ele, consigo visualizar as alterações realizadas, comparar as versões dos arquivos, escrever mensagens de commit e enviar as atualizações para o GitHub.

Uma de suas vantagens é tornar o processo mais visual e simples, principalmente para quem está começando a aprender Git. Dessa forma, não é necessário memorizar todos os comandos para realizar as operações mais comuns.

### 5. A filosofia da atualização contínua

Manter o repositório atualizado é importante porque permite acompanhar a evolução do projeto e manter um histórico das alterações realizadas.

Realizar commits pequenos e frequentes facilita a identificação de erros, a correção de problemas e a compreensão do que foi modificado em cada etapa.

Além disso, o envio contínuo das atualizações reduz o risco de perder trabalho e facilita a colaboração entre os integrantes de uma equipe.

Portanto, é mais organizado atualizar o GitHub durante o desenvolvimento, em vez de deixar todas as alterações para o final do mês. Dessa maneira, o histórico fica mais claro, o projeto permanece atualizado e o desenvolvedor consegue acompanhar sua própria evolução.

---

## Conclusão

O GitHub é uma ferramenta importante para armazenar projetos, controlar versões e compartilhar conhecimentos. Aprender a criar repositórios, realizar commits, enviar atualizações e documentar projetos com o README ajuda a desenvolver boas práticas de programação.

Com o uso do Git, do GitHub e de ferramentas como o Visual Studio Code e o GitHub Desktop, o desenvolvimento se torna mais organizado e facilita o trabalho individual e em equipe.
