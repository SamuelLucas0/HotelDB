# Sistema de Gerenciamento de Hotel

Este projeto é um sistema de gerenciamento de hotel desenvolvido em Python com integração ao banco de dados MySQL. Ele oferece uma solução completa para realizar operações CRUD (Criar, Ler, Atualizar, Excluir) em clientes, quartos e reservas, além de gerar relatórios detalhados sobre a operação do hotel.

## 🎬 Vídeo de Demonstração

Assista a uma demonstração completa do sistema, apresentando as principais funcionalidades, desde cadastros até a geração de relatórios.

[Link para o vídeo de demonstração](https://youtu.be/Mjx05IhnHu4?feature=shared)

## ✨ Funcionalidades Principais

O sistema oferece um conjunto robusto de funcionalidades para uma gestão hoteleira eficiente:

### 👤 Gerenciamento de Clientes
- **Cadastrar:** Adicione novos clientes ao sistema.
- **Listar:** Visualize todos os clientes cadastrados.
- **Atualizar:** Modifique informações de clientes existentes.
- **Excluir:** Remova clientes e suas reservas associadas, se houver.

### 🚪 Gerenciamento de Quartos
- **Cadastrar:** Adicione novos quartos, especificando tipo, valor da diária e capacidade.
- **Listar:** Verifique todos os quartos e seu status (livre/ocupado).
- **Atualizar:** Altere dados de quartos que não estejam em uso.
- **Excluir:** Remova quartos do sistema e cancele as reservas vinculadas.

### 🏨 Gerenciamento de Reservas
- **Criar:** Efetue novas reservas, associando clientes a quartos disponíveis.
- **Listar:** Consulte todas as reservas ativas no sistema.
- **Atualizar:** Modifique os detalhes de uma reserva existente.
- **Excluir:** Cancele reservas e libere os quartos para novas locações.

### 📊 Relatórios Gerenciais
- **Relatório de Quartos:** Obtenha um panorama completo com total de quartos, ocupação e faturamento.
- **Relatório de Hóspedes:** Analise dados como a quantidade total de hóspedes, média de dias de locação e valor médio das reservas.

### 🖥️ Tela Inicial
- Um painel inicial que exibe informações sobre o projeto (autores, disciplina) e estatísticas do banco de dados, como o total de registros em cada tabela.

## 🛠️ Estrutura do Projeto

O código é modular e orientado a objetos para facilitar a manutenção e escalabilidade.

- `DatabaseConnection`: Gerencia a conexão com o banco de dados MySQL.
- `Cliente`: Métodos CRUD para a entidade de clientes.
- `Quarto`: Métodos CRUD para a entidade de quartos.
- `Reserva`: Métodos CRUD para a entidade de reservas.
- `Menus`: Funções para a interface de usuário no console.
- `main.py`: Ponto de entrada da aplicação.

## 🗃️ Estrutura do Banco de Dados

O sistema utiliza o banco de dados `BDB_hotel` com as seguintes tabelas:

1.  **CLIENTE**:
    - `CPF`, `TELEFONE`, `NOME`, `EMAIL`, `DATA_NASCIMENTO`, `CEP`
2.  **QUARTO**:
    - `NUM_QUARTO`, `TIPO_QUARTO`, `VALOR_DIARIA`, `LIMITE_PESSOAS`
3.  **RESERVA**:
    - `NUM_RESERVA`, `DATA_INICIO`, `DATA_FINAL`, `QUANTIDADE_PESSOAS`, `VALOR_RESERVA`, `CPF`, `NUM_QUARTO`, `CAFE_INCLUSO`

## 🚀 Como Executar o Projeto

Siga os passos abaixo para configurar e executar o sistema em seu ambiente local.

### Pré-requisitos
- Python 3.x
- Git
- MySQL Server

### 1. Configuração do Ambiente Virtual

É uma boa prática usar um ambiente virtual para isolar as dependências.

```bash
# Criar o ambiente virtual
python3 -m venv venv

# Ativar o ambiente virtual
# No Linux ou MacOS:
source venv/bin/activate
# No Windows:
venv\Scripts\activate
```

### 2. Instalação de Dependências

Com o ambiente virtual ativado, instale a biblioteca necessária:

```bash
pip install mysql-connector-python
```

### 3. Configuração do Banco de Dados

Acesse seu terminal MySQL para criar e configurar o banco de dados.

```sql
-- Acesse o MySQL (será solicitada a senha)
mysql -u root -p

-- Crie o banco de dados
CREATE DATABASE BDB_hotel;

-- Selecione o banco de dados para uso
USE BDB_hotel;
```

**Importante:** Não se esqueça de atualizar as credenciais de conexão no arquivo `DatabaseConnection.py` (ou onde a conexão é definida) com seu usuário, senha e nome do banco de dados.

### 4. Executando o Programa

Com tudo configurado, execute o arquivo principal para iniciar o sistema:

```bash
python3 main.py
```
