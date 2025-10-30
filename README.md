# -Implementando-Infraestrutura-Automatizada-com-AWS-CloudFormation
---

## 🌐 Introdução  
O **AWS CloudFormation** é um serviço da Amazon Web Services que permite **automatizar a criação e o gerenciamento de recursos de infraestrutura** na nuvem por meio de **código**.  
Em vez de configurar manualmente cada serviço, tudo é definido em **templates escritos em YAML ou JSON**, tornando o processo mais rápido, consistente e seguro.  

Essa prática é chamada de **Infraestrutura como Código (IaC)** — uma das abordagens mais modernas e importantes da computação em nuvem.

---

## 🧠 O que é Infraestrutura como Código (IaC)
A **Infraestrutura como Código** é a técnica de descrever toda a infraestrutura (servidores, redes, bancos de dados, permissões etc.) **em forma de código**.  
Isso traz várias vantagens:  

- 🚀 **Automação**: os ambientes são criados automaticamente, sem precisar configurar tudo manualmente;  
- 📦 **Padronização**: garante que todos os ambientes (teste, produção, desenvolvimento) fiquem iguais;  
- 🔁 **Reprodutibilidade**: o mesmo código pode ser executado várias vezes para recriar o mesmo ambiente;  
- 🧾 **Versionamento**: é possível salvar, comparar e reverter versões do código no GitHub.  

---

## ⚙️ Como o CloudFormation Funciona  

O CloudFormation funciona com dois elementos principais: **Templates** e **Stacks**.

### 🔹 Template  
É o **arquivo de código** que descreve toda a infraestrutura.  
Ele contém seções como:  

- **Parameters** → entradas configuráveis, como nomes ou tamanhos;  
- **Resources** → onde os serviços AWS são definidos (S3, EC2, VPC etc.);  
- **Outputs** → resultados ou informações retornadas, como o endpoint de um site;  
- **Mappings e Conditions** → para adaptar o template a diferentes cenários.  

