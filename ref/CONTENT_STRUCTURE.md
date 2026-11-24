# Content Structure - Dashboard Mastery

Documentacao da estrutura e metodologia de criacao de conteudo para os modulos do curso.

---

## 1. Estrutura Geral de um Modulo

Cada modulo segue uma estrutura pedagogica consistente:

```
1. HEADER
   └── Badge da trilha (cor correspondente)
   └── Titulo com emoji
   └── Descricao (1-2 linhas)

2. STATS BANNER
   └── 3-4 metricas-chave do modulo (Topicos, Duracao, Nivel, Tipo)

3. TOPICOS EXPANSIVEIS (6 por modulo)
   └── Numero em circulo + emoji + titulo
   └── 3 secoes internas obrigatorias
   └── Comportamento accordion

4. ELEMENTOS DE SUPORTE
   └── Exemplos praticos
   └── Comparacoes (fazer/nao fazer)
   └── Dados e pesquisas

5. RESUMO/CHECKLIST
   └── Sintese dos pontos principais
   └── CTA para proximo modulo
```

---

## 2. Estrutura de um Topico Expansivel

### 2.1 Cabecalho do Topico

```html
<button onclick="toggleTopic(this)" class="w-full px-6 py-4 flex items-center...">
  <span class="w-6 h-6 rounded-full bg-emerald-500/20 text-emerald-400 text-sm font-bold flex items-center justify-center">1</span>
  <span class="text-lg">🎯</span>
  <div>
    <span class="font-medium">Titulo do Topico</span>
    <span class="text-neutral-500 text-sm ml-2">- Descricao breve</span>
  </div>
</button>
```

### 2.2 Conteudo Interno (3 Secoes Obrigatorias)

Cada topico DEVE ter estas 3 secoes:

| Secao | Descricao |
|-------|-----------|
| **O que e** | Definicao clara e objetiva do conceito |
| **Por que aprender** | Justificativa e beneficios praticos |
| **Conceitos-chave** | Lista dos pontos principais a memorizar |

**HTML:**
```html
<div class="bg-dark-700/50 rounded-lg p-4 space-y-3">
  <div>
    <span class="text-emerald-400 font-semibold">O que e:</span>
    <p class="text-neutral-300 text-sm">Dashboard e uma interface visual...</p>
  </div>
  <div>
    <span class="text-emerald-400 font-semibold">Por que aprender:</span>
    <p class="text-neutral-300 text-sm">Reduz tempo de analise em 80%...</p>
  </div>
  <div>
    <span class="text-emerald-400 font-semibold">Conceitos-chave:</span>
    <p class="text-neutral-300 text-sm">Consolidacao, tempo real, interatividade...</p>
  </div>
</div>
```

---

## 3. Tipos de Boxes de Conteudo

### 3.1 Box de Conceito Principal
- **Cor:** Gradiente da cor tematica da trilha
- **Uso:** Explicar o conceito central
- **Exemplo:** `bg-gradient-to-br from-emerald-900/30 to-dark-800`

### 3.2 Box de Detalhamento Tecnico
- **Cor:** `bg-dark-700/50` (cinza neutro)
- **Uso:** Aprofundar com detalhes tecnicos
- **Elementos:** Listas, grids, timelines

### 3.3 Box de Dados/Pesquisa
- **Cor:** `bg-blue-900/20` com borda `border-blue-500/30`
- **Uso:** Apresentar estatisticas e fontes

### 3.4 Box de Dica Pratica
- **Cor:** `bg-primary/10` com borda `border-primary/30`
- **Uso:** Aplicacao pratica do conceito

### 3.5 Grid de Comparacao
- **Cores:** `bg-emerald-900/20` vs `bg-red-900/20`
- **Uso:** Contrastar praticas corretas e incorretas

---

## 4. Estrutura da Pagina de Trilha (Index)

```
TRILHA INDEX
├── Navigation Global (com ARCKHÉ AI)
├── Header
│   └── Badge da trilha
│   └── Titulo + emoji
│   └── Descricao
│   └── Stats (Modulos, Topicos, Duracao, Nivel)
├── Modulos (8 por trilha)
│   └── Modulo Card
│       ├── Header (numero, titulo, descricao)
│       ├── Topicos Expansiveis (6 por modulo)
│       │   └── Numero em circulo (nao seta)
│       │   └── Emoji + titulo + subtitulo
│       │   └── Conteudo com 3 secoes
│       └── Botoes (ESQUERDA)
│           └── Ver em Modal
│           └── Ver Completo
└── Footer
```

---

## 5. Estrutura da Pagina Completa de Modulo

```
MODULO COMPLETO
├── Navigation Global (com ARCKHÉ AI)
├── Breadcrumb (Inicio / Trilha X / Modulo X.X)
├── Header
│   └── Badge do modulo
│   └── Titulo + emoji
│   └── Descricao
│   └── Stats (Topicos, Duracao, Nivel, Tipo)
├── Topicos (6 secoes completas)
│   └── Section por topico
│       ├── Numero em circulo + titulo
│       ├── Paragrafo introdutorio
│       ├── Boxes de detalhamento
│       ├── Grids de comparacao
│       └── Dicas praticas
├── Resumo Final
│   └── O que aprendemos (checklist)
│   └── Proximo modulo
│   └── CTAs de navegacao
└── Footer
```

---

## 6. Cores por Trilha

| Trilha | Nome | Cor Principal | Classes |
|--------|------|---------------|---------|
| Trilha 1 | Fundamentos | Emerald | `text-emerald-400`, `bg-emerald-500/20`, `border-emerald-500/30` |
| Trilha 2 | Tecnicas | Blue | `text-blue-400`, `bg-blue-500/20`, `border-blue-500/30` |
| Trilha 3 | Avancado | Purple | `text-purple-400`, `bg-purple-500/20`, `border-purple-500/30` |

---

## 7. Padroes de Escrita

### 7.1 Tom de Voz
- **Direto e pratico:** Sem enrolacao
- **Profissional:** Foco em dashboards empresariais
- **Confiante:** Afirmacoes claras
- **Didatico:** Explicacoes passo a passo

### 7.2 Estrutura de Paragrafos
- **Maximo 3-4 linhas** por paragrafo
- **Primeira frase:** Conceito principal
- **Destaque:** Palavra-chave em **negrito** ou cor da trilha

### 7.3 Uso de Listas
- **Bullets (•):** Para itens sem ordem especifica
- **Numeros (1, 2, 3):** Para passos sequenciais
- **Simbolos (check, X):** Para fazer/nao fazer

---

## 8. Checklist de Qualidade do Conteudo

### Antes de Publicar, Verificar:

**Estrutura:**
- [ ] Navigation com ARCKHÉ AI (sky-400)
- [ ] Trilhas com descricao (Fundamentos, Tecnicas, Avancado)
- [ ] Header completo (badge, titulo, descricao)
- [ ] Stats banner com metricas relevantes
- [ ] Topicos com numeros (nao setas)
- [ ] 3 secoes por topico (O que e, Por que, Conceitos)
- [ ] Botoes a esquerda (justify-start)
- [ ] Resumo/checklist no final

**Visual:**
- [ ] Cores seguem o padrao da trilha
- [ ] Emojis usados consistentemente
- [ ] Dark/light mode funcionando

**Tecnico:**
- [ ] Links funcionando
- [ ] Responsivo em mobile
- [ ] Modal carrega conteudo completo
