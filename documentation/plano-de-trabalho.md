# FichaAqui — Plano de Trabalho da Estagiária

## Referências
- **Carga:** 1h por dia · 5 dias por semana · 5h semanais
- **Ciclo:** Figma → Componente → Tela → JS → Revisão → Próxima tela
- **Referência de componentes:** Material 3 (visual e comportamento), não como biblioteca
- **Styleguide:** `styleguide.html` no repositório
- **Critério de pronto:** visual fiel ao Figma + todos os estados JS funcionando + PR aprovada

---

## Fase 0 — Ambientação (Semana 1)

> Objetivo: ela se sentir confortável com as ferramentas antes de tocar no projeto.

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 1 | Explorar o Figma: criar um frame de 1440×900px (desktop), adicionar retângulos, textos e mudar cores | Arquivo salvo no Figma com os elementos criados |
| Dia 2 | Ler o `styleguide.html` completo e identificar quais componentes existem | Lista escrita (pode ser num comentário no GitHub) |
| Dia 3 | No Figma: recriar o card de saldo do styleguide (cor, tipografia, espaçamento) | Card visualmente igual ao styleguide |
| Dia 4 | Criar a estrutura de pastas do projeto no repositório e fazer o primeiro commit na branch `feat/estrutura-inicial` | PR aberta para a `dev` com a estrutura de pastas |
| Dia 5 | Abrir o `styleguide.html` no VS Code, entender a estrutura HTML/CSS e anotar dúvidas | Lista de dúvidas enviada para você revisar |

---

## Fase 1 — Componentes Base (Semanas 2 e 3)

> Objetivo: construir a biblioteca de componentes que vai ser usada em todas as telas.
> Cada componente: olha o Material 3 → entende os estados → reproduz com o styleguide do FichaAqui.

### Semana 2

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 6 | Figma: desenhar o componente Button (primary, secondary, ghost, danger, disabled) | 5 variações no Figma |
| Dia 7 | Código: criar `components/button.css` com os 5 estilos | Visual igual ao Figma |
| Dia 8 | Código: criar `components/button.js` com estados hover, focus e disabled | Estados funcionando no browser |
| Dia 9 | Figma: desenhar o componente Input (default, focus, error, disabled) | 4 estados no Figma |
| Dia 10 | Código: criar `components/input.css` e `components/input.js` | Validação de campo vazio + estado de erro funcionando |

### Semana 3

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 11 | Figma: desenhar Badge (todas as variações) e Alert (sucesso, erro, atenção, info) | Componentes no Figma |
| Dia 12 | Código: criar `components/badge.css` e `components/alert.css` | Visual igual ao styleguide |
| Dia 13 | Figma: desenhar Card (simples e destacado) | 2 variações no Figma |
| Dia 14 | Código: criar `components/card.css` | Visual igual ao Figma |
| Dia 15 | Revisão geral dos componentes + PR para `dev` | PR aprovada, componentes todos funcionando juntos numa página de teste |

---

## Fase 2 — Fluxo do Participante (Semanas 4, 5 e 6)

> Objetivo: primeira tela real do app, do Figma ao código completo.

### Semana 4 — Tela de Login/Cadastro

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 16 | Figma: desenhar tela de login (logo, campo email, campo senha, botão entrar, link cadastro) | Tela no Figma fiel ao styleguide |
| Dia 17 | Figma: desenhar tela de cadastro (nome, email, telefone, senha, botão criar conta) | Tela no Figma fiel ao styleguide |
| Dia 18 | Código: estrutura HTML das duas telas usando os componentes existentes | HTML semântico criado |
| Dia 19 | Código: CSS das duas telas (layout, espaçamentos, centralização desktop) | Visual igual ao Figma em desktop |
| Dia 20 | Código: JS — validação dos campos + alternar entre login e cadastro | Validação funcionando + transição entre telas |

### Semana 5 — Página do Evento + Compra de Fichas

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 21 | Figma: desenhar página pública do evento (banner, nome, data, valor da ficha, botão comprar) | Tela no Figma |
| Dia 22 | Figma: desenhar tela de compra (quantidade de fichas, total em R$, botão gerar Pix) | Tela no Figma com cálculo dinâmico visível |
| Dia 23 | Código: HTML + CSS da página do evento | Visual igual ao Figma |
| Dia 24 | Código: HTML + CSS da tela de compra | Visual igual ao Figma |
| Dia 25 | Código: JS — seletor de quantidade atualiza total em tempo real + estado de loading no botão | Cálculo dinâmico + loading funcionando |

### Semana 6 — Carteira + QR Code

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 26 | Figma: desenhar tela da carteira (saldo em fichas, botão comprar mais, histórico de transações) | Tela no Figma |
| Dia 27 | Figma: desenhar tela do QR code (QR centralizado, nome do participante, saldo, timer de expiração) | Tela no Figma |
| Dia 28 | Código: HTML + CSS da carteira | Visual igual ao Figma |
| Dia 29 | Código: HTML + CSS da tela de QR (QR simulado com imagem placeholder) | Visual igual ao Figma |
| Dia 30 | Código: JS — timer de expiração do QR (5 min, atualiza em tempo real) + botão renovar | Timer funcionando + renovação |

---

## Fase 3 — Fluxo do Barraqueiro (Semanas 7 e 8)

