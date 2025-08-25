# 🌐 Aula de Programação Web  
## CSS – Seletores Personalizados: id e class  

---

## 1. O que são seletores em CSS?  
Seletores são como “endereços” que o CSS usa para encontrar os elementos de uma página HTML e aplicar estilos a eles.  

Exemplo:  
```css
p {
  color: blue;
}
```

👉 Esse seletor pega **todos os parágrafos (`<p>`)** e deixa o texto azul.  

Mas, e se quisermos **estilizar apenas um parágrafo específico**, ou um **grupo de elementos**?  
Aí entram os **seletores personalizados: `id` e `class`**.  

---

## 2. Seletor **id** (`#`)  
- O **id** é como um **RG**: só pode existir **um único elemento com esse identificador** na página.  
- Para usar, no HTML colocamos o atributo `id` no elemento.  
- No CSS, usamos o símbolo **#** para indicar que estamos chamando um id.  

**Exemplo:**  
```html
<p id="destaque">Esse parágrafo é único e especial.</p>
```

```css
#destaque {
  color: red;
  font-weight: bold;
}
```

👉 Apenas o parágrafo com `id="destaque"` ficará vermelho e em negrito.  

---

## 3. Seletor **class** (`.`)  
- A **class** é como um **apelido**: pode ser usada em **vários elementos ao mesmo tempo**.  
- No HTML colocamos o atributo `class`.  
- No CSS usamos o símbolo **.** (ponto).  

**Exemplo:**  
```html
<p class="importante">Esse é importante.</p>
<p class="importante">Esse também é importante.</p>
<p>Esse não é importante.</p>
```

```css
.importante {
  color: green;
  font-style: italic;
}
```

👉 Todos os parágrafos com `class="importante"` ficarão verdes e em itálico.  

---

## 4. Diferença entre **id** e **class**  
- `id` → identifica **um único elemento** (único na página).  
- `class` → pode ser usada em **vários elementos**.  

📌 **Analogia:**  
Imagine uma sala de aula:  
- Cada aluno tem seu **id** (número de matrícula, único).  
- Mas vários alunos podem ter a **mesma class** (ex.: todos que fazem parte do “time de futebol”).  

---

## 5. Exemplos combinando  
```html
<h1 id="titulo-principal">Bem-vindo!</h1>
<p class="texto">Esse é o primeiro parágrafo.</p>
<p class="texto">Esse é o segundo parágrafo.</p>
<p>Esse não tem classe.</p>
```

```css
#titulo-principal {
  text-align: center;
  color: blue;
}

.texto {
  font-size: 18px;
  color: gray;
}
```

👉 O título ficará azul e centralizado, enquanto os parágrafos com class “texto” terão fonte 18px e cinza.  

---

# ✍️ Exercícios de fixação  

1. Crie um parágrafo com `id="aviso"` e faça o texto aparecer em vermelho e em negrito.  
2. Crie três títulos `<h2>` com `class="secao"`. Faça todos eles ficarem verdes.  
3. Crie dois parágrafos com a mesma classe chamada `"destaque"`, deixando-os em itálico e cor azul.  
4. No mesmo código, crie um parágrafo sem classe nem id e veja como ele ficará sem estilo.  
5. Explique com suas palavras a diferença entre `id` e `class`.  

---

## 🔹 Dicas finais  
- Use **id** quando quiser aplicar estilo a **um único elemento**.  
- Use **class** quando quiser aplicar estilo a **vários elementos** ao mesmo tempo.  
- Você pode combinar **id e class** em um mesmo elemento se precisar de estilos diferentes.  

