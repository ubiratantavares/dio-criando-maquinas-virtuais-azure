# Guia Prático: Como Criar uma Máquina Virtual no Microsoft Azure

Este repositório foi criado como parte de um laboratório prático para documentar o processo de criação de máquinas virtuais (VMs) no Microsoft Azure. Aqui você encontrará um passo a passo detalhado, dicas importantes e links úteis para aprofundar seus conhecimentos.

## 📌 Objetivos

- Praticar o processo de criação e configuração de uma VM no Azure.

- Documentar o processo de forma clara e reutilizável.

- Criar um material de apoio para futuros projetos com Azure.

## 🛠️ Pré-requisitos

- Conta Microsoft com acesso ao Azure (pode usar a conta gratuita).

- Acesso ao Portal do Azure via navegador.

- Conexão com a internet.

## 🧭 Passo a Passo

### 1. Acessar o Portal do Azure

- Vá para [https://portal.azure.com](https://portal.azure.com) e faça login com sua conta.

### 2. Criar uma Nova Máquina Virtual

- No painel de navegação à esquerda, clique em **"Máquinas Virtuais"**.

- Clique em **"Criar"** > **"Máquina Virtual"**.

### 3. Configurações Básicas

- **Assinatura**: Selecione a disponível.

- **Grupo de Recursos**: Crie um novo ou selecione um existente.

- **Nome da VM**: Ex: `vm-estudo-azure`

- **Região**: Escolha a mais próxima (ex: "Brazil South").

- **Imagem**: Selecione uma imagem como "Windows Server 2022" ou "Ubuntu 20.04".

- **Tamanho**: Use um tamanho gratuito se possível (Ex: B1s).

- **Usuário e senha**: Defina credenciais de acesso.

### 4. Regras de Porta de Entrada

- Ative a porta RDP (para Windows) ou SSH (para Linux), conforme o sistema escolhido.

### 5. Disco e Rede

- Use as opções padrão inicialmente.

- Crie ou use uma VNet existente e sub-rede.

### 6. Revisar e Criar

- Clique em **"Revisar + criar"**, aguarde a validação e clique em **"Criar"**.

## 🔗 Links Úteis

- [Criar VM Windows no Portal do Azure (MS Learn)](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)

## 💡 Dicas

- Use o Azure Cost Calculator para prever custos.

- Aproveite o crédito gratuito de novos usuários.

- Desligue ou exclua a VM após o uso para evitar cobranças.
