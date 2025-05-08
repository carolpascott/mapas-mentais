# 🧮 Contagem Funcional de Software

## 🎯 O que é?
- Técnica para medir o **tamanho funcional** de um software.
- Avalia o **que o sistema entrega ao usuário**, não a tecnologia usada.
- Foco em **entradas, saídas, consultas e arquivos manipulados**.

## 📌 Finalidade
- Estimar **esforço, custo e prazo**.
- Padronizar contratos com fábricas de software.
- Base para medição de produtividade.

## 🧱 Tipos de Funcionalidade (IFPUG)

### **Transacional**
  #### 🔹 EE – Entrada Externa
  - Dados ou comandos inseridos pelo usuário.
  - Afetam o sistema ou seus arquivos.
  - Ex: Cadastro de cliente, login.

  #### 🔸 CE – Consulta Externa
  - Resposta sem processamento significativo.
  - Ex: Busca de dados por nome ou código.

  #### 🔸 SE – Saída Externa
  - Dados gerados com **processamento adicional**.
  - Ex: Relatório de vendas com cálculos.

### **De Dados**

  #### 🗃️ AIE – Arquivo de Interface Externa
  - Conjunto de dados usados **por outro sistema**, mas referenciados.
  - Ex: O sistema de vendas lê os clientes do sistema financeiro.
  
  #### 🗂️ ALI – Arquivo Lógico Interno
  - Conjunto de dados **mantidos pelo sistema**.
  - Dados logicamente relacionados e controlados internamente.
  - Ex: Tabela de produtos no sistema.


## 🛠️ Etapas da Contagem Funcional (IFPUG)

1. 📄 **Obter a documentação funcional**
2. 🎯 **Definir o escopo da contagem**
3. 🌐 **Identificar a fronteira do sistema** (Define o que está dentro e fora do sistema)
4. 🧱 **Identificar as funções transacionais (EE, SE, CE)**
5. 🗂️ **Identificar as funções de dados (ALI, AIE)**
6. 📊 **Classificar e pontuar a complexidade**
7. 🧮 **Calcular os pontos de função brutos**
8. ⚖️ **Aplicar os deflatores (ajuste)**
9. ✅ **Obter o total de PF ajustado**

## 🧮 Cálculo dos Pontos de Função (PF)

### 📌 Classificação por Complexidade

| Tipo | Baixa | Média | Alta |
|------|-------|-------|------|
| EE   | 3     | 4     | 6    |
| CE   | 3     | 4     | 6    |
| SE   | 4     | 5     | 7    |
| AIE  | 5     | 7     | 10   |
| ALI  | 7     | 10    | 15   |


### 📌 Fórmula final
- **PF Bruto** = soma dos pontos baseados nas funções e complexidade.
- PF Ajustado = PF Bruto × fórmula com deflatores (14 características).

## 📐 NESMA
- Metodologia alternativa (padrão europeu).
- Mais simples que IFPUG, boa para estimativas rápidas.
- Permite contagem parcial e considera algumas funções não funcionais.

## 🧠 Deflatores (Fatores de Ajuste Técnico)
- Ajustam a contagem de PF com base na **complexidade técnica e ambiental**.
- Exemplos de características:
  - Confiabilidade
  - Eficiência
  - Facilidade de instalação
  - Portabilidade
  - Uso de software reutilizável