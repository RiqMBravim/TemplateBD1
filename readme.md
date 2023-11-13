# TRABALHO 01:  Título do Trabalho
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>

Integrantes do grupo<br>
HenriqueMBravim@gmail.com
Cassiano.caporalis@gmail.com
gustavobilabbong@gmail.com

### 2.MINI-MUNDO<br>

A empresa Coda Fofo está criando um sistema para agendamento de consultas em Unidades Básicas de Saúde para alcançar uma maior produtividade dos funcionários e melhor atendimento aos pacientes. Para isso é necessário armazenar informações dos pacientes, sendo elas: Nome, RG, CPF, Data de Nascimento, Email, Telefone e dos Médicos Nome, RG, CPF, Data de Nascimento, Email, Telefone, Especialidade e CRM. Ambos médico e paciente devem possuir ao menos um Endereço contendo: estado, cidade, bairro, rua e logradouro. O paciente pode realizar vários agendamentos com vários médicos, porém apenas um agendamento por médico, o agendamento deve armazenar as seguintes informações: Data e Hora da Consulta, Nome do paciente, Nome do médico, quando o agendamento é efetivado cria-se uma consulta, a consulta está relacionado a um paciente e um médico, na consulta deve se conter as seguintes informações: Data e Hora da consulta, Nome do médico, Nome do paciente, Diagnóstico, Duração da consulta e Status (Concluída ou Faltosa).

### 3.PERGUNTAS A SEREM RESPONDIDAS<br>
#### 3.1 QUAIS PERGUNTAS PODEM SER RESPONDIDAS COM O SISTEMA PROPOSTO?
    a) O sistema proposto poderá fornecer quais tipos de relatórios e informaçes?
    
	Informação de registro dos Médicos, como: Nome, CRM, Especialidade, Email, Telefone.
 	Informações de registro dos Pacientes, como: Nome, Telefone, Email, Idade, Endereço, Diagnostico.
  	Informações sobre a Consulta, como: dados do médico e do paciente envolvidos, data da consulta, hora de inicio e do fim e observações

    b) Crie uma lista com os 5 principais relatórios que poderão ser obtidos por meio do sistema proposto!

	Relatório com a hora trabalhada de cada médico
 	Relatório com a hora de trabalho média de cada especialidade
  	Relatório da idade média de cada diagnostico
   	Relatório de taxa de cancelamento de consulta
    	Relatório de atraso de inicio e fim de consulta de cada médico
    
### 5.MODELO CONCEITUAL<br>
    A) Utilizar a Notação adequada (Preferencialmente utilizar o BR Modelo 3)
    B) O mínimo de entidades do modelo conceitual pare este trabalho será igual a 3 e o Máximo 5.
        * informe quais são as 3 principais entidades do sistema em densenvolvimento<br>(se houverem mais de 3 entidades, pense na importância da entidade para o sistema)
    C) Principais fluxos de informação/entidades do sistema (mínimo 3). <br>Dica: normalmente estes fluxos estão associados as tabelas que conterão maior quantidade de dados 
    D) Qualidade e Clareza
        Garantir que a semântica dos atributos seja clara no esquema (nomes coerentes com os dados).
        Criar o esquema de forma a garantir a redução de informação redundante, possibilidade de valores null, 
        e tuplas falsas (Aplicar os conceitos de normalização abordados).   

	3 principais entidades: Medico, Paciente e Consulta
 
