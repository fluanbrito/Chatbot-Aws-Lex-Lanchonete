## Integração com <a href="https://developers.facebook.com/products/" target="_blank"> <img src="https://imgs.search.brave.com/Lm3QSaaOMnI19WcTOtDADCI5Z6ZaTeujhZrHElNP6co/rs:fit:650:240:1/g:ce/aHR0cDovL3d3dy5h/cnRpdC1rLmNvbS93/cC1jb250ZW50L3Vw/bG9hZHMvMjAxNC8w/OS9GYWNlYm9vay1E/ZXZlbG9wZXJzLUxv/Z28ucG5n" alt="firebase" width="100" height="50" title="Slack"/> </a> 

Para integrar o bot criado no Amazon Lex V2 ao Facebook Messenger, você precisa seguir os seguintes passos:

1 - Crie um aplicativo no Facebook for Developers e adicione o Facebook Messenger como uma plataforma de produto.

- Acesse o site do Facebook for Developers em https://developers.facebook.com/ e faça login com sua conta do Facebook.
![01](https://user-images.githubusercontent.com/94761781/221447434-bafcc3c3-3b17-43fa-bf48-daa7876a93d5.png)

- Clique em "Meus Aplicativos" no canto superior direito da página e na sequência selecione "Criar Aplicativo".
![02](https://user-images.githubusercontent.com/94761781/221447439-ebbe9ba9-96c1-45a5-9222-96abbb1f4214.png)

- Selecione um tipo para sua Aplicação, clique em "Avançar" e digite um nome para o seu aplicativo. 

![03](https://user-images.githubusercontent.com/94761781/221447440-e288cb08-0efd-4c27-8756-08f564ed1a18.png)
![04](https://user-images.githubusercontent.com/94761781/221447442-c176def0-6cb2-4029-8da2-1e159c3bf98e.png)
    - não selecione a página agora, crie assim para ter mais disposição de serviços 

- Na página de inicial do aplicativo, seção de "Adicionar Produtos ao seu Aplicativo", localize e clique em "configurar" para adicionar a sua página e gerar o Token

    ![05](https://user-images.githubusercontent.com/94761781/221447444-27520eb5-6313-4721-8748-0cf6a658e9d3.png)

   Essa opção só irá aparecer se na criação do aplicativo você não selecioinar nem uma Página, pois assim terá mais privilégios sobre os serviços

- Na página de configuração do Messenger, selecione a página do Facebook que você deseja associar ao bot e clique em "Gerar Token de Acesso à Página".

![07](https://user-images.githubusercontent.com/94761781/221447453-4b9bc14a-3602-44ea-9c51-65dee49bd8ab.png)
![07 1](https://user-images.githubusercontent.com/94761781/221447450-2ead2a72-ec85-4b28-a22e-fc22feb21223.png)


    - Copie o token gerado e guarde-o em um local seguro.


2 - Configure o webhook do aplicativo do Facebook para apontar para o endpoint do Amazon Lex V2. Para fazer isso, você precisará fornecer a URL do endpoint do Amazon Lex V2 e um token de verificação.

- Na seção "Webhooks" da página de configuração do Messenger, clique em "Configurar Webhooks" e insira a URL do endpoint do Amazon Lex V2.
![08 00](https://user-images.githubusercontent.com/94761781/221447456-ddf7342b-3e80-4a9c-962b-a6eca0c9840e.png)
***ESSE TOKEN DE VERIFICAÇÃO É O ALIAS DA CRIAÇÃO DO ENDPOINT***

      - se ainda não houver endpoint vá na console em
      Lex > Bots  > Bot: MegaLanches > Channel integrations > Add channel  
      Selecione o Facebook e configure
   ![08 1](https://user-images.githubusercontent.com/94761781/221447459-604ddf77-9590-42ae-a9a7-f2245ed91d96.png)
   ![08 2](https://user-images.githubusercontent.com/94761781/221447460-66438245-10b8-4933-9b75-481be74f2b6e.png)
   ***App Secrret Key*** é chave secreta que está em configurações > básico
   ***Page Acess Token*** é o Token gerado na página


  ![08 4](https://user-images.githubusercontent.com/94761781/221447462-2028776a-d1da-4e1a-a92f-26bd9f2b8fbf.png)
- Selecione as opções de assinatura de eventos que você deseja receber e clique em "Verificar e Salvar".

3 - Teste o bot no Facebook Messenger.  
  -    <img src="https://user-images.githubusercontent.com/94761781/221450105-6c31b2c9-a41a-4bd6-b1e8-7cfedc87b506.jpeg" width="200">

Acesse a página: https://www.facebook.com/profile.php?id=100089482627701&mibextid=ZbWKwL

**Para mais detalhes, [acesse a documentação](https://docs.aws.amazon.com/lex/latest/dg/fb-bot-association.html) de integração do Faceboook ao Lex**.