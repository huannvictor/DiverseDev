# 🤖 AGENT.md — Guia para Agentes de IA e Colaboradores

Este arquivo orienta assistentes de IA e pessoas colaboradoras sobre como o projeto **VelozMart — Marketplace Priority Sorter (MPS)** está organizado e como editá-lo mantendo a simplicidade e consistência.

---

## 1. Contexto do Projeto

* **Programa:** Coding Tank — DiverseDEV 2026 (Ada Tech & Mercado Eletrônico).
* **Natureza do Projeto:** Protótipo conceitual e proposta técnica de engenharia (TI → Logística) para priorização de pedidos em tempo real.
* **Regra da Solução:** Arquitetura híbrida em 2 estágios combinando **Max-Heap (`O(log n)`)** com pontuação composta (`70% IA + 30% Urgência + Bônus Crítico de +25 pts para prazo <= 15 min`) e um **Buffer de Doca (`k = 10`) ordenado com Insertion Sort (`O(k)`)** para encaixar pacotes `P`, `M` e `G` conforme as vagas livres da bancada.

---

## 2. Onde Editar Cada Coisa

O projeto foi mantido intencionalmente simples e sem dependências externas:

* **[`Velox Mart - Grupo 04.html`](Velox%20Mart%20-%20Grupo%2004.html) e [`Velox Mart - Grupo 04.pdf`](Velox%20Mart%20-%20Grupo%2004.pdf):**
  * É a proposta técnica oficial formatada em estilo executivo claro (A4 print-ready) aderente às 5 seções do template da banca.
  * **Seções Obrigatórias:** (1) Problema, (2) Algoritmo / Estrutura, (3) Diagrama, (4) Trade-offs, (5) Próximos passos.
  * **Diagrama SVG Vetorial:** Gráfico de fluxo embutido diretamente no HTML com legenda e marcação de contraste.
* **[`docs/v01/`](docs/v01/):**
  * Versões conceituais anteriores (`entrega_velozmart_mps.html` e `entrega_velozmart_mps_com_roteiro.html`), onde fica preservado o roteiro de fala detalhado dos 5 apresentadores.
* **[`docs/enunciado-projeto.md`](docs/enunciado-projeto.md) e [`docs/guia-coding-tank.html`](docs/guia-coding-tank.html):**
  * Contêm as instruções originais e os requisitos mínimos da avaliação (template Canvas-PDF da banca). Não devem ter suas regras alteradas.
* **[`docs/brainstorming-grupo.md`](docs/brainstorming-grupo.md):**
  * Rascunho colaborativo com as ideias originais do grupo e as duas versões de pseudocódigo.

---

## 3. Boas Práticas ao Modificar o `Velox Mart - Grupo 04.html`

1. **Mantenha o arquivo autocontido:** Sem dependências externas de pacotes (`npm`) ou fontes externas obrigatórias, para abrir com duplo clique em qualquer navegador.
2. **Preserve a Diagramação A4 e Quebras de Página (`@page` e `@media print`):**
   * Configuração de página `@page { size: A4; margin: 12mm 13mm }`.
   * A classe `.topbar` deve permanecer oculta na impressão (`display: none`).
   * Elementos sensíveis usam `break-inside: avoid` e `.page-before` usa `break-before: page`.
3. **Preserve a Acessibilidade Visual:** Cores acompanhadas por texto legível, ícones ou bordas distintivas (não depender apenas de cor).

