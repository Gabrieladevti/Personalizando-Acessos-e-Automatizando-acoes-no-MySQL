# Desafio - Personalizando Acessos e Automatizando Ações no MySQL

## Descrição do Projeto

Neste projeto, o objetivo é personalizar o banco de dados MySQL com a criação de **visões** (views) e **gatilhos** (triggers) para automatizar ações em diferentes cenários, além de definir permissões de acesso com base nos tipos de usuários. O projeto está dividido em duas partes:

### Parte 1 – Personalizando Acessos com Views

Nesta parte, serão criadas **visões** para atender a cenários específicos e permitir o acesso eficiente aos dados conforme as necessidades da organização.

#### Cenários e Visões Criadas:

1. **Número de empregados por departamento e localidade:**
   - A visão agrupará os empregados por departamento e localidade, permitindo uma visualização clara de quantos empregados existem em cada localidade e departamento.

   ```sql
   CREATE VIEW numero_empregados_departamento_localidade AS
   SELECT departamento, cidade, COUNT(*) AS total_empregados
   FROM empregados
   GROUP BY departamento, cidade;
