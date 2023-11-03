
<img align="right" alt="logo-compass" height="100" style="border-radius:50px;" src="https://i.ibb.co/0nq71pK/LOGO-1.png"> 


# Projeto Integrador - DiaZen

Projeto apresentado ao Centro Universitário Senac, como exigência parcial para obtenção de aprovação na disciplina Projeto Integrador IV, do curso de Análise e Desenvolvimento de Sistemas.

## Tópicos
   * [Sobre o projeto](#sobre-o-projeto)
   * [Instalando o projeto](#instalando-o-projeto)
      * [Pré-requisitos](#pré-requisitos)
      * [Preparando o ambiente](#preparando-o-ambiente)
   * [Executando o projeto](#executando-o-projeto)
      * [Passos iniciais após clonar o repositório](#passos-iniciais-após-clonar-o-repositório)
      * [Criando nova branch para desenvolvimento](#criando-nova-branch-para-desenvolvimento)  
   * [Referências](#referências)
   * [Autores](#autores)

## Sobre o projeto 

O DiaZen tem como objetivo auxiliar pessoas com ansiedade e/ou depressão a alcançarem seus objetivos, servindo como uma ferramenta de autoconhecimento. O aplicativo oferece diversos benefícios para pessoas que têm dificuldade em realizar suas tarefas desejadas, o que é comum em pessoas com ansiedade e/ou depressão:
- Auxílio no alcance de objetivos;
- Facilitação da expressão dos pensamentos ao conquistar metas;
- Melhor entendimento das limitações individuais para que possam ser trabalhadas a fim de serem superadas, trabalhando assim a elevação da autoestima;
- Auxiliar o usuário a descobrir e/ou redescobrir experiências que foram benéficas.

## Instalando o projeto 

### Pré-requisitos 

- <a href='https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/8.2.4/xampp-windows-x64-8.2.4-0-VS16-installer.exe'>Xampp</a>: pacote que contém os componentes MySQL e PHP;
- <a href='https://getcomposer.org/Composer-Setup.exe'>Composer</a>: ferramenta de gerenciamento de dependências em PHP;
- <a href='https://www.heidisql.com/installers/HeidiSQL_12.5.0.6677_Setup.exe'>HeidiSQL</a>: utilizado para acessar o banco de dados.

### Preparando o ambiente 

1. Instale o Xampp;
2. Instale o Composer adicionando o PHP no patch do sistema operacional;
3. Instale o HeidiSQL.
> *Atenção*: para executar o Xampp é necessário executá-lo como administrador do sistema.

## Executando o projeto 

### Passos iniciais após clonar o repositório

1. Renomeie o arquivo '.env.example' para '.env';
2. Execute o comando ```composer install```;
3. Configure os dados do banco de dados dentro de '.env';
4. Execute o comando ```php artisan key:generate```;
5. Execute o comando ```php artisan migrate```;
6. Inicie o projeto através do comando ```php artisan serve```.

### Criando nova branch para desenvolvimento

1. Verifique a sua branch atual utilizando o comando ```git branch```;
2. Na branch main, use o comando  ```git checkout -b <nome_da_branch/#numero_da_issue_aberta>```.
<br> **Exemplo**: ```git checkout -b anotso/#1``` <br>
3. Use o comando ```git checkout main```; 
4. Na branch main, execute o ```git pull origin main``` **antes de iniciar o desenvolvimento de qualquer nova atividade**.
> Caso não exista issue aberta no repositório do projeto é só cria-lá. Caso seja destinada para um outro integrante é só informar no grupo e passar a URL para a pessoa.

## Referências
- <a href="https://serverest.dev/#/">Exemplo 1</a>
- <a href="https://github.com/PauloGoncalvesBH/sample-supertest">Exemplo 2</a>

## Autores

<a href="https://github.com/Adassalifer">Adassa Jeanneffer Lima Ferreira</a><br>
<a href="https://github.com/AmandaBritoPereira">Amanda Brito Pereira</a><br>
<a href="https://github.com/christian-lelis">Christian De Lelis Santana Ferreira</a><br>
<a href="https://github.com/Claudemirdev">Claudemir Alexandre Silva De Vasconcelos</a><br>
<a href="https://github.com/DionisioFlavio">Flávio Oliveira Dionisio</a><br>
<a href="https://github.com/Floritcha">Flora Cristina De Souza Guijarro</a><br>
<a href="https://github.com/gabrielzom">Gabriel Sales Do Nascimento</a><br>
<a href="https://github.com/Anotso">Gracilliano Dos Anjos Carvalho</a><br>
<a href="https://github.com/manoellasouza/">Manoella Souza</a>







