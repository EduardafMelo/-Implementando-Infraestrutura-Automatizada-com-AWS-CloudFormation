# -Implementando-Infraestrutura-Automatizada-com-AWS-CloudFormation

# ☁️ AWS CloudFormation — Infraestrutura como Código (IaC)
### 📚 Resumo elaborado por Maria Eduarda Melo  

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

🧾 *Exemplo simples de template:*
```yaml
Resources:
  MeuBucketS3:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: meu-bucket-exemplo

## 🪄 Explicando o Código

- **Resources:** define os recursos que serão criados.  
- **Type:** indica o tipo de recurso — aqui, um `AWS::S3::Bucket`.  
- **Properties:** define as configurações do recurso (nome, controle de acesso etc).  
- **Outputs:** retorna informações úteis após a criação da stack (ex: nome do bucket).  

---

## 💡 Vantagens do AWS CloudFormation

✅ **Automação completa:** cria e gerencia recursos sem intervenção manual.  
✅ **Consistência:** garante que todos os ambientes sigam o mesmo padrão.  
✅ **Versionamento:** templates podem ser salvos no GitHub e reaproveitados.  
✅ **Escalabilidade:** ideal para gerenciar grandes infraestruturas.  
✅ **Segurança:** reduz erros manuais de configuração.  
✅ **Integração:** funciona com IAM, EC2, Lambda, S3 e muitos outros serviços da AWS.  

---

## 🔁 Ciclo de Vida de uma Stack

- **🧩 Criação:** o template é enviado e os recursos são provisionados.  
- **🛠️ Atualização:** mudanças no template atualizam automaticamente os recursos existentes.  
- **🗑️ Exclusão:** remove todos os recursos criados pela stack.  

Durante todo o processo, o **CloudFormation exibe logs e eventos em tempo real**, permitindo acompanhar cada etapa.  

---

## 🧾 Boas Práticas

🔖 Use **nomes claros e padronizados** para os recursos.  
🧩 Utilize **Parameters** para tornar os templates reutilizáveis.  
🧾 **Valide o template** antes de criar a stack.  
💬 Adicione **Outputs** para retornar informações úteis.  
📁 Organize templates por ambiente (ex: `dev`, `test`, `prod`).  
💡 **Documente e versione** todas as alterações no GitHub.  

---

## ⚡ Dicas Extras

⚙️ Use **Change Sets** para visualizar o que vai mudar antes de aplicar alterações.  
☁️ Combine **CloudFormation com AWS CLI** para automações via terminal.  
🧱 Utilize **Stack Policies** para proteger recursos críticos contra exclusões acidentais.  
📦 Mantenha uma pasta `/templates` no repositório para guardar diferentes configurações.  

---

## 📚 Referências e Leitura Recomendada

- 📘 [Documentação Oficial do AWS CloudFormation](https://docs.aws.amazon.com/cloudformation/index.html)  
- 🧩 [Guia do Usuário CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)  
- 💻 [AWS CLI Reference](https://docs.aws.amazon.com/cli/latest/reference/)  
- 🏗️ [AWS Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/)  

---
