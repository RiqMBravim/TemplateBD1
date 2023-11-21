# TRABALHO 01:  Título do Trabalho
Trabalho desenvolvido durante a disciplina de BD1

# Sumário

### 1. COMPONENTES<br>

Integrantes do grupo<br>
HenriqueMBravim@gmail.com
Cassiano.caporalis@gmail.com
gustavobilabbong@gmail.com

### 2.MINI-MUNDO<br>

A empresa Coda Fofo está criando um sistema para agendamento de consultas em Unidades Básicas de Saúde para alcançar uma maior produtividade dos funcionários e melhor atendimento aos pacientes. Para isso é necessário armazenar informações dos pacientes, sendo elas: Nome, RG, CPF, Data de Nascimento, Email, Telefone e dos Médicos Nome, RG, CPF, Data de Nascimento, Email, Telefone, Especialidade e CRM. Ambos médico e paciente devem possuir ao menos um Endereço contendo: estado, cidade, bairro, rua e logradouro. O paciente pode realizar vários agendamentos com vários médicos, porém apenas um agendamento por médico, o agendamento deve armazenar as seguintes informações: Data e Hora da Consulta, Nome do paciente, Nome do médico, quando o agendamento é efetivado cria-se uma consulta, a consulta está relacionado a um paciente e um médico, na consulta deve se conter as seguintes informações: Data e Hora da consulta, Nome do médico, Nome do paciente, Duração da consulta e Status (Concluída ou Faltosa).

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
 
![image](https://github.com/RiqMBravim/TemplateBD1/assets/116319569/dbaf16a3-d3ee-4ecc-a9cd-62a633823992)


#### 5.1 Validação do Modelo Conceitual

#### 5.2 Descrição dos dados 
    
    
	    PESSOA: Tabela que armazena as informações relativas aos Usuários:
	    	id: campo que armazena o número de identificação da tabela, chave primária.
	    	cpf: campo que armazena o número de Cadastro de Pessoa Física para cada pessoa.
	     	nome: campo que armazena o nome de cada pessoa.
		rg: campo que armazena o numero de Registro Geral de cada pessoa.
		datanascimento: campo que armazena a data de nascimento de cada pessoa.
	   CONTATO: Tabela que armazena os métodos de contato:
		id: campo que armazena o número de indentificação da tabela, chave primária
	 	email: campo que armazena o email de cada pessoa.
	  	telefone: campo que armazena o número de telefone de cada pessoa.
	   ENDERECO: Tabela que armazena o endereço de cada pessoa:
		id: campo que armazena o número de identificação da tabela, chave primária.
		estado: campo que armazena o estado em que o usuário reside.
		cidada: campo que armazena a cidade em que o usuário reside.
		bairro: campo que armazena o bairro em que o usuário reside.
		rua: campo que armazena a rua em que o usuário reside.
	    MEDICO: Tabela que armazena as informações relativas aos Medicos:
	    	id: Número de identificação da tabela, chave primária.
	     	crm_medico: campo que armazena o numero de registro do Conselho Regional de Medicina do medico.
	      	especialidade_medico: campo que armazena a especialidade do medico (se é pediatra, dermatologista, dentista etc...)
	    PACIENTE: Tabela que armazena as informações relativas aos Pacientes:
	    	id: campo que armazena o número de identificação da tabela, chave primaria.
	     	diagnostico_paciente: campo que armazena o diagnostico do paciente apos ter sido examinado na consulta.
	    AGENDAMENTO: Tabela que armazena as informações referentes ao agendamento das consultas:
	    	id: campo que armazena o número de identificação da tabela, chave primária
	     	datahoraconsulta_agendamento: campo que armazena a data e a hora em que a consulta será realizada.
	      	id_paciente: chave estrangeira da tabela Pessoa, serve para receber o nome do paciente que será consultado.
	       	id_medico: chave estrangeira da tabela Medico, serve para receber o nome do medico que fara a consulta.
	    CONSULTA: Tabela que armazena as informações referentes as consultas:
	    	id: campo que armazena o número de identificação da tabela, chave primária
	     	datahorainicio_consulta: campo que armazena a data e a hora de inicio da consulta.
	      	datahorafim_consulta: campo que armazena a data e a hora do fim da consulta.
	       	id_agendamento: chave estrangeira da tabela Agendamento, serve para receber o id do agendamento da respectiva consulta.
	 	status_consulta = campo que armazena o status da consulta (Concluida ou Faltosa).
    

># Marco de Entrega 01: Do item 1 até o item 5.2 (5 PTS) <br> 

### 6	MODELO LÓGICO<br>
        a) inclusão do esquema lógico do banco de dados
        b) verificação de correspondencia com o modelo conceitual
        (não serão aceitos modelos que não estejam em conformidade)

