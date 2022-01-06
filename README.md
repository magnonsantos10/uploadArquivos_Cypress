# uploadArquivos_Cypress
Realizando upload de arquivos com Cypress

### Instalação

* Inicialmente vamos precisar do plugin `cypress-file-upload`, sua instalação é bem simples, basta executar o comando abaixo: 

```
npm install cypress-file-upload --save-dev
```

![image](https://user-images.githubusercontent.com/91263334/148432406-0fa5b1b7-41f0-4414-810f-0aa0f30cc182.png)

* Após a instalação você verá que uma nova devDependencia foi adcionada ao arquivo `package.json` com a versão do `cypress-file-upload`

![image](https://user-images.githubusercontent.com/91263334/148432700-b188041f-4995-412e-959f-616b35839abf.png)

### Configurações

* Feito isso vamos adicionar o arquivo desejado no pastinha `fixtures`, essa pastinha fica localizada no projeto dentro da pasta Cypress

```
./cypress/fixtures
```

![image](https://user-images.githubusercontent.com/91263334/148434530-f77861b4-7a39-4ccf-921a-36e8179ea882.png)

**Observação**: Para adicionar o arquivo para a pastinha de fixtures é só arrastar da pasta de destino para a pata fixtures

* Configurando `index.js` >> Aqui vamos importar as congurações de plugin para que possamos utiliza-los no código, veja:

```
./cypress/support/index.js
```

`import 'cypress-file-upload'`

### Código

* Após concluir a instalação e configuração, chegou a hora de codar, abaixo segue um código de exemplo que utilizei em um projeto real.

![image](https://user-images.githubusercontent.com/91263334/148434969-345cb553-6a33-4306-8cc7-af3b6b02b0f3.png)

* exemplificando o código: Repare na imagem acima onde utilizei uma variável, dentro desta variável eu passei um parâmetro com o nome de `importArea`, após passar por todos os passos, quando clico no botão de busca, então passo a chamada `input[type="file"]`, nela uso a biblioteca `attachFile` e dentro dessa biblioteca eu chamo a minha variável com o parâmetro que desejo utilizar, um ponto muito importante também é que o valor do parâmetro deve ser exatamente o nome do arquivo com a extensão exata que colocamos dentro de `fixtures`. Todo esse processo é que vai fazer o arquivo ser pré-selecionado, após isso só clicar para importar e fazer as devidas validações.
