# ☁️ Redução de Custos AWS na Abstergo Industries

Projeto prático desenvolvido para o desafio da **DIO (Digital Innovation One)**, focado em arquitetura Cloud e otimização financeira (FinOps) utilizando os pilares de eficiência da AWS.

---

## 📄 RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

**Data:** 13/03/2026  
**Empresa:** Abstergo Industries  
**Responsável:** Maike Simoncini da Silva  

### 1. Introdução
Este relatório apresenta o processo de implementação de ferramentas na empresa **Abstergo Industries**, realizado por **Maike Simoncini da Silva**. O objetivo principal foi identificar e aplicar 3 serviços AWS que proporcionassem uma diminuição de custos imediatos e maior eficiência operacional.

### 2. Descrição do Projeto
A estratégia de otimização foi dividida em três frentes técnicas:

#### Etapa 1: Computação de Baixo Custo (Spot Instances)
- **Ferramenta:** Amazon EC2 Spot Instances
- **Foco:** Economia em cargas de trabalho flexíveis.
- **Caso de Uso:** Uso de instâncias ociosas para ambientes de teste e processamento de dados, reduzindo custos em até 90% comparado ao modelo On-Demand.

#### Etapa 2: Modernização para Serverless
- **Ferramenta:** AWS Lambda
- **Foco:** Eliminação da fatura por ociosidade de servidor.
- **Caso de Uso:** Execução de scripts e APIs apenas quando houver demanda real, garantindo que o faturamento ocorra apenas pelo tempo de execução (milissegundos).

#### Etapa 3: Inteligência em Armazenamento (S3)
- **Ferramenta:** Amazon S3 Intelligent-Tiering
- **Foco:** Automação do ciclo de vida dos dados.
- **Caso de Uso:** Movimentação automática de objetos entre camadas de acesso frequente e infrequente, otimizando o valor do GB armazenado sem impacto na disponibilidade.

### 3. Conclusão
Com a implementação dessas soluções, a **Abstergo Industries** projeta uma infraestrutura mais resiliente e financeiramente sustentável, com uma redução significativa no desperdício de recursos.

---

## 📂 Anexos e Demonstração Técnica

### I. Projeção de Economia (Estimativa Mensal)
O gráfico abaixo ilustra a queda nos custos operacionais após a transição para os serviços propostos:

![Gráfico de Redução de Custos](https://quickchart.io/chart?c={type:'bar',data:{labels:['Antes','Depois'],datasets:[{label:'Custo%20Mensal%20(USD)',data:[1000,300]}]}})

### II. Exemplo de Política S3 Lifecycle (JSON)
Configuração técnica para automação do armazenamento:

```json
{
  "Rules": [
    {
      "ID": "OtimizacaoCustosAbstergo",
      "Status": "Enabled",
      "Transitions": [
        { "Days": 30, "StorageClass": "STANDARD_IA" },
        { "Days": 90, "StorageClass": "GLACIER" }
      ],
      "Expiration": { "Days": 365 }
    }
  ]
}

```

### III. Manual de Boas Práticas
- Resiliência: Utilizar Spot Instances apenas em aplicações tolerantes a falhas.
- Monitoramento: Acompanhar diariamente o AWS Cost Explorer.
- Governança: Aplicar a Tag Project: Reducao_Custos_Farmacia em todos os novos recursos.

---

### Assinatura do Responsável pelo Projeto: 
Maike Simoncini da Silva
