<hr>

# 📑 Chatbot Amazon lex - Lanchonete.

Trata-se de um chatbot desenvolvido para uso de uma lanchonete, que vende kit de salgados.

<hr>
<p align="center">
  
## Tópicos 

- [🧾 Descrição do projeto](#-descrição-do-projeto)

- [⚙️ Ferramentas e tecnologias](#⚙-ferramentas-e-tecnologias)

- [📝 Requisitos](#-requisitos)

- [🤖 Estrutura do chatbot](#-estrutura-do-chatbot)

- [🔌 Integração com Slack](#-integração-com-slack)

- [😟 Impedimentos](#-impedimentos)

- [📌 Considerações finais](#-considerações-finais)

- [📝 Informações adicionais](#-informações-adicionais)

- [🧑‍🤝‍🧑 Equipe](#-equipe)

<hr>

## 🧾 Descrição do projeto 
Com base na [documentação do Amazon Lex](https://compasso-my.sharepoint.com/:f:/g/personal/lucas_sousa_compasso_com_br/Eph8d9BDeRhGhBzyoAYRLZUBhfjA54P1-5YHERGaN5_Osg?e=1ibFDI), foi realizada a construção de um chatbot utilizando o Amazon Lex V2 e a integração com as plataformas de mensageria [Slack](https://slack.com/) e [Facebook Messenger](https://www.messenger.com/).
A funcionalidade do bot faz analogia ao atendimento online de uma fábrica de salgados, nesse contexto, a MegaLanches.

<p align="justify">
<hr>

## ⚙️ Ferramentas e tecnologias 

<a href="https://aws.amazon.com/pt/" target="_blank"> <img src="https://imgs.search.brave.com/GMxBwk4HNqhFJEmYkqXOW8kelyHphegTgfv8jGX3E3M/rs:fit:1200:1197:1/g:ce/aHR0cHM6Ly9naXN1/c2VyLmNvbS93cC1j/b250ZW50L3VwbG9h/ZHMvMjAxOC8wOC8y/MDAwcHgtQW1hem9u/X1dlYl9TZXJ2aWNl/c19Mb2dvLnN2Z18u/cG5n" alt="aws" width="40" height="40" title="AWS"/> </a><a href="https://docs.aws.amazon.com/pt_br/lexv2/latest/dg/what-is.html" target="_blank"> <img src="https://imgs.search.brave.com/bVZ4uQWr-3duPfutx8MysuJr104Mk89zeMApyYVzVjg/rs:fit:300:300:1/g:ce/aHR0cHM6Ly9zeW1i/b2xzLmdldHZlY3Rh/LmNvbS9zdGVuY2ls/XzcvM19hbWF6b24t/cmVrb2duaXRpb24u/NmFkOGEzYzFiOC5w/bmc" alt="firebase" width="40" height="40" title="AWS LexV2"/> </a> <a href="https://slack.com/intl/pt-br/media-kit" target="_blank"> <img src="https://imgs.search.brave.com/eEl2VJx5Re6JoRirC111bGSvKYC2Hj0Hltdn26O5pbA/rs:fit:1200:1200:1/g:ce/aHR0cHM6Ly9jZG4u/ZnJlZWJpZXN1cHBs/eS5jb20vbG9nb3Mv/bGFyZ2UvMngvc2xh/Y2stMS1sb2dvLXBu/Zy10cmFuc3BhcmVu/dC5wbmc" alt="firebase" width="40" height="40" title="Slack"/> </a><a href="https://developers.facebook.com/products/" target="_blank"> <img src="https://imgs.search.brave.com/Lm3QSaaOMnI19WcTOtDADCI5Z6ZaTeujhZrHElNP6co/rs:fit:650:240:1/g:ce/aHR0cDovL3d3dy5h/cnRpdC1rLmNvbS93/cC1jb250ZW50L3Vw/bG9hZHMvMjAxNC8w/OS9GYWNlYm9vay1E/ZXZlbG9wZXJzLUxv/Z28ucG5n" alt="firebase"  height="40" title="Slack"/> </a> 

<hr>

## 📝 Requisitos

- Conta na [AWS](https://aws.amazon.com/pt/account/)
  - Serviço [Amazon Lex](https://aws.amazon.com/lex/): cria chatbots com inteligência artifical conversacional.

<hr>

## 🤖 Estrutura do chatbot

### Intents
- **Saudacao_Intent** apresentação do bot e menu principal.
- **Pedido_Intent** conecta o menu principal e a escolha dos kits. 
- **Kit_Intent** revela os combos de salgados disponíveis e pede a quantidade.
- **Retirada_Intent** retirar o pedido na loja.
- **Entrega_Intent** fornece a escolha do usuário pedir delivery dos salgados.
- **Pagamento_Intent** oferece as formas de pagamento.
- **PagDinheiro_Intent** pagamento em dinheiro.
- **AvaliacaoServico_Intent** julgamento do usuário sobre a qualidade do serviço.
- **Question_Intent** pergunta para gerar um abatimento no total da compra.
- **Desconto_Intent** desconto para o pedido.
- **Sobre_Intent** conta uma breve história da empresa.
- **Sair_Intent** cancela a interação com o bot.
- **FallbackIntent** tratamento de erros.

### Slots
- **KitSelecionado** a escolha do combo desejado.
- **Quantidade** quantos kits o usuário deseja pedir.
- **Bairro** detalhamento dos bairros onde a empresa atua.
- **FormaPagamento** opções de pagamento.
- **Troco** quanto de troco necessário caso o usuário escolha o *delivery*.
- **Feedback** avaliação do serviço.
- **Retirada** variações da escolha de buscar os salgados.

<hr>

## 🔌 Integração com Slack 

O chatbot está sendo disponibilizado na seguinte plataforma:
  - Slack - [Conexão Slack](https://docs.aws.amazon.com/pt_br/lex/latest/dg/slack-bot-association.html);  

1 - Para realizar a integração, inicialmente criamos o bot conforme detalhado anteriormente.

2 - Realizamos um  [cadastro na plataforma Slack](https://slack.com/intl/pt-br/).

3 - Criamos a aplicação Slack na [Plataforma de Desenvolvedores](https://api.slack.com/).

![criando app](https://user-images.githubusercontent.com/103221427/221373306-2c9fbdfb-9053-4b95-ba18-2a7318a94ada.png)

4 - Definindo nome e configurações básicas para obtenção do token de verificação.

![criando nome](https://user-images.githubusercontent.com/103221427/221375218-98172466-fe99-412b-a740-f1181595e718.png)

![interatividade](https://user-images.githubusercontent.com/103221427/221375376-50dfb9a8-cae4-41eb-a0f4-f327c1bbcc5d.png)

5 - Em sequência, no menu esquerdo consultamos os tokens disponibilizados através dos campos:

> Settings > Basic Information

6 - Realizando configuração no console da AWS.

![plataforma aws](https://user-images.githubusercontent.com/103221427/221376414-d09a9643-4540-4e0c-a513-2e1cd70fa6de.png)

Atribuindo nome à integração e selecionando o alias do bot criado e o idioma utilizado

![Config Integração](https://user-images.githubusercontent.com/103221427/221376543-25c118b4-3647-48b0-acbb-403268a34ebc.png)

7 - Em seguida, deve-se preencher os campos indicados no menu de **Configuração adicional** com os tokens obtidos no passo 5 e clicar em **Adicionar**.

8 - Com o canal devidamente criado, selecione-o e anote o Endpoint e o Endpoint OAuth.

9 - Voltando a página do slack, no menu **OAuth & Permissions**, foram realizadas as seguintes modificações: 

> **Redirect URLs** > Add New Redirect URL > Adicionar o Endpoint OAuth fornecido no passo 8

> **Scopes** > Add an OAuth Scope > Adicionar: chat:write e team:read

A página OAuth & Permissions deve ficar assim: 

![url slack](https://user-images.githubusercontent.com/103221427/221377760-73fe9f38-6fb0-43d9-8f19-75400e816ea6.png)

10 - Voltando ao menu **Interactivity e Shortcuts** devemos substituir a URL definida no passo 4 pelo Endpoint fornecido no console da AWS.

11 - No menu **Event Subscriptions** foram realizadas as seguintes modificações:

> **Enable Events** > Request URL > Adicionar o Endpoint fornecido no passo 8

> **Subscribe to bot events** > Add bot User event > Adicionar: message.im

A página Event Subscriptions deve ficar assim: 

![final config](https://user-images.githubusercontent.com/103221427/221378247-eaf9c37c-85da-4c13-a91b-68267ef652cd.png)

12 - Para finalizar no Menu **Manage Distribution em Settings**:
> Clique em **Add to Slack**.

> Na solicitação de permissões selecione permitir.

> Selecione o app e na aba Mensagens comece a interagir com o bot!

##### Resultado da integração

![resultado](https://user-images.githubusercontent.com/103221427/221378685-fdcdf354-a830-4ed2-940f-7796337a2233.png)

O projeto pode ser acessado por este [link](https://join.slack.com/t/equipe1-pbcompass/shared_invite/zt-1px13neg5-y1DZNGcReDflShTsZnQQYg).



<hr>

## 😟 Impedimentos
Desenvolver um chatbot Lex V2 integrado com Slack e Facebook Messenger nos apresentou alguns desafios. 
- Configuração: Configurar corretamente o bot no Amazon Lex, Slack e Facebook Messenger, dado que se deve seguir cuidadosamente as documentações e guias disponíveis para garantir que tudo esteja configurado corretamente.
- Teste e Ajuste: Testar e ajustar o bot para garantir que ele esteja funcionando corretamente pode levar tempo. É importante testar o bot em diferentes cenários para identificar problemas e ajustar suas respostas de acordo.
- Utilização de *lambdas*.
- Diferenças nas documentações do slack e do amazon lex para as versões atuais: Solucionado com estudo e pesquisa das ferramentas.

***

## 📌 Considerações Finais


De modo geral, consideramos o projeto de chatbot Lex V2 integrado com Slack e Facebook Messenger incluindo os seguintes eixos de ênfase:

- Foco no usuário: É importante focar na experiência do usuário ao desenvolver o chatbot. Isso significa entender as necessidades dos usuários e projetar o bot para atender a essas necessidades de maneira eficaz...

- Monitoramento contínuo: É importante monitorar continuamente o chatbot para identificar problemas e oportunidades de melhoria. Isso pode envolver análise de dados e feedback dos usuários.

- Iteração constante: O desenvolvimento de chatbot é um processo contínuo e iterativo. É importante estar disposto a fazer ajustes e melhorias no bot com base em feedback e análise contínuos.

<hr>

## 📝 Informações adicionais

### Criação do bot

O passo a passo para a criação de um bot no Lex está [aqui](https://github.com/Compass-pb-aws-2022-IFCE/sprint-7-pb-aws-ifce/tree/Grupo-1/Instru%C3%A7%C3%B5es%20adicionais/Cria%C3%A7%C3%A3o%20de%20bots).

### Facebook Messenger

As instruções para realizar a conexão do Facebook com o bot Lex está detalhada [aqui](https://github.com/Compass-pb-aws-2022-IFCE/sprint-7-pb-aws-ifce/tree/Grupo-1/Instru%C3%A7%C3%B5es%20adicionais/Integra%C3%A7%C3%A3o%20Lex%20bot%20com%20Facebook%20%20Messenger).

<hr>

## 🧑‍🤝‍🧑 Equipe

- [Luan Ferreira](https://github.com/fluanbrito)
- [Mylena Soares](https://github.com/mylensoares)
- [Jhonnatan Gonçalves](https://github.com/jhonatangoncalvespereira)
- [Rafael Pereira](https://github.com/Kurokishin)