> Objetivo: segunda persona do app. Componentes novos: leitor de QR simulado, confirmação de débito.

### Semana 7 — Tela de Cobrança

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 31 | Figma: desenhar tela inicial do barraqueiro (nome da barraca, campo valor em fichas, botão escanear) | Tela no Figma |
| Dia 32 | Figma: desenhar tela de scan (área da câmera simulada, instrução, botão cancelar) | Tela no Figma |
| Dia 33 | Figma: desenhar tela de confirmação (nome do participante, saldo atual, valor a cobrar, confirmar/cancelar) | Tela no Figma |
| Dia 34 | Código: HTML + CSS das 3 telas | Visual igual ao Figma |
| Dia 35 | Código: JS — navegação entre as 3 telas + simulação do scan (botão "simular QR lido") | Fluxo completo navegável |

### Semana 8 — Feedback e Painel da Barraca

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 36 | Figma: desenhar tela de sucesso do débito (ícone, valor cobrado, novo saldo, botão nova cobrança) | Tela no Figma |
| Dia 37 | Figma: desenhar painel da barraca (total do dia em fichas, lista de cobranças) | Tela no Figma |
| Dia 38 | Código: HTML + CSS das 2 telas | Visual igual ao Figma |
| Dia 39 | Código: JS — estado de sucesso/erro + atualizar lista de cobranças dinamicamente | Estados funcionando |
| Dia 40 | Revisão do fluxo completo barraqueiro + PR para `dev` | PR aprovada, fluxo navegável do início ao fim |

---

## Fase 4 — Painel Admin do Evento (Semanas 9 e 10)

> Objetivo: telas mais complexas com tabelas, formulários e múltiplas ações.

### Semana 9 — Criar Evento + Gestão de Barracas

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 41 | Figma: desenhar formulário de criação de evento (nome, data, valor da ficha, chave Pix) | Tela no Figma |
| Dia 42 | Figma: desenhar lista de barracas + formulário de nova barraca | Telas no Figma |
| Dia 43 | Código: HTML + CSS do formulário de evento | Visual igual ao Figma |
| Dia 44 | Código: HTML + CSS da lista de barracas | Visual igual ao Figma |
| Dia 45 | Código: JS — adicionar barraca dinamicamente na lista + validação dos formulários | Formulários funcionando |

### Semana 10 — Relatórios e Visão Geral

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 46 | Figma: desenhar painel geral do evento (métricas: total arrecadado, fichas vendidas, participantes) | Tela no Figma |
| Dia 47 | Figma: desenhar tabela de participantes com saldo | Tela no Figma |
| Dia 48 | Código: HTML + CSS do painel de métricas | Visual igual ao Figma |
| Dia 49 | Código: HTML + CSS da tabela de participantes | Visual igual ao Figma |
| Dia 50 | Código: JS — ordenar tabela por coluna (nome, saldo) | Ordenação funcionando |

---

## Fase 5 — Financeiro (Semanas 11 e 12)

> Objetivo: última persona. Telas de saque e repasse.

### Semana 11 — Saques

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 51 | Figma: desenhar lista de barracas com total a receber e botão solicitar saque | Tela no Figma |
| Dia 52 | Figma: desenhar modal de confirmação de saque (valor, chave Pix, confirmar) | Tela no Figma |
| Dia 53 | Código: HTML + CSS da lista de saques | Visual igual ao Figma |
| Dia 54 | Código: HTML + CSS do modal | Visual igual ao Figma |
| Dia 55 | Código: JS — abrir/fechar modal + estado de processando + sucesso | Modal e estados funcionando |

### Semana 12 — Extrato e Revisão Final

| Dia | Tarefa | Critério de pronto |
|-----|--------|--------------------|
| Dia 56 | Figma: desenhar extrato financeiro por barraca (lista de transações, total) | Tela no Figma |
| Dia 57 | Código: HTML + CSS do extrato | Visual igual ao Figma |
| Dia 58 | Código: JS — filtrar extrato por barraca | Filtro funcionando |
| Dia 59 | Revisão geral — testar navegação entre todos os fluxos | Todos os fluxos navegáveis sem erros |
| Dia 60 | PR final para `dev` + você faz merge para `main` | Versão mínima no ar |

---

## Resumo de Prazos

| Fase | Entrega | Prazo |
|------|---------|-------|
| Fase 0 — Ambientação | Estrutura do projeto no repositório | Semana 1 |
| Fase 1 — Componentes base | Biblioteca de componentes funcionando | Semana 3 |
| Fase 2 — Participante | Fluxo completo do participante | Semana 6 |
| Fase 3 — Barraqueiro | Fluxo completo do barraqueiro | Semana 8 |
| Fase 4 — Admin | Painel admin funcionando | Semana 10 |
| Fase 5 — Financeiro | Versão mínima completa no ar | Semana 12 |

---

## Dicas para o orientador

- **Revisão semanal:** reserve 15min por semana para ver o que ela fez e dar feedback antes de ela avançar
- **Não desbloquear antes da hora:** se ela travou num dia, deixa tentar resolver sozinha por 30min antes de ajudar — faz parte do aprendizado
- **PR é obrigatória:** nenhuma tarefa está pronta sem PR aprovada — ensina o fluxo real desde o início
- **Elogie o progresso:** para quem está começando, ver o próprio código no ar é muito motivador — celebre cada merge na `main`