![image](https://github.com/RiqMBravim/TemplateBD1/assets/116319569/8d5811f1-4530-4516-b07f-65ddea1c4861)


### 7	MODELO FÍSICO<br>
        a) inclusão das instruções de criacão das estruturas em SQL/DDL
	
	CREATE TABLE IF NOT EXISTS PESSOA (
	  id SERIAL PRIMARY KEY NOT NULL,
	  rg_pessoa VARCHAR(255) UNIQUE NOT NULL,
	  cpf_pessoa VARCHAR(255) UNIQUE NOT NULL,
	  nome_pessoa VARCHAR(255) NOT NULL,
   	  sexo_pessoa VARCHAR(255) NOT NULL,
	  datanasc_pessoa DATE NOT NULL
	);
 
	CREATE TABLE IF NOT EXISTS CONTATO (
	  id SERIAL PRIMARY KEY NOT NULL,
	  email_contato VARCHAR(255),
	  telefone_contato VARCHAR(255),
	  fk_id_pessoa INTEGER NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id)
	);
	
	CREATE TABLE IF NOT EXISTS ENDERECO (
	  id SERIAL PRIMARY KEY NOT NULL,
	  estado_endereco VARCHAR(255) NOT NULL,
	  cidade_endereco varchar(255) NOT NULL,
	  bairro_endereco VARCHAR(255) NOT NULL,
	  rua_endereco VARCHAR(255) NOT NULL,
	  logradouro_endereco VARCHAR(255) NOT NULL,
	  fk_id_pessoa INTEGER NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id)
	);
	
	CREATE TABLE IF NOT EXISTS MEDICO (
	  id SERIAL PRIMARY KEY NOT NULL,
	  crm_medico VARCHAR(255) UNIQUE NOT NULL,
	  fk_id_pessoa INTEGER NOT NULL,
	  especialidade_medico VARCHAR(255) NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id)
	);
	
	CREATE TABLE IF NOT EXISTS PACIENTE (
	  id SERIAL PRIMARY KEY NOT NULL,
	  diagnostico_paciente VARCHAR(255) NOT NULL,
	  fk_id_pessoa INTEGER NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id)
	);
	
	CREATE TABLE IF NOT EXISTS AGENDAMENTO (
	  id SERIAL PRIMARY KEY NOT NULL,
	  fk_id_pessoa INTEGER NOT NULL,
	  fk_id_medico INTEGER NOT NULL,
	  datahoraagendamento_agendamento TIMESTAMP NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id),
	  CONSTRAINT fk_id_medico FOREIGN KEY (fk_id_medico) REFERENCES MEDICO(id)
	);
	
	CREATE TABLE IF NOT EXISTS CONSULTA (
	  id SERIAL PRIMARY KEY NOT NULL,
	  fk_id_agendamento INTEGER NOT NULL,
	  datahorainicio_consulta DATETIME,
	  datahorafim_consulta DATETIME,
	  status_consulta VARCHAR(255),
	  CONSTRAINT fk_id_agendamento FOREIGN KEY (fk_id_agendamento) REFERENCES AGENDAMENTO(id)
	);
      
