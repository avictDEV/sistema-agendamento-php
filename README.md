Sistema de Agendamento PHP

Este é um sistema de agendamento robusto desenvolvido em PHP, focado em fornecer organização e gestão de horários para profissionais autônomos.
Visão Geral

O Sistema de Agendamento é uma aplicação web estratégica projetada para simplificar o controle de atividades de profissionais que buscam eficiência. A solução centraliza o cadastro, visualização e gestão de atendimentos, eliminando conflitos de horários e otimizando a agenda.

O projeto foi construído seguindo rigorosas boas práticas de desenvolvimento, utilizando Programação Orientada a Objetos (POO) e o princípio de Separação de Responsabilidades.
O Problema

Muitos profissionais autônomos gerenciam suas agendas manualmente, o que resulta em:

    Falta de organização crônica.

    Sobreposição e conflitos de horários.

    Dificuldade em visualizar a disponibilidade a longo prazo.

    Experiência negativa para o cliente e perda de faturamento.

A Solução

Esta aplicação resolve esses gargalos oferecendo:

    Gestão Estruturada: Cadastro intuitivo de cada agendamento.

    Inteligência de Dados: Validação automática de horários para evitar duplicidade.

    Visibilidade: Listagem clara de atendimentos organizados por data e hora.

    Acessibilidade: Interface responsiva e moderna.

Funcionalidades

    Cadastro dinâmico de agendamentos.

    Validação em tempo real de horários ocupados.

    Listagem completa de registros salvos no banco de dados.

    Exclusão simplificada de registros.

    Design Responsivo (Mobile-First).

Tecnologias Utilizadas

    Linguagem: PHP 8+

    Banco de Dados: MySQL

    Conectividade: PDO (PHP Data Objects)

    Frontend: HTML5, CSS3

    Versionamento: Git e GitHub

Arquitetura do Projeto

O sistema segue o padrão MVC (Model-View-Controller) simplificado para garantir escalabilidade:

    Model: Gerencia a comunicação direta e lógica com o banco de dados.

    Controller: Processa as requisições do usuário e dita o fluxo da aplicação.

    View: Interface final que interage com o usuário.

Estrutura de Pastas
Plaintext

sistema-agendamento/
│
├── index.php                # Ponto de entrada da aplicação
├── config/
│   └── database.php         # Configuração de conexão PDO
├── models/
│   └── Agendamento.php      # Lógica de negócio e CRUD
├── controllers/
│   ├── AgendamentoController.php
│   └── processa.php         # Intermediário de requisições
├── views/
│   └── admin.php            # Painel administrativo
├── assets/
│   ├── css/
│   │   └── style.css
│   └── images/
└── manifest.json            # Metadados da aplicação

Banco de Dados

Banco: nail_agendamento
Tabela: agendamentos
Campo	Tipo	Descrição
id	INT (PK)	Identificador único
nome_cliente	VARCHAR	Nome do cliente
servico	VARCHAR	Tipo de serviço prestado
data	DATE	Data do atendimento
horario	TIME	Hora do atendimento
criado_em	DATETIME	Registro de criação
Diagrama UML
Snippet de código

classDiagram
    class Agendamento {
        +String nome_cliente
        +String servico
        +Date data
        +Time horario
        +salvar()
        +listar()
        +verificarDisponibilidade()
        +deletar()
    }

    class AgendamentoController {
        +Agendamento agendamento
        +criar()
        +deletar()
    }

    AgendamentoController --> Agendamento : Gerencia

Como Executar o Projeto

    Certifique-se de ter um ambiente como XAMPP ou WAMP instalado.

    Crie o banco de dados nail_agendamento e execute o script SQL da tabela agendamentos.

    Configure as credenciais de acesso no arquivo config/database.php.

    Mova a pasta do projeto para o diretório htdocs (no caso do XAMPP).

    Acesse no seu navegador: http://localhost/sistema-agendamento.

Melhorias Futuras

    Dashboard estatístico com métricas de atendimentos.

    Integração com gateways de pagamento.

    Sistema de login multiusuário para diferentes profissionais.

    Notificações automáticas via WhatsApp ou E-mail.

    Suporte completo a PWA (Progressive Web App).

Autor: Alan Victor
Projeto desenvolvido com foco em excelência técnica e organização de sistemas em PHP.
