# Sistema Web de Gestão e Acompanhamento Clínico para Fisioterapia

## Sumário

1. [Introdução](#1-introdução)
   - 1.1. [Motivação](#11-motivação)
   - 1.2. [Problema](#12-problema)
   - 1.3. [Hipótese](#13-hipótese)
   - 1.4. [Objetivos](#14-objetivos)
     - 1.4.1. [Objetivo Geral](#141-objetivo-geral)
     - 1.4.2. [Objetivos Específicos](#142-objetivos-específicos)
   - 1.5. [Escopo do Projeto](#15-escopo-do-projeto)
     - 1.5.1. [MVP (Mínimo Produto Viável)](#151-mvp-mínimo-produto-viável)
     - 1.5.2. [Componentes Técnicos Utilizados](#152-componentes-técnicos-utilizados)
     - 1.5.3. [Possíveis Funcionalidades Futuras](#153-possíveis-funcionalidades-futuras)

---

## 1. Introdução

A prática da fisioterapia exige acompanhamento contínuo além do tempo de consultório. O resultado do tratamento depende do engajamento do paciente com os exercícios domiciliares e da capacidade do profissional em monitorar a progressão de forma estruturada. Os Sistemas de Informação desempenham papel estratégico ao conectar dados clínicos à rotina dos pacientes, o que permite um tratamento eficiente. O objetivo deste trabalho é propor a concepção de uma solução tecnológica para otimizar essa jornada.

### 1.1. Motivação

A idealização deste projeto origina-se na observação direta das necessidades e dificuldades diárias enfrentadas em uma clínica de fisioterapia administrada pela minha avó . Nota-se na prática que clínicas de pequeno porte dependem de registros em papel ou de softwares de gestão voltados quase exclusivamente à área financeira e de agendamento, o que negligencia o acompanhamento clínico (LAUDON e LAUDON, 2014)[^1]. Essa limitação tecnológica cria uma lacuna no cuidado: o fisioterapeuta perde a visibilidade sobre a adesão do paciente aos exercícios em casa e o paciente fica sem instruções fora da clínica.

A ineficiência organizacional afeta o tempo de recuperação e a retenção de pacientes. Portanto, este trabalho justifica-se pela necessidade de desenvolver uma ferramenta que transcenda o gerenciamento administrativo, com foco central na progressão clínica. A contribuição reside em fornecer uma plataforma que consolide o prontuário eletrônico com o acompanhamento ativo, para apoiar a tomada de decisão do fisioterapeuta no contexto real dessa organização familiar e de outras clínicas com perfil semelhante.

### 1.2. Problema

Como apoiar o acompanhamento contínuo e o engajamento de pacientes no contexto de clínicas de fisioterapia de pequeno porte por meio de um sistema web de gestão de prontuários e prescrição de exercícios?

### 1.3. Hipótese

Acredita-se que a adoção de um sistema web focado na jornada clínica, que integra o prontuário eletrônico à prescrição de exercícios, aumenta a adesão ao tratamento por parte dos pacientes e fornece dados estruturados para a tomada de decisão dos fisioterapeutas.

### 1.4. Objetivos

#### 1.4.1. Objetivo Geral

Desenvolver um sistema web para a gestão de prontuários, acompanhamento de progressão e prescrição de exercícios, aplicado no contexto de clínicas de fisioterapia de pequeno porte da região de Niterói (RJ).

#### 1.4.2. Objetivos Específicos

- Analisar os processos atuais de registro clínico, agendamento e acompanhamento domiciliar de pacientes em clínicas de fisioterapia.

- Modelar a arquitetura da informação e o banco de dados para suportar o gerenciamento de prontuários e rotinas de exercícios.

- Implementar um Mínimo Produto Viável (MVP) com módulos de agendamento, prontuário eletrônico e portal do paciente.

- Avaliar a usabilidade do sistema por meio de testes de interação com profissionais de fisioterapia.

### 1.5. Escopo do Projeto

#### 1.5.1. MVP (Mínimo Produto Viável)

O escopo inicial do MVP é restrito às funcionalidades da operação clínica direta:

- **Módulo do Profissional**: Gestão de agenda, criação de prontuários eletrônicos evolutivos e montagem de cartilhas de exercícios (com descrições e links de apoio).

- **Módulo do Paciente**: Área de acesso restrito para visualização dos exercícios prescritos, orientações gerais e acompanhamento da própria evolução clínica.

#### 1.5.2. Componentes Técnicos Utilizados

- **Arquitetura e Infraestrutura**: Adoção de um modelo de implantação híbrido. O sistema e o banco de dados serão hospedados e executados primariamente em um hardware na própria clínica (*on-premise*), garantindo controle total, baixa latência e operação independente da internet externa. Simultaneamente, existirá uma instância leve configurada em nuvem para atuar como contingência (*fallback*), assegurando a disponibilidade do serviço caso o hardware local sofra eventualidades técnicas.

- **Frontend**: JavaScript (React.js) para interfaces dinâmicas.

- **Backend**: Python (Django ou FastAPI) para a construção da API REST e manipulação de dados lógicos.

- **Banco de Dados**: Relacional (PostgreSQL ou MySQL) para garantia da integridade e segurança dos dados dos prontuários médicos.

#### 1.5.3. Possíveis Funcionalidades Futuras

Funcionalidades sugeridas para expansão futura do software:

- Integração com gateway de pagamentos e faturamento de consultas.

- Sistema automatizado de notificações via WhatsApp ou SMS (lembretes de consulta e exercícios).

- Gamificação da progressão do paciente (sistema de metas visuais por completarem os exercícios propostos).

---

[^1]: A falta de sistemas especializados e acessíveis em clínicas de pequeno porte é um gargalo comum no setor de saúde suplementar brasileiro, o que força profissionais a utilizarem planilhas genéricas.
