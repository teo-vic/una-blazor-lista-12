# 🌱 EcoMonitor - Prova de Conceito (Blazor)

## 👤 Identificação

* **Nome:** Seu Nome Completo
* **Curso:** Seu Curso (ex: Sistemas de Informação)

---

## 🧠 Heurísticas de Nielsen Aplicadas

### 1. Visibilidade do Status do Sistema

O sistema mantém o usuário sempre informado sobre o que está acontecendo.
No componente **EcoStatus**, isso é aplicado através da exibição do contador atualizado em tempo real após cada clique no botão.

👉 Exemplo: Ao registrar uma ação, o valor total é imediatamente atualizado na tela.

---

### 2. Feedback Imediato

Cada interação do usuário gera uma resposta clara e instantânea.
Ao clicar no botão "Registrar ação", o sistema incrementa o valor e altera a cor do texto quando a meta é atingida.

👉 Exemplo: Quando o contador ultrapassa 50 pontos, a cor muda para verde, indicando progresso.

---

## ⚙️ Guia de Execução

Siga os passos abaixo para rodar o projeto:

1. Abra o terminal na pasta do projeto
2. Execute o comando:

```
dotnet run --launch-profile https
```

3. Abra o navegador no endereço exibido (geralmente):

```
https://localhost:xxxx
```

---

## 💻 Explicação Técnica

O componente **EcoStatus** foi desenvolvido de forma reutilizável utilizando o atributo `[Parameter]`.

### 🔹 Como funciona:

O `[Parameter]` permite passar valores da página principal (**Home.razor**) para o componente.

```razor
[Parameter]
public int Peso { get; set; }
```

Cada instância do componente recebe um valor diferente para o **Peso**, que define quanto será incrementado no contador a cada clique.

### 🔹 Exemplo de uso:

```razor
<EcoStatus Titulo="Plantio de Árvores" Peso="10" />
```

👉 Nesse caso:

* O título exibido será "Plantio de Árvores"
* Cada clique adiciona **10 pontos** ao contador

### 🔹 Benefício:

Isso torna o componente reutilizável, pois o mesmo código pode ser usado para diferentes ações ambientais, apenas alterando os parâmetros.

---

## 🚀 Conclusão

O EcoMonitor demonstra como conceitos de componentização, estado e interatividade podem ser aplicados com Blazor para criar interfaces dinâmicas e reutilizáveis, alinhadas com boas práticas de experiência do usuário.
