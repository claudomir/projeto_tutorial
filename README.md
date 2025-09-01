
# 📘 Apostila de CSS  
## **Pseudo-classes e Pseudo-elementos**

---

## **1. Introdução**
No CSS, **pseudo-classes** e **pseudo-elementos** são recursos que permitem **estilizar elementos HTML de forma especial**, sem precisar criar novas tags ou alterar o conteúdo do HTML.

- **Pseudo-classes** → Definem **estados especiais** de um elemento, como quando o mouse passa por cima ou quando um campo está selecionado.
- **Pseudo-elementos** → Permitem **estilizar partes específicas** de um elemento ou adicionar conteúdo extra via CSS.

---

## **2. Pseudo-classes**
### **2.1 Conceito**
Uma **pseudo-classe** descreve um **estado ou condição** de um elemento, aplicando um estilo apenas quando essa condição é verdadeira.

### **2.2 Sintaxe**
```css
seletor:pseudo-classe {
    propriedade: valor;
}
```

### **2.3 Principais Pseudo-classes**
| Pseudo-classe | Descrição | Exemplo de uso |
|--------------|-----------|----------------|
| `:hover` | Quando o mouse está sobre o elemento | Mudar cor de um botão |
| `:active` | Quando o elemento está sendo clicado | Botão fica mais escuro no clique |
| `:focus` | Quando o elemento recebe foco (campo de formulário) | Borda colorida no campo |
| `:visited` | Link já visitado | Cor diferente para links visitados |
| `:first-child` | Primeiro filho de um elemento pai | Estilo especial no primeiro item |
| `:last-child` | Último filho de um elemento pai | Estilo especial no último item |
| `:nth-child(n)` | Elemento na posição “n” | Linhas alternadas de tabela |

---

### **2.4 Exemplo aplicado**
**HTML**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemplo Pseudo-classes</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <a href="#">Link normal</a>
    <a href="#">Link visitado</a>

    <br><br>

    <button>Botão</button>

    <br><br>

    <ul>
        <li>Primeiro item</li>
        <li>Segundo item</li>
        <li>Terceiro item</li>
    </ul>
</body>
</html>
```

**CSS (style.css)**
```css
a:hover {
    color: red; /* Quando o mouse passar */
}

a:visited {
    color: purple; /* Link já visitado */
}

button:hover {
    background-color: blue;
    color: white;
}

button:active {
    background-color: navy;
}

li:first-child {
    font-weight: bold; /* Primeiro item */
}

li:last-child {
    color: green; /* Último item */
}

li:nth-child(2) {
    color: orange; /* Segundo item */
}
```

---

## **3. Pseudo-elementos**
### **3.1 Conceito**
Um **pseudo-elemento** estiliza **uma parte específica** de um elemento ou adiciona conteúdo extra antes ou depois dele.

### **3.2 Sintaxe**
```css
seletor::pseudo-elemento {
    propriedade: valor;
}
```
> **Obs.:** O uso de dois pontos duplos `::` é recomendado para diferenciar de pseudo-classes.

### **3.3 Principais Pseudo-elementos**
| Pseudo-elemento | Descrição | Exemplo de uso |
|-----------------|-----------|----------------|
| `::first-letter` | Primeira letra do texto | Estilo de “capitular” em parágrafos |
| `::first-line` | Primeira linha do texto | Estilo especial para primeira linha |
| `::before` | Conteúdo antes do elemento | Adicionar ícones ou símbolos |
| `::after` | Conteúdo depois do elemento | Adicionar texto extra |
| `::selection` | Texto selecionado pelo usuário | Alterar cor de seleção |

---

### **3.4 Exemplo aplicado**
**HTML**
```html
<!DOCTYPE html>
<html>
<head>
    <title>Exemplo Pseudo-elementos</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Título da Página</h1>
    <p>Este é um parágrafo para demonstrar o uso de pseudo-elementos no CSS.</p>
</body>
</html>
```

**CSS (style.css)**
```css
p::first-letter {
    font-size: 2em;
    color: red;
    font-weight: bold;
}

p::first-line {
    color: blue;
}

h1::before {
    content: "🔥 ";
}

h1::after {
    content: " ✨";
}

p::selection {
    background-color: yellow;
    color: black;
}
```

---

## **4. Diferença entre Pseudo-classes e Pseudo-elementos**
| Característica | Pseudo-classe | Pseudo-elemento |
|----------------|--------------|-----------------|
| O que faz | Define **estados** de um elemento | Estiliza **partes específicas** do elemento |
| Sintaxe | `:nome` | `::nome` |
| Exemplo | `a:hover` | `p::first-letter` |

---

## **5. Exercícios**
### **Parte 1 – Pseudo-classes**
1. Crie um botão que mude de cor quando o mouse passar por cima e quando for clicado.
2. Estilize links visitados para que fiquem com cor roxa.
3. Faça com que o primeiro item de uma lista fique em negrito.
4. Pinte as linhas pares de uma tabela com cor de fundo cinza claro usando `:nth-child()`.

### **Parte 2 – Pseudo-elementos**
1. Use `::first-letter` para deixar a primeira letra de um parágrafo grande e vermelha.
2. Adicione um ícone antes de todos os títulos `<h2>` usando `::before`.
3. Coloque o texto "(fim)" no final de todos os parágrafos usando `::after`.
4. Mude a cor de fundo e do texto quando um trecho for selecionado (`::selection`).

