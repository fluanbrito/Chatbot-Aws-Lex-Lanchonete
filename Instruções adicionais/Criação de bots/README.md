## Passo a passo para a criação de um bot

1 - Ao acessar o serviço na console, já uma breve aboradagem.... Clique em *Criar bot a partir de um modelo*.
![01](https://user-images.githubusercontent.com/94761781/221339202-d0c91b13-a92a-4029-a767-4c9578d54738.png)

2 - De forma semelhante se já tiver alguns bots, haverá um outro rearranjo, mas configura a mesma situação anterior. Prossiga clicando em *Create Bot*.
![1 5](https://user-images.githubusercontent.com/94761781/221339194-aef37fe9-98cb-496a-9244-e74396576e46.png)

3 - Na próxima visualização marque proceda com os componentes indicados e ao final clique em *next*.
![2](https://user-images.githubusercontent.com/94761781/221339199-987f99b2-7cf6-4c0a-9aba-284c4431cfa1.png)
Na raia *IAM permissions*, selecione a opção *Create a role with basic Amazon Lex permissions*. Logo em seguida, selecione *Não* na opção *Children's Online Privacy Protection* e deixe tempo de sessão na escolha padrão (poderá ser alterado futuramente).

4 - A próxima tela se refere a configuração de todos os idiomas que o bot suportará. Selecione Português como opção, e deixar a Voice Interaction em 
``` "None". This is only a text based application” ```.
![2 5](https://user-images.githubusercontent.com/94761781/221339196-e01f5c50-6256-4bf3-9025-d190c9cddb5e.png)

5 - Após a criação será solicitada a princípio a criação de intenções
![2 6](https://user-images.githubusercontent.com/94761781/221339198-b74b5efd-2906-4c3a-a9b4-b57294781ac9.png)

6 - Segue as respectivas *intents* utilizadas para o chatbot:
![3](https://user-images.githubusercontent.com/94761781/221339200-bfb74b51-9bae-494a-bcf9-f1aca4f62b26.png)

7 - Sobre os *slots*, observa-se os seguintes desenvolvidos para entrega desse chatbot
![5](https://user-images.githubusercontent.com/94761781/221339426-67b25a8b-ca9b-4e78-9399-f8027cf8add2.png)

8 - Criadas Itens, pode-se prosseguir com a exploração da aba lateral.

<img src="https://user-images.githubusercontent.com/94761781/221339201-189f750d-fad3-4dfe-a30a-3c7659d4fdfc.png" width="140">

``` Bot versions ```
 Possibilita o versionamento e controle de versões do bot.

```Idioma```
É a seção principal para o desenvolvedor. Nela, é possível criar intents e slots, que são a base do funcionamento de qualquer chatbot. 

```Deployment```
A opção de aliases serve para realizar o controle de versões e de ambientes de desenvolvimento.
Enquanto o versions possibilita a criação de versões, os aliases permitem a criação de ambientes
como homologação e produção, que apontam para versões desejadas no bot. Integrações com canais de comunicação podem ser realizadas nesta aba.

**A documentação utilizada para o desenvolvimento desse documento se encontra [aqui](https://compasso-my.sharepoint.com/personal/lucas_sousa_compasso_com_br/_layouts/15/onedrive.aspx?ga=1&id=%2Fpersonal%2Flucas%5Fsousa%5Fcompasso%5Fcom%5Fbr%2FDocuments%2FDocs%20Lex%2FDocumentacao%5FAmazon%5FLex%2Epdf&parent=%2Fpersonal%2Flucas%5Fsousa%5Fcompasso%5Fcom%5Fbr%2FDocuments%2FDocs%20Lex)**.