### 8	INSERT APLICADO NAS TABELAS DO BANCO DE DADOS<br>
        a) Script das instruções relativas a inclusão de dados 
	Requisito mínimo: (Script dev conter: Drop para exclusão de tabelas + create definição de para tabelas e estruturas de dados + insert para dados a serem inseridos)
        OBS
	1) Criar um novo banco de dados para testar a restauracao (em caso de falha na restauração o grupo não pontuará neste quesito)
        2) script deve ser incluso no template em um arquivo no formato .SQL

	drop table if exists CONSULTA;
	drop table if exists AGENDAMENTO;
	drop table if exists CONTATO;
	drop table if exists ENDERECO;
	drop table if exists PACIENTE;
	drop table if exists MEDICO;
	drop table if exists PESSOA;
	
	CREATE TABLE IF NOT EXISTS PESSOA (
	  id SERIAL PRIMARY KEY NOT NULL,
	  rg_pessoa VARCHAR(255) UNIQUE NOT NULL,
	  cpf_pessoa VARCHAR(255) UNIQUE NOT NULL,
	  nome_pessoa VARCHAR(255) NOT NULL,
   	  sexo_pessoa VARCHAR(255) NOT NULL,
	  datanasc_pessoa DATE NOT NULL
	);
	
	INSERT INTO PESSOA (rg_pessoa, cpf_pessoa, nome_pessoa, sexo_pessoa, datanasc_pessoa) VALUES
	('1234567', '12345678901', 'João Silva', 'M', '1990-01-01'),
	('2345678', '23456789012', 'Maria Oliveira', 'F', '1985-02-15'),
	('3456789', '34567890123', 'Carlos Pereira', 'M', '1992-05-20'),
	('4567890', '45678901234', 'Ana Santos', 'F', '1988-08-10'),
	('5678901', '56789012345', 'Rodrigo Souza', 'M', '1995-11-25'),
	('6789012', '67890123456', 'Juliana Lima', 'F', '1982-04-05'),
	('7890123', '78901234567', 'Lucas Mendes', 'M', '1991-07-30'),
	('8901234', '89012345678', 'Fernanda Costa', 'F', '1987-09-18'),
	('9012345', '90123456789', 'Rafael Oliveira', 'M', '1993-12-05'),
	('1122334', '11223344556', 'Aline Pereira', 'F', '1985-03-21'),
	('4455667', '44556677889', 'Gustavo Santos', 'M', '1990-06-14'),
	('7788990', '77889900112', 'Camila Lima', 'F', '1988-08-01'),
	('9988776', '99887766554', 'Pedro Souza', 'M', '1997-11-09'),
	('1122336', '11223344557', 'Luana Oliveira', 'F', '1983-04-22'),
	('4455669', '44556677890', 'Marcos Pereira', 'M', '1996-07-15'),
	('7788992', '77889900113', 'Amanda Costa', 'F', '1989-10-03'),
	('9988778', '99887766555', 'Vinícius Santos', 'M', '1994-01-18'),
	('1122338', '11223344558', 'Isabela Lima', 'F', '1981-05-29'),
	('4455671', '44556677891', 'Paulo Mendes', 'M', '1999-08-11'),
	('7788994', '77889900114', 'Larissa Oliveira', 'F', '1986-12-26'),
	('9988780', '99887766556', 'Luciana Costa', 'F', '1991-03-05'),
	('1122340', '11223344559', 'Roberto Souza', 'M', '1984-06-17'),
	('4455673', '44556677892', 'Eduarda Lima', 'F', '1992-09-01'),
	('7788996', '77889900115', 'Felipe Santos', 'M', '1987-11-07'),
	('9988782', '99887766557', 'Carolina Pereira', 'F', '1996-02-24'),
	('1122342', '11223344560', 'Thiago Oliveira', 'M', '1980-05-12'),
	('4455675', '44556677893', 'Julia Lima', 'F', '1993-08-06'),
	('7788998', '77889900116', 'Daniel Costa', 'M', '1988-10-28'),
	('9988784', '99887766558', 'Mariana Santos', 'F', '1995-01-21'),
	('1122344', '11223344561', 'Giovanni Souza', 'M', '1982-04-03'),
	('4455677', '44556677894', 'Patrícia Oliveira', 'F', '1997-07-18'),
	('7788100', '77889900117', 'Roberta Lima', 'F', '1989-09-14'),
	('9988786', '99887766559', 'Leonardo Costa', 'M', '1994-12-09'),
	('1122346', '11223344562', 'Vanessa Santos', 'F', '1986-01-26'),
	('4455679', '44556677895', 'Renato Pereira', 'M', '1991-04-11'),
	('7788102', '77889900118', 'Nathalia Oliveira', 'F', '1983-06-19'),
	('9988788', '99887766560', 'Alexandre Lima', 'M', '1990-09-04'),
	('1122348', '11223344563', 'Fernanda Souza', 'F', '1985-12-03'),
	('4455681', '44556677896', 'Diego Santos', 'M', '1992-02-15'),
	('7788104', '77889900119', 'Luiza Costa', 'F', '1988-05-28'),
	('9988790', '99887766561', 'Erick Oliveira', 'M', '1995-08-22'),
	('1122350', '11223344564', 'Leticia Lima', 'F', '1981-07-16'),
	('4455683', '44556677897', 'Ana Carolina', 'F', '1998-11-28'),
	('7788106', '77889900120', 'Lucas Oliveira', 'M', '1984-02-07'),
	('9988792', '99887766562', 'Isabel Pereira', 'F', '1992-05-02'),
	('1122352', '11223344565', 'Fábio Santos', 'M', '1989-08-17'),
	('4455685', '44556677898', 'Gabriela Lima', 'F', '1994-10-12'),
	('7788108', '77889900121', 'Ricardo Costa', 'M', '1987-01-26'),
	('9988794', '99887766563', 'Amanda Souza', 'F', '1996-04-11'),
	('1122354', '11223344566', 'Henrique Oliveira', 'M', '1983-07-21'),
	('4455687', '44556677899', 'Juliana Pereira', 'F', '1990-09-05');
	
	CREATE TABLE IF NOT EXISTS CONTATO (
	  id SERIAL PRIMARY KEY NOT NULL,
	  email_contato VARCHAR(255),
	  telefone_contato VARCHAR(255),
	  fk_id_pessoa INTEGER NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id)
	);
	
	INSERT INTO CONTATO (email_contato, telefone_contato, fk_id_pessoa) VALUES
	('joao.silva@email.com', '123456789', 1),
	('maria.oliveira@email.com', '234567890', 2),
	('carlos.pereira@email.com', '345678901', 3),
	('ana.santos@email.com', '456789012', 4),
	('rodrigo.souza@email.com', '567890123', 5),
	('juliana.lima@email.com', '678901234', 6),
	('lucas.mendes@email.com', '789012345', 7),
	('fernanda.costa@email.com', '890123456', 8),
	('rafael.oliveira@email.com', '901234567', 9),
	('aline.pereira@email.com', '112233445', 10),
	('gustavo.santos@email.com', '445566778', 11),
	('camila.lima@email.com', '778899001', 12),
	('pedro.souza@email.com', '998877665', 13),
	('luana.oliveira@email.com', '112233445', 14),
	('marcos.pereira@email.com', '445566778', 15),
	('amanda.costa@email.com', '778899001', 16),
	('vinicius.santos@email.com', '998877665', 17),
	('isabela.lima@email.com', '112233445', 18),
	('paulo.mendes@email.com', '445566778', 19),
	('larissa.oliveira@email.com', '778899001', 20),
	('luciana.costa@email.com', '998877665', 21),
	('roberto.souza@email.com', '112233445', 22),
	('eduarda.lima@email.com', '445566778', 23),
	('felipe.santos@email.com', '778899001', 24),
	('carolina.pereira@email.com', '998877665', 25),
	('thiago.oliveira@email.com', '112233445', 26),
	('julia.lima@email.com', '445566778', 27),
	('daniel.costa@email.com', '778899001', 28),
	('mariana.santos@email.com', '998877665', 29),
	('giovanni.souza@email.com', '112233445', 30),
	('patricia.oliveira@email.com', '445566778', 31),
	('roberta.lima@email.com', '778899001', 32),
	('leonardo.costa@email.com', '998877665', 33),
	('vanessa.santos@email.com', '112233445', 34),
	('renato.pereira@email.com', '445566778', 35),
	('nathalia.oliveira@email.com', '778899001', 36),
	('alexandre.lima@email.com', '998877665', 37),
	('fernanda.souza@email.com', '112233445', 38),
	('diego.santos@email.com', '445566778', 39),
	('luiza.costa@email.com', '778899001', 40),
	('erick.oliveira@email.com', '998877665', 41),
	('leticia.lima@email.com', '112233445', 42),
	('ana.carolina@email.com', '445566778', 43),
	('lucas.oliveira@email.com', '778899001', 44),
	('isabel.pereira@email.com', '998877665', 45),
	('fabio.santos@email.com', '112233445', 46),
	('gabriela.lima@email.com', '445566778', 47),
	('ricardo.costa@email.com', '778899001', 48),
	('amanda.souza@email.com', '998877665', 49),
	('henrique.oliveira@email.com', '112233445', 50);
	
	  
	CREATE TABLE IF NOT EXISTS ENDERECO (
	  id SERIAL PRIMARY KEY NOT NULL,
	  estado_endereco VARCHAR(255) NOT NULL,
	  cidade_endereco varchar(255) NOT NULL,
	  bairro_endereco VARCHAR(255) NOT NULL,
	  rua_endereco VARCHAR(255) NOT NULL,
	  logradouro_endereco VARCHAR(255) NOT NULL,
	  fk_id_pessoa INTEGER NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id)
	);
	
	INSERT INTO ENDERECO (estado_endereco, cidade_endereco, bairro_endereco, rua_endereco, logradouro_endereco, fk_id_pessoa) VALUES
	('SP', 'São Paulo', 'Centro', 'Rua A', 'Apartamento 101', 1),
	('RJ', 'Rio de Janeiro', 'Copacabana', 'Avenida B', 'Casa 102', 2),
	('MG', 'Belo Horizonte', 'Savassi', 'Rua C', 'Apartamento 103', 3),
	('RS', 'Porto Alegre', 'Moinhos de Vento', 'Avenida D', 'Casa 104', 4),
	('BA', 'Salvador', 'Barra', 'Rua E', 'Apartamento 105', 5),
	('PR', 'Curitiba', 'Batel', 'Avenida F', 'Casa 106', 6),
	('PE', 'Recife', 'Boa Viagem', 'Rua G', 'Apartamento 107', 7),
	('CE', 'Fortaleza', 'Aldeota', 'Avenida H', 'Casa 108', 8),
	('SC', 'Florianópolis', 'Centro', 'Rua I', 'Apartamento 109', 9),
	('GO', 'Goiânia', 'Setor Bueno', 'Avenida J', 'Casa 110', 10),
	('AM', 'Manaus', 'Centro', 'Rua K', 'Apartamento 111', 11),
	('PA', 'Belém', 'Batista Campos', 'Avenida L', 'Casa 112', 12),
	('ES', 'Vitória', 'Jardim da Penha', 'Rua M', 'Apartamento 113', 13),
	('PB', 'João Pessoa', 'Manaíra', 'Avenida N', 'Casa 114', 14),
	('MT', 'Cuiabá', 'Araés', 'Rua O', 'Apartamento 115', 15),
	('AL', 'Maceió', 'Ponta Verde', 'Avenida P', 'Casa 116', 16),
	('PI', 'Teresina', 'Centro', 'Rua Q', 'Apartamento 117', 17),
	('TO', 'Palmas', 'Plano Diretor Sul', 'Avenida R', 'Casa 118', 18),
	('RN', 'Natal', 'Ponta Negra', 'Rua S', 'Apartamento 119', 19),
	('MA', 'São Luís', 'Calhau', 'Avenida T', 'Casa 120', 20),
	('MS', 'Campo Grande', 'Centro', 'Rua U', 'Apartamento 121', 21),
	('SE', 'Aracaju', 'Jardins', 'Avenida V', 'Casa 122', 22),
	('RO', 'Porto Velho', 'Centro', 'Rua W', 'Apartamento 123', 23),
	('AC', 'Rio Branco', 'Bosque', 'Avenida X', 'Casa 124', 24),
	('RR', 'Boa Vista', 'Centro', 'Rua Y', 'Apartamento 125', 25),
	('AP', 'Macapá', 'Central', 'Avenida Z', 'Casa 126', 26),
	('PI', 'Teresina', 'Centro', 'Rua AA', 'Apartamento 127', 27),
	('TO', 'Palmas', 'Plano Diretor Sul', 'Avenida BB', 'Casa 128', 28),
	('RN', 'Natal', 'Ponta Negra', 'Rua CC', 'Apartamento 129', 29),
	('MA', 'São Luís', 'Calhau', 'Avenida DD', 'Casa 130', 30),
	('MS', 'Campo Grande', 'Centro', 'Rua EE', 'Apartamento 131', 31),
	('SE', 'Aracaju', 'Jardins', 'Avenida FF', 'Casa 132', 32),
	('RO', 'Porto Velho', 'Centro', 'Rua GG', 'Apartamento 133', 33),
	('AC', 'Rio Branco', 'Bosque', 'Avenida HH', 'Casa 134', 34),
	('RR', 'Boa Vista', 'Centro', 'Rua II', 'Apartamento 135', 35),
	('AP', 'Macapá', 'Central', 'Avenida JJ', 'Casa 136', 36),
	('PI', 'Teresina', 'Centro', 'Rua KK', 'Apartamento 137', 37),
	('TO', 'Palmas', 'Plano Diretor Sul', 'Avenida LL', 'Casa 138', 38),
	('RN', 'Natal', 'Ponta Negra', 'Rua MM', 'Apartamento 139', 39),
	('MA', 'São Luís', 'Calhau', 'Avenida NN', 'Casa 140', 40),
	('MS', 'Campo Grande', 'Centro', 'Rua OO', 'Apartamento 141', 41),
	('SE', 'Aracaju', 'Jardins', 'Avenida PP', 'Casa 142', 42),
	('RO', 'Porto Velho', 'Centro', 'Rua QQ', 'Apartamento 143', 43),
	('AC', 'Rio Branco', 'Bosque', 'Avenida RR', 'Casa 144', 44),
	('RR', 'Boa Vista', 'Centro', 'Rua SS', 'Apartamento 145', 45),
	('AP', 'Macapá', 'Central', 'Avenida TT', 'Casa 146', 46),
	('PI', 'Teresina', 'Centro', 'Rua UU', 'Apartamento 147', 47),
	('TO', 'Palmas', 'Plano Diretor Sul', 'Avenida VV', 'Casa 148', 48),
	('RN', 'Natal', 'Ponta Negra', 'Rua WW', 'Apartamento 149', 49),
	('MA', 'São Luís', 'Calhau', 'Avenida XX', 'Casa 150', 50);
	
	
	CREATE TABLE IF NOT EXISTS MEDICO (
	  id SERIAL PRIMARY KEY NOT NULL,
	  crm_medico VARCHAR(255) UNIQUE NOT NULL,
	  fk_id_pessoa INTEGER NOT NULL,
	  especialidade_medico VARCHAR(255) NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id)
	);
	
	INSERT INTO MEDICO (crm_medico, fk_id_pessoa, especialidade_medico) VALUES
	('12345/SP', 1, 'Clínico Geral'),
	('23456/RJ', 2, 'Dermatologista'),
	('34567/MG', 3, 'Cardiologista'),
	('45678/RS', 4, 'Ortopedista'),
	('56789/BA', 5, 'Ginecologista'),
	('67890/PR', 6, 'Neurologista'),
	('78901/PE', 7, 'Oftalmologista'),
	('89012/CE', 8, 'Pediatra'),
	('90123/SC', 9, 'Endocrinologista'),
	('11223/GO', 10, 'Psiquiatra'),
	('44556/AM', 11, 'Urologista'),
	('77889/PA', 12, 'Gastroenterologista'),
	('99887/ES', 13, 'Oncologista'),
	('11223/PB', 14, 'Radiologista'),
	('44556/MT', 15, 'Dentista'),
	('77889/AL', 16, 'Fisioterapeuta'),
	('99887/PI', 17, 'Nutricionista'),
	('11223/TO', 18, 'Psicólogo'),
	('44556/RN', 19, 'Otorrinolaringologista'),
	('77889/MA', 20, 'Pneumologista');
	
	
	
	CREATE TABLE IF NOT EXISTS PACIENTE (
	  id SERIAL PRIMARY KEY NOT NULL,
	  diagnostico_paciente VARCHAR(255) NOT NULL,
	  fk_id_pessoa INTEGER NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id)
	);
	
	INSERT INTO PACIENTE (diagnostico_paciente, fk_id_pessoa) VALUES
	('Febre alta', 21),
	('Dermatite', 22),
	('Pressão alta', 23),
	('Fratura no braço', 24),
	('Gravidez confirmada', 25),
	('Enxaqueca crônica', 26),
	('Problema de visão', 27),
	('Alergia alimentar', 28),
	('Diabetes tipo 2', 29),
	('Depressão', 30),
	('Infecção urinária', 31),
	('Problema gastrointestinal', 32),
	('Câncer de mama', 33),
	('Fratura na perna', 34),
	('Tratamento odontológico', 35),
	('Lesão no joelho', 36),
	('Controle de peso', 37),
	('Aconselhamento psicológico', 38),
	('Problema respiratório', 39),
	('Problema auditivo', 40),
	('Lesão no ombro', 41),
	('Reabilitação física', 42),
	('Distúrbio alimentar', 43),
	('Problema cardíaco', 44),
	('Acompanhamento nutricional', 45),
	('Alergia respiratória', 46),
	('Dor crônica nas costas', 47),
	('Problema renal', 48),
	('Tratamento psiquiátrico', 49),
	('Alergia cutânea', 50);
	
	CREATE TABLE IF NOT EXISTS AGENDAMENTO (
	  id SERIAL PRIMARY KEY NOT NULL,
	  fk_id_pessoa INTEGER NOT NULL,
	  fk_id_medico INTEGER NOT NULL,
	  datahoraagendamento_agendamento TIMESTAMP NOT NULL,
	  CONSTRAINT fk_id_pessoa FOREIGN KEY (fk_id_pessoa) REFERENCES PESSOA(id),
	  CONSTRAINT fk_id_medico FOREIGN KEY (fk_id_medico) REFERENCES MEDICO(id)
	);
	

	INSERT INTO AGENDAMENTO (fk_id_pessoa, fk_id_medico, datahoraagendamento_agendamento) VALUES
	(1, 1, '2023-11-17 09:00:00'),
	(2, 2, '2023-11-17 10:30:00'),
	(3, 3, '2023-11-17 12:00:00'),
	(4, 4, '2023-11-17 14:30:00'),
	(5, 5, '2023-11-17 16:00:00'),
	(6, 6, '2023-11-18 09:30:00'),
	(7, 7, '2023-11-18 11:00:00'),
	(8, 8, '2023-11-18 13:30:00'),
	(9, 9, '2023-11-18 15:00:00'),
	(10, 10, '2023-11-18 16:30:00'),
	(11, 11, '2023-11-19 10:00:00'),
	(12, 12, '2023-11-19 11:30:00'),
	(13, 13, '2023-11-19 13:00:00'),
	(14, 14, '2023-11-19 15:30:00'),
	(15, 15, '2023-11-19 17:00:00'),
	(16, 16, '2023-11-20 09:30:00'),
	(17, 17, '2023-11-20 11:00:00'),
	(18, 18, '2023-11-20 12:30:00'),
	(19, 19, '2023-11-20 14:00:00'),
	(20, 20, '2023-11-20 15:30:00'),
	(21, 1, '2023-11-21 09:00:00'),
	(22, 2, '2023-11-21 10:30:00'),
	(23, 3, '2023-11-21 12:00:00'),
	(24, 4, '2023-11-21 14:30:00'),
	(25, 5, '2023-11-21 16:00:00'),
	(26, 6, '2023-11-22 09:30:00'),
	(27, 7, '2023-11-22 11:00:00'),
	(28, 8, '2023-11-22 13:30:00'),
	(29, 9, '2023-11-22 15:00:00'),
	(30, 10, '2023-11-22 16:30:00');
	
	
	CREATE TABLE IF NOT EXISTS CONSULTA (
	  id SERIAL PRIMARY KEY NOT NULL,
	  fk_id_agendamento INTEGER NOT NULL,
	  datahorainicio_consulta TIMESTAMP,
	  datahorafim_consulta TIMESTAMP,
	  status_consulta VARCHAR(255),
	  CONSTRAINT fk_id_agendamento FOREIGN KEY (fk_id_agendamento) REFERENCES AGENDAMENTO(id)
	);
	
	INSERT INTO CONSULTA (fk_id_agendamento, datahorainicio_consulta, datahorafim_consulta, status_consulta) VALUES
	(1, '2023-11-17 09:00:00', '2023-11-17 09:45:00', 'realizada'),
	(2, '2023-11-17 10:30:00', '2023-11-17 11:15:00', 'realizada'),
	(3, '2023-11-17 12:00:00', '2023-11-17 12:45:00', 'realizada'),
	(4, '2023-11-17 14:30:00', '2023-11-17 15:15:00', 'realizada'),
	(5, '2023-11-17 16:00:00', '2023-11-17 16:45:00', 'realizada'),
	(6, '2023-11-18 09:30:00', '2023-11-18 10:15:00', 'realizada'),
	(7, '2023-11-18 11:00:00', '2023-11-18 11:45:00', 'realizada'),
	(8, '2023-11-18 13:30:00', '2023-11-18 14:15:00', 'realizada'),
	(9, '2023-11-18 15:00:00', '2023-11-18 15:45:00', 'realizada'),
	(10, '2023-11-18 16:30:00', '2023-11-18 17:15:00', 'realizada'),
	(11, '2023-11-19 10:00:00', '2023-11-19 10:45:00', 'realizada'),
	(12, '2023-11-19 11:30:00', '2023-11-19 12:15:00', 'realizada'),
	(13, '2023-11-19 13:00:00', '2023-11-19 13:45:00', 'realizada'),
	(14, '2023-11-19 15:30:00', '2023-11-19 16:15:00', 'realizada'),
	(15, '2023-11-19 17:00:00', '2023-11-19 17:45:00', 'realizada'),
	(16, '2023-11-20 09:30:00', '2023-11-20 10:15:00', 'realizada'),
	(17, '2023-11-20 11:00:00', '2023-11-20 11:45:00', 'realizada'),
	(18, '2023-11-20 12:30:00', '2023-11-20 13:15:00', 'realizada'),
	(19, '2023-11-20 14:00:00', '2023-11-20 14:45:00', 'realizada'),
	(20, '2023-11-20 15:30:00', '2023-11-20 16:15:00', 'realizada'),
	(21, '2023-11-21 09:00:00', '2023-11-21 09:45:00', 'realizada'),
	(22, '2023-11-21 10:30:00', NULL, 'faltosa'),
	(23, '2023-11-21 12:00:00', NULL, 'faltosa'),
	(24, '2023-11-21 14:30:00', NULL, 'faltosa'),
	(25, '2023-11-21 16:00:00', NULL, 'faltosa'),
	(26, '2023-11-22 09:30:00', NULL, 'faltosa'),
	(27, '2023-11-22 11:00:00', NULL, 'faltosa'),
	(28, '2023-11-22 13:30:00', NULL, 'faltosa'),
	(29, '2023-11-22 15:00:00', NULL, 'faltosa'),
	(30, '2023-11-22 16:30:00', NULL, 'faltosa');


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


