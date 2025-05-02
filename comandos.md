# 🧾 Comandos Úteis com Azure CLI

Este documento apresenta exemplos práticos de comandos com o **Azure CLI** para gerenciar recursos no Microsoft Azure de forma automatizada pelo terminal.

> ✅ Antes de executar os comandos, certifique-se de:

> - Ter o [Azure CLI](https://learn.microsoft.com/pt-br/cli/azure/install-azure-cli) instalado.

> - Estar autenticado com `az login`.

> - Ter selecionado a assinatura correta com `az account set`.

## 📦 Criar uma Máquina Virtual com Azure CLI

### 1. Criar um Grupo de Recursos

```bash
az group create --name MeuGrupoRecursos --location brazilsouth
```

### 2. Criar a Máquina Virtual

```bash
az vm create \
  --resource-group MeuGrupoRecursos \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys \
  --location brazilsouth
```

> Este comando:

> - Cria uma VM com Ubuntu Linux

> - Gera automaticamente chaves SSH

> - Usa o nome de usuário `azureuser`


## 📋 Listar Recursos

### 1. Listar todos os grupos de recursos

```bash
az group list --output table
```

### 2. Listar todas as máquinas virtuais

```bash
az vm list --output table
```

### 3. Ver detalhes de uma VM específica

```bash
az vm show --resource-group MeuGrupoRecursos --name MinhaVM --output json
```

## ❌ Deletar Recursos

### 1. Deletar uma VM específica

```bash
az vm delete --resource-group MeuGrupoRecursos --name MinhaVM --yes
```

### 2. Deletar um grupo de recursos completo (e todos os recursos dentro dele)

```bash
az group delete --name MeuGrupoRecursos --yes --no-wait
```

> ⚠️ Atenção: Esta ação é irreversível. Use com cuidado!

## 📚 Links úteis

- [Referência do Azure CLI - Virtual Machines](https://learn.microsoft.com/pt-br/cli/azure/vm)

- [Azure CLI Cheatsheet (em inglês)](https://learn.microsoft.com/en-us/cli/azure/cheatsheet)
