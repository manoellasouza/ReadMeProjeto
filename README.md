
<img align="right" alt="logo-compass" height="100" style="border-radius:50px;" src="https://i.ibb.co/0nq71pK/LOGO-1.png"> 


# Projeto Integrador - DiaZen

Projeto apresentado ao Centro Universitário Senac, como exigência parcial para obtenção de aprovação na disciplina Projeto Integrador IV, do curso de Análise e Desenvolvimento de Sistemas.


## Tópicos
   * [Instalando o projeto](#instalando-o-projeto)
      * [Pré-requisitos](#pré-requisitos)
      * [Preparando o ambiente](#preparando-o-ambiente)
      * [Passos iniciais após clonar o repositório](#passos-iniciais-após-clonar-o-repositório)
      * [Criando nova branch para desenvolvimento](#criando-nova-branch-para-desenvolvimento)  
   * [Executando os testes](#executando-os-testes)
      * [Resultados](#resultados)
   * [Sobre o projeto](#sobre-o-projeto)
      * [Diretório](#diretório)
      * [Frameworks utilizados](#frameworks-utilizados)
   * [Referências](#referências)
   * [Autores](#autores)

## Instalando o projeto 

### Pré-requisitos 

- <a href='https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/8.2.4/xampp-windows-x64-8.2.4-0-VS16-installer.exe'>Xampp</a>: pacote que contém os componentes MySQL e PHP;
- <a href='https://getcomposer.org/Composer-Setup.exe'>Composer</a>: ferramenta de gerenciamento de dependências em PHP;
- <a href='https://www.heidisql.com/installers/HeidiSQL_12.5.0.6677_Setup.exe'>HeidiSQL</a>: utilizado para acessar o banco de dados.

### Preparando o ambiente 

1. Instale o Xampp;
2. Instale o Composer adicionando o PHP no patch do sistema operacional;
3. Instale o HeidiSQL;
> *Atenção*: para executar o Xampp é necessário executá-lo como administrador do sistema;

### Passos iniciais após clonar o repositório

1. Renomeie o arquivo '.env.example' para '.env';
2. Execute o comando ```composer install```;
3. Configure os dados do banco de dados dentro de '.env';
4. Execute o comando ```php artisan key:generate```;
5. Execute o comando ```php artisan migrate```;
6. Inicie o projeto através do comando ```php artisan serve```.


### Criando nova branch para desenvolvimento

1. Verifique a sua branch atual utilizando o comando ```git branch```;
2. 
- Se exiter na branch main, use o comando 'git checkout -b <nome_da_branch/#numero_da_issue_aberta>'. **Exemplo**:
```
git checkout -b anotso/#1
```
- Caso não esteja na branch main use o comando 'git checkout main';
- Na branch main execute o 'git pull origin main' **antes de iniciar o desenvolvimento de qualquer nova atividade**;
- Caso não exista issue aberta no repositório do projeto é só cria-lá. Caso seja destinada para um outro integrante é só informar no grupo e passar a URL para a pessoa.





## Executando os testes
1. Rode a ServeRest localmente pelo terminal:  ```npx serverest ```
> Não feche este terminal enquanto estiver realizando os testes!

2. Baixe os <a href="https://github.com/manoellasouza/RoboTron_Manoella_Souza_Projeto_Final/tree/main/extras/arquivos-bdd-testes">arquivos .bdd</a> deste repositório e faça a substituição em ```C:\Users\NomeUsuario\AppData\Local\npm-cache\_npx\5ae2362f38c57068\node_modules\serverest\src\data```. Esses arquivos contêm os dados base de cadastro usados para realizar os testes deste projeto.

2. Abra o projeto através do VS Code. Os arquivos com os cenários de teste estarão na pasta tests.

3. Abra um terminal dentro da pasta do projeto e execute os testes localmente de acordo com as opções abaixo:
- Todos os endpoints: ```robot -d ./reports ./tests```
- Endpoint /login: ``` robot -d ./reports ./tests/login_tests.robot ```
- Endpoint /usuarios: ``` robot -d ./reports ./tests/usuarios_tests.robot ```
- Endpoint /produtos: ``` robot -d ./reports ./tests/produtos_tests.robot ```
- Endpoint /carrinhos: ``` robot -d ./reports ./tests/carrinho_tests.robot ```
- Utilizando a TAG de cada cenário, por exemplo: ``` robot -d ./reports -i GETALLUSERS ./tests/usuarios_tests.robot ```

### Resultados

Ao executar os testes, o resultado é apresentado no terminal e os arquivos report.html e log.html são gerados:

![image](https://user-images.githubusercontent.com/100487940/188459886-25f55d58-31c8-4ddc-924d-05c58b0b03b6.png)

O <a href="https://github.com/manoellasouza/RoboTron_Manoella_Souza_Projeto_Final/blob/main/extras/imagens/report.png">report.html</a> é um resumo que mostra o status da execução, horário de início e de término, tempo total da execução e a quantidade de testes que passou e que falhou. Já o <a href="https://github.com/manoellasouza/RoboTron_Manoella_Souza_Projeto_Final/blob/main/extras/imagens/log.png">log.html</a> detalha os testes, mostrando cada keyword utilizada, a library da keyword, logs solicitados e resultado da execução.


## Sobre o projeto 

A automação de testes de uma API é importante para que os testes e as correções sejam realizados em menos tempo, o que diminui os custos com as correções e acelera o lançamento do produto.

### Diretório
- :file_folder: [extras/](extras): Dir com os arquivos extras deste repositório
  - :file_folder: [arquivos-bdd-testes/](extras/arquivos-bdd-testes): Dir com os arquivos .bdd base utilizados para realizar os testes
  - :file_folder: [imagens/](extras/imagens): Dir com as imagens de exemplo de Log e Report 
- :file_folder: [keywords/](keywords): Dir com as keywords utilizadas nos testes 
- :file_folder: [reports/](reports): Dir com os relatórios de resultados dos testes realizados, incluindo o report.html e o log.html
- :file_folder: [support/](support): Dir com os arquivos base, massas de dados e variáveis
  - :file_folder: [common/](support/common): Dir com o arquivo commom.robot, a library em Python e o arquivo .robot que consome essa library
  - :file_folder: [fixtures/](support/fixtures): Dir com todas as massas de dados
    - :file_folder: [static/](support/fixtures/static): Dir com as massas de dados estáticas
  - :file_folder: [variables/](support/variables): Dir com o arquivo .robot que contém as variáveis padrão utilizadas
- :file_folder: [tests/](tests): Dir com os arquivos de teste .robot para cada endpoint da API
- :page_with_curl: [funcoes-python-explicadas](funcoes-python-explicadas): Arquivo explicando o código e os objetivos das funções utilizadas na library criada com Python 
- :page_with_curl: [mapa-mental/](mapa-mental): Arquivo com o mapa mental de todas as rotas da API



### Frameworks utilizados
- <a href="https://robotframework.org/robotframework/latest/libraries/BuiltIn.html#library-documentation-top">BuiltIn</a>: library padrão do Robot que possui as palavras-chave mais utilizadas
- <a href="https://marketsquare.github.io/robotframework-requests/doc/RequestsLibrary.html#library-documentation-top">RequestsLibrary</a>: utilizada para fazer as requisições HTTP REST



## Referências
- <a href="https://serverest.dev/#/">Documentação da API ServeRest</a>
- <a href="https://github.com/PauloGoncalvesBH/sample-supertest">Repositório Supertest - Inspiração de ReadMe</a>




## Autores
<a href="https://www.linkedin.com/in/manoellasouza/">Manoella Souza</a>









