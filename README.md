sistema-agendamento-php

Projeto de sistema de agendamento em PHP utilizando programação orientada a objetos.

Sistema de Agendamento para Nail Designer
Descrição do Projeto

O Sistema de Agendamento é uma aplicação web desenvolvida em PHP com o objetivo de automatizar o controle de horários de uma profissional de nail designer.

A aplicação permite que clientes realizem agendamentos de forma simples, escolhendo serviço, data e horário disponíveis. Além disso, o sistema conta com um painel administrativo que permite o gerenciamento completo da agenda.

O projeto foi estruturado com base nos conceitos de Programação Orientada a Objetos, organização em camadas e integração com banco de dados MySQL.

Objetivo

Desenvolver uma aplicação prática aplicando conceitos fundamentais e intermediários de desenvolvimento web com PHP, incluindo:

Criação de classes
Uso de atributos e métodos
Conexão com banco de dados
Organização de código
Interface responsiva mobile-first

Tecnologias Utilizadas

PHP
MySQL
HTML5
CSS3
PDO
Git
GitHub

Estrutura do Projeto
sistema-agendamento/
│
├── index.php
│
├── config/
│   └── database.php
│
├── models/
│   └── Agendamento.php
│
├── controllers/
│   ├── AgendamentoController.php
│   └── processa.php
│
├── views/
│   └── admin.php
│
├── assets/
│   ├── css/
│   │   └── style.css
│   └── images/
│
└── manifest.json
Banco de Dados

O sistema utiliza o banco de dados:

nail_agendamento

Tabela agendamentos:

Campo	Tipo
id	INT
nome_cliente	VARCHAR
servico	VARCHAR
data	DATE
horario	TIME
criado_em	TIMESTAMP
Funcionalidades do Sistema

Cadastro de agendamentos
Validação de horários disponíveis
Listagem de agendamentos
Exclusão de registros
Interface responsiva

Interface e Experiência do Usuário

O layout foi desenvolvido com abordagem mobile-first, inspirado em interfaces modernas.

Design limpo
Cores suaves
Botões acessíveis
Navegação simples

Como Executar o Projeto
Instalar um servidor local como XAMPP ou WAMP
Criar o banco de dados nail_agendamento no MySQL
Criar a tabela conforme especificado
Configurar o arquivo config/database.php
Colocar o projeto na pasta htdocs
Acessar no navegador

http://localhost/sistema-agendamento

Diagrama UML

Classe Agendamento

+----------------------+
|     Agendamento      |
+----------------------+
| nome_cliente         |
| servico              |
| data                 |
| horario              |
+----------------------+
| salvar()             |
| listar()             |
| verificarDisponibilidade() |
| deletar()            |
+----------------------+

Classe AgendamentoController

+----------------------------+
|  AgendamentoController     |
+----------------------------+
| agendamento                |
+----------------------------+
| criar()                    |
| deletar()                  |
+----------------------------+

Relação entre classes

AgendamentoController -> Agendamento
Melhorias Futuras

Dashboard com métricas
Sistema de pagamento
Multiusuários
Notificações em tempo real
Versão PWA

Autor

Alan Victor

Projeto desenvolvido para fins educacionais e prática em desenvolvimento web com PHP.
