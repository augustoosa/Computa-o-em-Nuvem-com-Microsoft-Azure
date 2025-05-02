# 💻 Desafio de Projeto: Computação em Nuvem com Microsoft Azure

Este repositório foi criado como parte do desafio prático da plataforma DIO, com o objetivo de consolidar conhecimentos adquiridos sobre Computação em Nuvem, especialmente utilizando a plataforma **Microsoft Azure**. Aqui estão reunidos **resumos, anotações e dicas** para facilitar futuros estudos e implementações.

---

## 🎯 Objetivos do Repositório

- Praticar a criação e configuração de máquinas virtuais no Azure;
- Documentar os conceitos essenciais da computação em nuvem;
- Servir como material de apoio para revisões e novos projetos.

---

### ☁️ Benefícios da Computação em Nuvem

## 🔄 Escalabilidade
Permite aumentar a capacidade computacional conforme a demanda do seu negócio cresce, sem a necessidade de investimentos físicos adicionais.

## 📈 Elasticidade
Permite ajustar automaticamente os recursos da aplicação.  
Exemplo: configurar para que, se a CPU atingir 75% da capacidade, um novo servidor seja adicionado automaticamente. Se a carga diminuir, o recurso extra é desativado.

## ✅ Confiabilidade
Os serviços podem ser distribuídos globalmente e configurados com tolerância a falhas, garantindo resiliência e continuidade em caso de falhas regionais.

## 📊 Previsibilidade
Comportamento estável em termos de desempenho e custos. A previsibilidade orçamentária é um dos principais atrativos da nuvem.

## 🔐 Segurança
A plataforma de nuvem oferece ferramentas de segurança, mas a **responsabilidade pela implementação correta é do cliente**. Isso inclui criptografia, controle de acesso, firewall, etc.

## 🛡️ Governança
Gerenciamento de recursos baseado em políticas de negócios.  
Exemplo: restringir o acesso a serviços em determinadas regiões por questões legais ou operacionais.

## ⚙️ Gerenciabilidade
Recursos podem ser gerenciados de diversas formas:
- Portal do Azure (interface gráfica)
- Azure CLI
- PowerShell
- APIs (REST)
- Infraestrutura como Código (IaC), como ARM Templates ou Bicep

Essa flexibilidade permite automatizar e escalar operações com facilidade.

---

## ⏱️ Disponibilidade e SLA (Service Level Agreement)

# O que é SLA?
É um acordo que define o nível de disponibilidade garantido pelo provedor de nuvem. Ele determina o tempo máximo que um serviço pode ficar indisponível dentro de um período.

| SLA (%)     | Tempo máximo de inatividade (por semana) |
|-------------|-------------------------------------------|
| 99.00%      | ~1h 41min                                 |
| 99.90%      | ~10min                                    |
| 99.99%      | ~1min                                     |
| 99.999%     | ~6 segundos                               |

- Quanto maior o SLA, maior a garantia de uptime, mas **maior o custo**.
- Caso o SLA não seja cumprido, o provedor deve compensar o cliente, normalmente com **créditos de serviço**.

---

# 💡 Dicas Práticas

- Comece com o Portal do Azure para se familiarizar com os recursos.
- Em projetos maiores, prefira automações com CLI, PowerShell ou Bicep.
- Use **tags** nos recursos para facilitar a organização e o controle de custos.
- Habilite **monitoramento e alertas** para identificar gargalos ou problemas automaticamente.
- Configure **backup e recuperação** para aumentar a resiliência dos seus serviços.

---

# 🛠️ Tecnologias Utilizadas

- Microsoft Azure
- Azure CLI / PowerShell
- Portal do Azure

---

## 🧱 Como Criar uma Máquina Virtual Windows no Portal do Azure

1. **Acesse o Portal do Azure**: [https://portal.azure.com](https://portal.azure.com)

2. **Pesquise por "Máquinas Virtuais"** no menu de busca e clique em **"Criar" > "Máquina virtual"**.

3. **Preencha as Informações Básicas**:
   - Assinatura e grupo de recursos
   - Nome da VM
   - Região (ex: Brazil South)
   - Imagem: escolha "Windows 11" ou "Windows Server"
   - Tipo de autenticação: senha ou chave SSH

4. **Tamanho da VM**:
   - Selecione a configuração de hardware (CPU/RAM) ideal ou use a sugerida.

5. **Configuração de Disco**:
   - Use o disco padrão (geralmente SSD) ou escolha outro tipo.

6. **Rede**:
   - Deixe a configuração padrão (com IP público e porta RDP aberta) para facilitar o acesso remoto.

7. **Revisar + Criar**:
   - Revise todas as configurações e clique em **"Criar"**.

8. **Aguarde a Implantação** e depois clique em **"Ir para o recurso"** para visualizar e gerenciar sua VM.

9. **Conexão via RDP**:
   - Clique em **"Conectar" > "RDP"**, baixe o arquivo `.rdp`, abra-o e entre com as credenciais definidas.

📌 Fonte oficial: [Documentação Microsoft Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