![image](https://github.com/RiqMBravim/TemplateBD1/assets/111908300/b3424cc4-ffdf-4507-b58b-ac65c2f72708)

#### 5.1 Validação do Modelo Conceitual

#### 5.2 Descrição dos dados 
    
    Pessoa: Tabela que armazena as informações relativas aos Pacientes e Medicos<br>
    	Id: campo que armazena o número de identificação da tabela, chave primária
    	CPF: campo que armazena o número de Cadastro de Pessoa Física para cada pessoa.<br>
     	Nome: campo que armazena o nome de cada pessoa.
      	RG: campo que armazena o numero de Registro Geral de cada pessoa.
       	CEP: campo que armazena o Código de Endereçamento Postal de cada pessoa.
		Datanascimento: campo que armazena a data de nascimento de cada pessoa.
 		email: campo que armazena o email de cada pessoa.
  		telefone: campo que armazena o número de telefone de cada pessoa.
   		endereco: campo que armazena o endereço de cada pessoa (estado, cidade, bairro, rua e logradouro)
    Medico: Tabela que armazena as informações relativas aos Medicos.
    	Id: Número de identificação da tabela, chave primária.
     	crm_medico: campo que armazena o numero de registro do Conselho Regional de Medicina do medico.
      	especialidade_medico: campo que armazena a especialidade do medico (se é pediatra, dermatologista, dentista etc...)
    Paciente: Tabela que armazena as informações relativas aos Pacientes.
    	Id: campo que armazena o número de identificação da tabela, chave primaria.
     	diagnostico_paciente: campo que armazena o diagnostico do paciente apos ter sido examinado na consulta.
    Agendamento: Tabela que armazena as informações referentes ao agendamento das consultas.
    	Id: campo que armazena o número de identificação da tabela, chave primária
     	datahoraconsulta_agendamento: campo que armazena a data e a hora em que a consulta será realizada.
      	fk_nome_paciente: chave estrangeira da tabela Pessoa, serve para receber o nome do paciente que será consultado.
       	fk_nome_medico: chave estrangeira da tabela Medico, serve para receber o nome do medico que fara a consulta.
    Consulta: Tabela que armazena as informações referentes as consultas.
    	Id: campo que armazena o número de identificação da tabela, chave primária
     	datahorainicio_consulta: campo que armazena a data e a hora de inicio da consulta.
      	datahorafim_consulta: campo que armazena a data e a hora do fim da consulta.
       	fk_nome_medico: chave estrangeira da tabela Medico, serve para receber o nome do medico que fez a consulta.
		fk_nome_pessoa: chave estrangeira da tabela Pessoa, serve para receber o nome da pessoa que foi consultada.
 		diagnostico_consulta = campo que armazena o diagnostico emitido pelo Medico do paciente.
    

># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual
        (não serão aceitos modelos que não estejam em conformidade)

![image](https://github.com/RiqMBravim/TemplateBD1/assets/111908300/e8b1e7f4-a7aa-4212-ba21-9a3ebe296637)


### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL
        (criação de tabelas, alterações, etc..)

      
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) Script das instruções relativas a inclusão de dados 
	Requisito mínimo: (Script dev conter: Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        OBS
	1) Criar um novo banco de dados para testar a restauracao (em caso de falha na restauração o grupo não pontuará neste quesito)
        2) script deve ser incluso no template em um arquivo no formato .SQL


### 9	TABELAS E PRINCIPAIS CONSULTAS<br>
    OBS: Usa template da disciplina disponibilizado no Colab.<br>
#### 9.1	CONSULTAS DAS TABELAS COM TODOS OS DADOS INSERIDOS (Todas) <br>

#### 9.2	CONSULTAS DAS TABELAS COM FILTROS WHERE (Mínimo 4)<br>

#### 9.3	CONSULTAS QUE USAM OPERADORES LÓGICOS, ARITMÉTICOS E TABELAS OU CAMPOS RENOMEADOS (Mínimo 11)
    a) Criar 5 consultas que envolvam os operadores lógicos AND, OR e Not
    b) Criar no mínimo 3 consultas com operadores aritméticos 
    c) Criar no mínimo 3 consultas com operação de renomear nomes de campos ou tabelas

#### 9.4	CONSULTAS QUE USAM OPERADORES LIKE E DATAS (Mínimo 12) <br>
    a) Criar outras 5 consultas que envolvam like ou ilike
    b) Criar uma consulta para cada tipo de função data apresentada.

># Marco de Entrega 02: Do item 6. até o item 9.1 (5 PTS) <br>

