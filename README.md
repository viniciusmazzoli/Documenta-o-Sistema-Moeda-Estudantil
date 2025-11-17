# Documentação de Projeto - Sistema de Moeda Estudantil

Este documento apresenta a modelagem e os modelos de projeto para o **Sistema de Moeda Estudantil**, uma plataforma desenvolvida para **reconhecer e valorizar o mérito estudantil** por meio de uma moeda virtual. Esta moeda é distribuída por professores e utilizada por alunos para resgatar produtos e vantagens oferecidas por empresas parceiras.

## 1. Modelos de Usuário e Requisitos

O sistema define quatro atores principais: **Professor**, **Aluno**, **Empresa Parceira** e **Administrador**. Os requisitos foram detalhados através de **Casos de Uso** (UC-01: Enviar Moeda, UC-02: Resgatar Vantagem, UC-04: Validar Cupom, etc.) e **Contratos de Operação** que especificam as pré e pós-condições das interações críticas.

## 2. Modelos de Projeto

O projeto adota a arquitetura **MVC (Model-View-Controller)**, separando a lógica de negócio, a interface do usuário e o controle de fluxo.

*   **Componentes e Implantação:** O sistema é dividido em **Frontend** (React/TypeScript) e **Backend** (Node.js/Express), que interage com um **Banco de Dados PostgreSQL** e um **Serviço de E-mail** para notificações. O modelo de implantação sugere a alocação em servidores Web e de Banco de Dados separados.
*   **Diagrama de Classes:** O modelo estático do sistema, baseado no `schema.prisma`, define as classes principais como `User`, `Account`, `Transaction`, `Reward` (Vantagem) e `Redemption` (Resgate/Cupom).
*   **Comportamento:** O comportamento do sistema é ilustrado por **Diagramas de Sequência do Sistema (DSS)** para os principais Casos de Uso e um **Diagrama de Comunicação** que detalha a colaboração entre objetos para a transferência de moedas.
*   **Ciclo de Vida:** O **Diagrama de Estados** modela o ciclo de vida do objeto `Redemption` (Cupom), que transita entre os estados **GERADO**, **UTILIZADO** e **EXPIRADO**.

## 3. Modelos de Dados

O modelo de dados é representado pelo Diagrama de Classes, que reflete o esquema do banco de dados relacional. O mapeamento Objeto-Relacional é gerenciado pelo **Prisma ORM**, garantindo a persistência e integridade dos dados.

Em suma, a documentação fornece uma visão abrangente, desde os requisitos funcionais até a estrutura técnica e o comportamento do sistema, servindo como referência fundamental para o desenvolvimento e manutenção do **Sistema de Moeda Estudantil**.
