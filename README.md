sistema-agendamento-php

Sistema de agendamento desenvolvido em PHP com foco em organização de horários para profissionais autônomos.

Visão Geral

O sistema de agendamento é uma aplicação web desenvolvida para facilitar o controle de horários de uma profissional de nail designer.

A solução permite o cadastro, visualização e gerenciamento de agendamentos, garantindo organização da agenda e evitando conflitos de horários.

O projeto foi construído com base em boas práticas de desenvolvimento, utilizando Programação Orientada a Objetos e separação de responsabilidades.

Problema

Profissionais autônomos frequentemente realizam agendamentos manualmente, o que pode gerar:

Falta de organização
Conflito de horários
Dificuldade de controle da agenda
Perda de clientes

Solução

A aplicação resolve esse problema oferecendo:

Cadastro estruturado de agendamentos
Validação de horários disponíveis
Visualização organizada dos atendimentos
Interface simples e responsiva

Funcionalidades

Cadastro de agendamentos
Validação de horários duplicados
Listagem de agendamentos
Exclusão de registros
Interface responsiva para dispositivos móveis

Tecnologias Utilizadas

PHP
MySQL
HTML5
CSS3
PDO
Git e GitHub

Arquitetura do Projeto

O sistema segue uma organização baseada no padrão MVC simplificado:

Model
Responsável pela comunicação com o banco de dados

Controller
Responsável pela lógica da aplicação

View
Responsável pela interface com o usuário

Estrutura de Pastas
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

Banco de dados utilizado: nail_agendamento

Tabela agendamentos:

id
nome_cliente
servico
data
horario
criado_em

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

Interface

O sistema foi desenvolvido com abordagem mobile-first, priorizando usabilidade em dispositivos móveis.

Layout simples
Foco em experiência do usuário
Navegação intuitiva

Como Executar o Projeto
Instalar XAMPP ou WAMP
Criar o banco de dados nail_agendamento
Criar a tabela agendamentos
Configurar o arquivo config/database.php
Colocar o projeto na pasta htdocs
Acessar no navegador

http://localhost/sistema-agendamento

Melhorias Futuras

Dashboard com métricas
Sistema de pagamento
Multiusuários
Notificações automatizadas
Versão PWA

Autor

Alan Victor

Projeto desenvolvido com foco em prática de desenvolvimento web e organização de sistemas em PHP.
