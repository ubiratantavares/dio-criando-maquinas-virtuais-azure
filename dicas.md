# 💡 Dicas e Anotações sobre o Uso de Máquinas Virtuais no Microsoft Azure

Este documento contém dicas úteis e informações complementares sobre a criação e utilização de máquinas virtuais no Azure, visando ajudar na tomada de decisões durante o processo de configuração.

## 🔁 Diferença entre Discos SSD e HDD

| Característica       | SSD (Solid State Drive)       | HDD (Hard Disk Drive)         |
|----------------------|-------------------------------|-------------------------------|
| Velocidade           | Muito mais rápida (menor tempo de leitura e escrita) | Mais lenta                    |
| Desempenho           | Ideal para aplicações que exigem performance (banco de dados, apps críticos) | Adequado para cargas leves ou arquivos |
| Durabilidade         | Sem partes móveis, mais resistente a falhas físicas | Partes mecânicas, mais suscetível a desgaste |
| Custo                | Mais caro por GB              | Mais barato por GB            |
| Indicado para        | Sistemas operacionais, apps com alta E/S | Armazenamento em massa, backups |

**Recomendação:** Use SSD para o disco do sistema e HDD como disco de dados secundário, se for necessário.

## 💻 Quando Usar Windows vs. Linux em VMs

| Situação/Objetivo                  | Recomendado |
|-----------------------------------|-------------|
| Aplicações .NET, ASP.NET          | **Windows** |
| Terminal com bash, ferramentas DevOps | **Linux**   |
| Servidor de banco de dados SQL Server | **Windows** |
| Servidor web com Apache, NGINX    | **Linux**   |
| Projetos com baixo custo          | **Linux**   |
| Interface gráfica (GUI) necessária | **Windows** |

**Observação:** Linux é mais leve e geralmente mais barato no Azure, enquanto Windows pode oferecer mais facilidade de uso para usuários não familiarizados com o terminal.

## 🔐 Como Acessar a VM Remotamente

### 👉 Para Máquinas Virtuais Windows

1. Verifique se a porta RDP (3389) está aberta nas regras de entrada.

2. No portal do Azure, selecione a VM e clique em **Conectar > RDP**.

3. Baixe o arquivo `.rdp` e abra com o aplicativo "Conexão de Área de Trabalho Remota" (Windows).

4. Insira o nome de usuário e senha definidos durante a criação.

### 👉 Para Máquinas Virtuais Linux

1. Verifique se a porta SSH (22) está aberta nas regras de entrada.

2. Use um terminal local e digite:

```bash
ssh nome_usuario@IP_da_VM
```

3. Se tiver configurado uma chave SSH, inclua o caminho:

```bash
ssh -i caminho_para_chave.pem nome_usuario@IP_da_VM
```

Dica de segurança: Evite deixar RDP ou SSH expostos diretamente à internet por muito tempo. Use IPs restritos ou implemente Jump Boxes/VPN.