#### 9.5	INSTRUÇÕES APLICANDO ATUALIZAÇÃO E EXCLUSÃO DE DADOS (Mínimo 6)<br>
    a) Criar minimo 3 de exclusão
    b) Criar minimo 3 de atualização

#### 9.6	CONSULTAS COM INNER JOIN E ORDER BY (Mínimo 6)<br>
    a) Uma junção que envolva todas as tabelas possuindo no mínimo 2 registros no resultado
    b) Outras junções que o grupo considere como sendo as de principal importância para o trabalho

#### 9.7	CONSULTAS COM GROUP BY E FUNÇÕES DE AGRUPAMENTO (Mínimo 6)<br>
    a) Criar minimo 2 envolvendo algum tipo de junção

#### 9.8	CONSULTAS COM LEFT, RIGHT E FULL JOIN (Mínimo 4)<br>
    a) Criar minimo 1 de cada tipo

#### 9.9	CONSULTAS COM SELF JOIN E VIEW (Mínimo 6)<br>
        a) Uma junção que envolva Self Join (caso não ocorra na base justificar e substituir por uma view)
        b) Outras junções com views que o grupo considere como sendo de relevante importância para o trabalho

#### 9.10	SUBCONSULTAS (Mínimo 4)<br>
     a) Criar minimo 1 envolvendo GROUP BY
     b) Criar minimo 1 envolvendo algum tipo de junção

># Marco de Entrega 03: Do item 9.2 até o ítem 9.10 (10 PTS)<br>

### 10 RELATÓRIOS E GRÁFICOS

#### a) análises e resultados provenientes do banco de dados desenvolvido (usar modelo disponível)
#### b) link com exemplo de relatórios será disponiblizado pelo professor no AVA
#### OBS: Esta é uma atividade de grande relevância no contexto do trabalho. Mantenha o foco nos 5 principais relatórios/resultados visando obter o melhor resultado possível.

    

### 11	AJUSTES DA DOCUMENTAÇÃO, CRIAÇÃO DOS SLIDES E VÍDEO PARA APRESENTAÇAO FINAL <br>

#### a) Modelo (pecha kucha)<br>
#### b) Tempo de apresentação 6:40 

># Marco de Entrega 04: Itens 10 e 11 (20 PTS) <br>
<br>
<br>




### 12 FORMATACAO NO GIT:<br> 
https://help.github.com/articles/basic-writing-and-formatting-syntax/
<comentario no git>
    
##### About Formatting
    https://help.github.com/articles/about-writing-and-formatting-on-github/
    
##### Basic Formatting in Git
    
    https://help.github.com/articles/basic-writing-and-formatting-syntax/#referencing-issues-and-pull-requests
    
    
##### Working with advanced formatting
    https://help.github.com/articles/working-with-advanced-formatting/
#### Mastering Markdown
    https://guides.github.com/features/mastering-markdown/

    
### OBSERVAÇÕES IMPORTANTES

#### Todos os arquivos que fazem parte do projeto (Imagens, pdfs, arquivos fonte, etc..), devem estar presentes no GIT. Os arquivos do projeto vigente não devem ser armazenados em quaisquer outras plataformas.
1. <strong>Caso existam arquivos com conteúdos sigilosos<strong>, comunicar o professor que definirá em conjunto com o grupo a melhor forma de armazenamento do arquivo.

#### Todos os grupos deverão fazer Fork deste repositório e dar permissões administrativas ao usuário do git "profmoisesomena", para acompanhamento do trabalho.

#### Os usuários criados no GIT devem possuir o nome de identificação do aluno (não serão aceitos nomes como Eu123, meuprojeto, pro456, etc). Em caso de dúvida comunicar o professor.


Link para BrModelo:<br>
http://www.sis4.com/brModelo/download.html
<br>


Link para curso de GIT<br>
![https://www.youtube.com/curso_git](https://www.youtube.com/playlist?list=PLo7sFyCeiGUdIyEmHdfbuD2eR4XPDqnN2?raw=true "Title")


