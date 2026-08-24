# 💻 Modelador e Minimizador de AFD Interativo

> Um editor, simulador visual e minimizador interativo de alta fidelidade para **Autômatos Finitos Determinísticos (AFD)** com suporte completo ao **Algoritmo da Tabela de Distinguibilidade (Hopcroft/Moore)** e **Refinamento de Partições**.

🌐 **Acesse online:** [https://rovanni.github.io/Modelador_Minimizacao_AFD/](https://rovanni.github.io/Modelador_Minimizacao_AFD/)

Este projeto foi desenvolvido com foco em acessibilidade pedagógica, riqueza visual e rigor formal para apoiar professores e estudantes em cursos de **Teoria da Computação**, **Linguagens Formais e Autômatos** e **Compiladores**.

O sistema opera 100% *client-side* no navegador web, sem necessidade de instalação, compiladores, servidores ou dependências externas!

---

## ✨ Principais Funcionalidades

### 🧩 1. Minimização Completa & Passo a Passo
*   **Identificação e Remoção de Estados Inalcançáveis**:
    *   Algoritmo BFS a partir do estado inicial $q_0$.
    *   Destaque com bordas pontilhadas/amarelas no diagrama e remoção com 1 clique.
*   **Tabela Triangular de Distinguibilidade ($Q \times Q$)**:
    *   Matriz triangular interativa calculada dinamicamente para todos os pares $(p, q)$.
    *   Marcação de pares $0$-distinguíveis ($X_0$, estados finais vs. não-finais).
    *   Iterações sucessivas $k \ge 1$ com justificativa detalhada exibindo o símbolo $a \in \Sigma$ e a propagação de distinguibilidade.
    *   Reprodutor animado passo a passo (**Play / Pause / Avançar / Retroceder / Concluir**).
*   **Modo Desafio / Exercício para Alunos**:
    *   Permite ao aluno clicar manualmente nas células para preencher a matriz e validar suas respostas com cálculo de acertos e nota percentual imediata.
*   **Refinamento Sucessivo de Partições**:
    *   Visualização da árvore de partição $P_0 = \{F, Q \setminus F\} \to P_1 \to \dots \to P_{\text{final}}$.
    *   Definição formal da 5-tupla do autômato mínimo: $M' = (Q', \Sigma, \delta', q_0', F')$.
    *   Tabela de transição formal com classes de equivalência $[q]$.
*   **Comparação Lado a Lado & Testes Cruzados**:
    *   Dois painéis simultâneos exibindo o **AFD Original** e o **AFD Minimizado**.
    *   Bateria de testes cruzados com dezenas de cadeias representativas para demonstrar na prática que $L(M) = L(M')$.
*   **Substituição Direta no Canvas**:
    *   Transforme o AFD atual no seu equivalente mínimo no canvas com apenas um clique!

### 🎨 2. Editor Visual & Gestos no Canvas
*   **Criação Rápida de Estados**: Duplo clique no espaço vazio cria novos estados onde o cursor estiver.
*   **Conexão de Transições por Arraste**: Segure a tecla **Shift** ou ative o botão "Criar Transições" e arraste entre os estados.
*   **Menu de Contexto Customizado (Botão Direito)**: Definir como inicial, alternar aceitação, renomear ou excluir.
*   **Organização Geométrica**: Auto-layout em círculo ou grade com alinhamento e centralização automáticos.

### 💾 3. Exportação Acadêmica & Persistência
*   **Exportação para LaTeX / TikZ**: Gera código TikZ completo pronto para inclusão em relatórios e artigos acadêmicos.
*   **Exportação de Tabelas em LaTeX & Markdown**: Tabelas de distinguibilidade triangulares prontas para listas de exercícios e provas.
*   **Exportação PNG em Alta Resolução**: Com temas escuro, claro ou transparente (fator DPR = 2).
*   **Salvamento Automático (LocalStorage)** e **Importação/Exportação JSON**.

### ⚡ 4. Simulador Integrado de Cadeias
*   Simulação em tempo real (individual e passo a passo).
*   Testador em lote para validação de dezenas de cadeias simultaneamente.

---

## 🎮 Exemplos Didáticos Pré-Carregados

1.  **Exemplo Clássico (6 estados)**: Demonstração padrão com múltiplos pares equivalentes ($\{C, D, E\}$ e $\{A, B\}$) e estado inalcançável/redundante.
2.  **Paridade Redundante (6 estados $\to$ 2 estados)**: AFD com múltiplos estados redundantes de paridade de 0s e 1s.
3.  **Divisível por 3 (7 estados $\to$ 3 estados)**: AFD para módulo 3 com estados extras e inalcançáveis.
4.  **Já Mínimo (3 estados)**: Demonstração de verificação em que o algoritmo confirma que o AFD já está na sua forma irredutível.

---

## 🚀 Como Executar Localmente

Basta abrir o arquivo `index.html` em qualquer navegador moderno (Google Chrome, Firefox, Safari, Edge, Opera):

*   No Windows / macOS / Linux: Dê um duplo clique no arquivo `index.html`.
*   Ou utilize qualquer servidor local:
    ```bash
    python -m http.server 8000
    ```
    Acesse `http://localhost:8000/index.html`.

---

## 📄 Licença

Este projeto é disponibilizado sob a licença **MIT** para fins educacionais e acadêmicos.
