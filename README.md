## PROJETO(WebService/API)

### Baixar a pasta com o projeto

Fazer o download da pasta zipada pelo link https://github.com/rodrigosalles7/Desafio-BackEnd/archive/refs/heads/main.zip ou se preferir utilizar o terminal executando:
```
git clone ttps://github.com/rodrigosalles7/Desafio-BackEnd.git 
```

### Instalação do Postman

1. Baixar o Postman para Windows 64-bit através do link https://www.postman.com/downloads/;
2. Realizar a instalação;
3. Abrir o Postman e criar uma conta.

### Importar a Collection e o Environment

1. Com o Postman aberto, selecione **import** e posteriormente **Upload Files**.

![image](https://user-images.githubusercontent.com/72480923/163622465-aa7a6e57-ff46-4e62-a345-0febf1e68447.png)

2. Selecione a Collection e o Environment desejado e clique em abrir.

![image](https://user-images.githubusercontent.com/72480923/163622597-19269370-09b2-4e68-b4b3-2f18a4962bb6.png)

3. Clique em **Import** para abrir os arquivos dentro do Postman.

![image](https://user-images.githubusercontent.com/72480923/163623824-c9ea0016-34e6-4a02-bce2-942c456042b5.png)

### Alterar o Environment

Altere a opção do Environmet de **No Environment** para **Teste** que foi importado anteriormente.

![image](https://user-images.githubusercontent.com/72480923/163624122-3c8901d4-7214-46d5-923e-e6ec16043de7.png)

### Realizar os testes

1. Selecione uma Request (eu selecionei o **POST - Criar usuário com email diferente**);
2. Confira em **Body** se os dados estão preenchidos e possuem um email válido;
3. Clique em **Send** para executar o teste.

![image](https://user-images.githubusercontent.com/72480923/163624490-6b860f8c-60bb-4b3b-8a6e-4b86eafbbae8.png)

4. Observe em **Body** os dados apresentado e em **Test Results** o Status code e a mensagem exibida.

![image](https://user-images.githubusercontent.com/72480923/163625229-b86b1994-f64d-4ed7-a6f4-cb667b9d117c.png)

![image](https://user-images.githubusercontent.com/72480923/163625271-8c7d56e1-91a7-4159-b04d-069b1231202b.png)

Para realizar outro teste de outra Request, basta seguir os passos anteriores, porém os que utilizam o método **GET** e **DELETE** não usam o **Body** para entrada de dados, mas sim para conferir a mensagem de resposta depois de uma requisição de teste.

Para o teste que realiza uma busca ou uma exclusão, que necessita utilizar um **ID**, é preciso pegar o **ID** desejado (ele pode ser obtido na Request do **GET - Listar todos os usuários cadastrados**) e colar na barra de endereço juntamente com a URL.

![image](https://user-images.githubusercontent.com/72480923/163626845-4d451e58-bcf4-421e-b503-4108786ffc03.png)

### Realizar todos os testes de forma automática utilizando um Script

1. Na aba de **Collections**, clique em **...*** que está na frente da collection **Casos de testes**;
2. Posteriormente clique em **Run collection**.

![image](https://user-images.githubusercontent.com/72480923/163627404-a6b439ef-05ae-4a19-b336-59918d8a138c.png)

3. Observe que é possível rodar o teste com mais de 1 iteração, isso pode ser alterado em **Iterations**;
4. O tempo de atraso entre os casos de testes também pode ser alterado, observe que ele é apresentado em **ms**;
5. Verifique se todos os testes que você queira rodar estejam selecionados;
6. Por fim, clique no botão **Run Casos de testes** para executar os testes.

![image](https://user-images.githubusercontent.com/72480923/163627907-47cb36e2-a02e-4bc5-9f37-3167915e8ee0.png)

7. Observe os resultados dos testes. É possível verificar que alguns foram sucesso (**Pass**) e outros deram erro (**Fail**), isso se da por conta dos usuários que já estão cadastrados ou não. Para resolver, é necessário preencher alguns dados nas Requests como: um **ID** correto e um errado nos métodos **GET** e preencher com um email ainda não cadastrado um já cadastrado nos métodos **POST**.

![image](https://user-images.githubusercontent.com/72480923/163628530-72cd734c-d7fa-4ca9-8aff-588a15de65be.png)

### Scripts utilizados

Para visualizar os Scripts que foram utilizados, basta selecionar uma Request qualquer e clicar em **Tests**, na caixa de texto exibida é possível ver o código.

Se quiser saber quais Scripts foram utilizados nas outras Requests, é só selecionar a desejada e repetir o passo anterior.

![image](https://user-images.githubusercontent.com/72480923/163629489-0eefc1b9-0200-4ded-aa38-cd62846955b6.png)

