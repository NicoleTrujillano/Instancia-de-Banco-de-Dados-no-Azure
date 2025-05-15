# Documentação Técnica - Instância de Banco de Dados no Azure

Este repositório foi criado como parte do desafio proposto pela DIO para demonstrar o conhecimento adquirido sobre a configuração de uma instância de banco de dados na plataforma Microsoft Azure.

## Conteúdo Aprendido

### Tipos de Serviço de Nuvem

Durante as aulas, foram abordados três principais modelos de serviço em nuvem:

- **IaaS (Infrastructure as a Service)**  
  Modelo mais flexível, permitindo ao usuário gerenciar o sistema operacional, aplicações e configurações de rede. O provedor (Microsoft) é responsável pela infraestrutura física.

- **PaaS (Platform as a Service)**  
  Ideal para desenvolvedores que querem focar em aplicativos e dados sem se preocupar com infraestrutura. O controle da rede, aplicativos e identidade é parcialmente compartilhado.

- **SaaS (Software as a Service)**  
  Serviço completo entregue ao usuário final, como e-mail ou CRM. Toda a responsabilidade técnica fica com o provedor de nuvem.

---

## Modelo de Responsabilidade Compartilhada

Baseado na documentação oficial da Microsoft, a responsabilidade entre cliente e provedor varia conforme o tipo de serviço:

| Responsabilidade                            | SaaS       | PaaS         | IaaS         | No Local    |
|--------------------------------------------|------------|--------------|--------------|-------------|
| **Informações e dados**                    | Cliente    | Cliente      | Cliente      | Cliente     |
| **Dispositivos (móveis e PCs)**            | Cliente    | Cliente      | Cliente      | Cliente     |
| **Contas e identidades**                   | Cliente    | Cliente      | Cliente      | Cliente     |
| **Infraestrutura de identidade e diretório**| Compartilhada  | Compartilhada| Cliente| Cliente     |
| **Aplicativos**                            | Microsoft  | Compartilhada      | Cliente      | Cliente     |
| **Controles de rede**                      | Microsoft  | Compartilhada| Cliente      | Cliente     |
| **Sistema operacional**                    | Microsoft  | Microsoft    | Cliente      | Cliente     |
| **Hosts físicos**                          | Microsoft  | Microsoft    | Microsoft    | Cliente     |
| **Rede física**                            | Microsoft  | Microsoft    | Microsoft    | Cliente     |
| **Datacenter físico**                      | Microsoft  | Microsoft    | Microsoft    | Cliente     |

---

## Configuração da Instância SQL no Azure

### Etapas Realizadas

1. **Acesso ao Portal Azure**
   - Entrar com a conta Microsoft no [portal.azure.com](https://portal.azure.com/)

2. **Criação de um Recurso de Banco de Dados SQL**
   - Navegar até "Criar um recurso"
   - Selecionar **Banco de Dados SQL**
   - Inserir as informações:
     - Nome do banco
     - Grupo de recursos
     - Nome do servidor (e credenciais de administrador)

3. **Configuração do Servidor SQL**
   - Criar um servidor lógico (nome único, região, login e senha)
   - Configurar o firewall para permitir acessos externos (inserir IP local)

4. **Definição do Plano de Serviço**
   - Escolher o modelo de compra (DTU ou vCore)
   - Definir o tamanho da instância (por ex., Basic, Standard ou Premium)

5. **Finalização e Criação**
   - Revisar configurações
   - Clicar em “Criar” para provisionar a instância

6. **Conexão ao Banco**
   - Utilização do **Azure Data Studio** ou **SQL Server Management Studio (SSMS)**
   - Conectar via string de conexão usando login/senha definidos

---

## Como Utilizar

Este repositório serve como base para criar, configurar e documentar uma instância de Banco de Dados SQL na nuvem Azure, usando boas práticas técnicas e de segurança.
