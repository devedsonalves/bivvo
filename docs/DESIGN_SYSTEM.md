# Bivvo — Design System da Interface

> **Versão:** 1.0 · **Status:** Diretrizes iniciais · **Plataformas:** Mobile (React Native + Expo) e Web (React)

## 1. Objetivo

Definir uma linguagem visual consistente para o **Bivvo**, aplicativo que transforma gravações de áudio em ordens de serviço com auxílio de inteligência artificial. O design deve transmitir **clareza, agilidade, confiança e simplicidade**, priorizando o trabalho de campo no mobile e o acompanhamento operacional no dashboard web.

Este documento é a referência visual do projeto, não a arquitetura técnica da API.

## 2. Identidade visual

- **Marca:** Bivvo (nome de trabalho; verificar disponibilidade antes do lançamento).
- **Mascote:** castor de corpo inteiro, de construção geométrica e minimalista.
- **Cor principal do mascote:** marrom escuro `#431407`.
- **Cor de ação:** laranja queimado `#EA580C`.
- **Fundo principal:** creme `#FFF7ED`.
- **Estilo:** minimalista, acolhedor e profissional; formas suaves, áreas bem definidas e poucos elementos decorativos.
- **Tom textual:** direto, acessível e objetivo. Exemplo: “Gravar áudio”, “Revisar ordem”, “Concluir serviço”.

### Regras de uso da marca

1. Usar o castor sem distorcer proporções nem adicionar efeitos 3D, gradientes ou sombras fortes.
2. Preferir o castor em marrom escuro sobre fundo creme ou branco.
3. Reservar o laranja às ações, indicadores ativos e detalhes de marca, evitando aplicá-lo indiscriminadamente.
4. Manter área de respiro mínima equivalente a aproximadamente 20% da largura do símbolo em volta da marca.
5. Preparar versões horizontal, símbolo isolado e monocromática para tamanhos pequenos. O desenho final deve ser validado em 24 px, 32 px e 48 px.

## 3. Paleta de cores

### 3.1 Tokens principais

| Token | Nome | Hex | Uso principal |
|---|---|---|---|
| `brand.primary` | Laranja queimado | `#EA580C` | Gravação, botões primários, links de ação e destaques |
| `brand.dark` | Marrom escuro | `#431407` | Logo, títulos e elementos da marca |
| `surface.canvas` | Creme | `#FFF7ED` | Fundo das telas |
| `surface.card` | Branco | `#FFFFFF` | Cards, inputs e superfícies elevadas |
| `text.secondary` | Cinza quente | `#57534E` | Descrições, legendas e informações secundárias |
| `status.success` | Verde | `#15803D` | Ordens concluídas e confirmações |

### 3.2 Tokens complementares propostos

Estas cores complementam a paleta original para permitir bordas, textos, interações e estados sem improvisação.

| Token | Hex | Uso |
|---|---|---|
| `text.primary` | `#431407` | Texto de maior destaque |
| `text.inverse` | `#FFFFFF` | Texto sobre superfícies escuras, quando houver contraste adequado |
| `border.default` | `#E7E5E4` | Bordas de inputs, cards e divisores |
| `surface.muted` | `#F5F5F4` | Áreas secundárias e backgrounds discretos |
| `brand.primaryHover` | `#C2410C` | Hover no botão primário web |
| `brand.primaryPressed` | `#9A3412` | Estado pressionado |
| `status.warning` | `#B45309` | Avisos e revisão pendente |
| `status.error` | `#B91C1C` | Falhas, ações destrutivas e validação |
| `focus.ring` | `#9A3412` | Contorno de foco visível |

**Acessibilidade:** não assumir que toda combinação de cores tem contraste suficiente. Para textos normais, buscar razão mínima de **4,5:1**; para texto grande, **3:1**; para indicadores visuais relevantes e limites de componentes, **3:1**. Validar as combinações reais em testes. Não depender só da cor para indicar status.

### 3.3 Regras de aplicação

- **60–70%:** superfícies claras (`#FFF7ED`, `#FFFFFF`).
- **20–30%:** conteúdo e elementos estruturais (`#431407`, `#57534E`).
- **Até ~10%:** destaque visual (`#EA580C`), salvo elementos de gravação que merecem maior ênfase.
- Verde apenas para **sucesso/conclusão**; não usá-lo como segundo botão principal.
- Mensagens de erro usam vermelho com ícone e texto descritivo.

As proporções são orientativas, não limites rígidos.

## 4. Tipografia

**Fonte sugerida:** **Inter** para web e mobile, com fallback para a fonte nativa do sistema. Priorizar legibilidade em telas pequenas.

| Estilo | Mobile | Web | Peso | Uso |
|---|---|---|---|---|
| `display` | 28/36 | 36/44 | 700 | Títulos de páginas de destaque |
| `heading.lg` | 24/32 | 28/36 | 700 | Títulos de telas |
| `heading.md` | 20/28 | 22/30 | 600 | Seções |
| `heading.sm` | 16/24 | 18/26 | 600 | Títulos de cards |
| `body` | 16/24 | 16/24 | 400 | Texto principal |
| `body.sm` | 14/20 | 14/20 | 400 | Texto de apoio |
| `caption` | 12/16 | 12/16 | 500 | Metadados curtos |
| `button` | 16/24 | 14/20 ou 16/24 | 600 | Ações |

Formato `tamanho/altura de linha`, em pixels lógicos (mobile: dp; web: px/rem equivalentes). Respeitar ampliação de texto e configurações de acessibilidade do sistema.

## 5. Espaçamento, cantos e elevação

Usar base de **4 unidades** para evitar medidas aleatórias.

| Token | Valor | Exemplo |
|---|---|---|
| `space.1` | 4 | Ícone e texto muito próximos |
| `space.2` | 8 | Elementos internos de um campo |
| `space.3` | 12 | Lacunas compactas |
| `space.4` | 16 | Padding padrão de cards e telas mobile |
| `space.5` | 20 | Agrupamentos |
| `space.6` | 24 | Distância entre seções |
| `space.8` | 32 | Respiro entre blocos principais |
| `space.12` | 48 | Seções maiores na web |

**Raios:** `radius.sm = 8`, `radius.md = 12`, `radius.lg = 16`, `radius.xl = 24`, `radius.pill = 9999`.

**Sombras:** sutis e usadas apenas quando necessárias para distinguir camadas; preferir bordas claras em cards padrão. Não simular profundidade excessiva.

## 6. Layout responsivo

### Mobile

- Layout mobile-first, predominantemente uma coluna.
- Padding lateral padrão: **16 px lógicos**; aumentar para **20–24** em telas largas.
- Ação de **gravar áudio** com grande área de toque e posição evidente.
- Barra inferior para as áreas mais acessadas, se a navegação justificar: **Início**, **Ordens**, **Gravar**, **Perfil**.
- Considerar safe areas, teclado virtual, estados de permissão e acessibilidade dos dispositivos.
- Alvos interativos: preferir pelo menos **44 × 44 pt** (iOS) ou **48 × 48 dp** (Android).

### Web

- Dashboard com sidebar em telas largas e menu adaptativo em telas menores.
- Largura útil máxima sugerida: **1440 px**; padding interno **24–32 px** em desktop.
- Grades para cards de indicadores; tabela de ordens com filtros e busca.
- Quebras iniciais de referência: `< 640 px` (pequena), `640–1023 px` (intermediária) e `≥ 1024 px` (desktop). Ajustar conforme conteúdo real, não apenas dispositivos.

## 7. Biblioteca de componentes

| Componente | Variantes/estados | Regras de uso |
|---|---|---|
| `Button` | primary, secondary, ghost, destructive; default, hover, pressed, disabled, loading | Primário laranja; apenas uma ação principal por região |
| `IconButton` | default, active, disabled | Ícone com rótulo acessível |
| `TextField` | normal, focused, error, disabled | Rótulo persistente, descrição e erro claro |
| `TextArea` | normal, error, disabled | Descrição detalhada da ordem |
| `Select` | normal, focused, error | Prioridade, responsável e categoria |
| `Card` | default, interactive | Resumo de ordem, métricas e informações |
| `StatusBadge` | draft, processing, review, open, in_progress, completed, canceled, failed | Sempre apresentar texto além da cor |
| `AudioRecorder` | idle, requesting_permission, recording, paused, uploading, processing, error | Tempo, estado, botão de parar e feedback evidentes |
| `WorkOrderCard` | compact, detailed | Identificador, título, prioridade, status e data |
| `Dialog` / `BottomSheet` | confirm, form, destructive | Diálogo na web; bottom sheet quando apropriado no mobile |
| `Toast` / `Alert` | info, success, warning, error | Feedback conciso, recuperável quando for erro |
| `Skeleton` / `EmptyState` | loading, no_data, no_results | Substituir telas sem conteúdo ou em carregamento |

**Padrão para botões:** não colocar texto branco em laranja sem validar o contraste. Para `#EA580C`, usar preferencialmente texto marrom muito escuro (`#431407`) ou adotar um tom mais escuro do laranja para botões com texto branco, após testes de contraste.

## 8. Fluxos de experiência (UX)

### 8.1 Fluxo principal de áudio → ordem de serviço

1. Usuário toca em **Gravar áudio**.
2. App solicita permissão de microfone quando necessário.
3. A tela mostra gravação ativa, cronômetro e controles claros.
4. Usuário encerra a gravação e revisa o áudio, se desejar.
5. App envia o arquivo e mostra progresso de upload.
6. API processa transcrição e estruturação por IA.
7. App mostra uma **prévia editável** com campos extraídos (cliente, descrição, endereço, prioridade etc.).
8. Usuário corrige as informações e confirma a criação da ordem.
9. Uma mensagem confirma o salvamento e oferece acesso à ordem.

**Regra essencial:** dados extraídos por IA devem ser revisáveis; não tratar inferências incertas como fatos confirmados. Mostrar campos ausentes ou incertos explicitamente.

### 8.2 Telas mobile essenciais

| Tela | Conteúdo prioritário | Ação principal |
|---|---|---|
| Início | Resumo de ordens recentes e pendências | Gravar áudio |
| Gravação | Estado do microfone, duração e controles | Iniciar/parar |
| Processamento | Etapas e progresso disponível | Aguardar / voltar |
| Revisar ordem | Campos sugeridos, transcrição de apoio | Criar ordem |
| Lista de ordens | Busca, filtros e status | Abrir ordem |
| Detalhe da ordem | Dados, histórico e atualização | Atualizar status |
| Perfil/Configurações | Conta, preferências e permissões | Salvar ajustes |

### 8.3 Telas web essenciais

| Tela | Conteúdo prioritário |
|---|---|
| Dashboard | Resumo de ordens, pendências, concluídas e atividade recente |
| Ordens de serviço | Tabela com pesquisa, filtro, ordenação e paginação |
| Detalhe da ordem | Dados, responsáveis, alterações e acompanhamento |
| Equipe | Usuários e responsáveis, conforme permissões disponíveis |
| Configurações | Perfil, organização e parâmetros operacionais |

## 9. Estados de ordens e linguagem visual

Os estados abaixo são uma **proposta de produto**, sujeita a refinamento conforme as regras de negócio.

| Estado | Rótulo na interface | Apresentação recomendada |
|---|---|---|
| `draft` | Rascunho | Cinza neutro |
| `processing` | Processando | Neutro + indicador de progresso |
| `review` | Aguardando revisão | Âmbar + ícone |
| `open` | Aberta | Neutro com destaque discreto |
| `in_progress` | Em andamento | Ênfase contextual + texto |
| `completed` | Concluída | Verde `#15803D` + ícone de confirmação |
| `canceled` | Cancelada | Cinza + indicação textual |
| `failed` | Falha no processamento | Vermelho + ação de tentar novamente |

Nunca comunicar status exclusivamente pela cor.

## 10. Ícones, imagens e movimento

- Preferir ícones lineares com traço coerente; exemplo de biblioteca: **Lucide** na web e equivalente no mobile.
- Tamanhos usuais: 16, 20 e 24 px lógicos.
- Usar o castor em onboarding, tela vazia e comunicação da marca, sem prejudicar o foco na tarefa.
- Microinterações discretas (aproximadamente **150–250 ms**), com suporte a preferência por movimento reduzido.
- Durante gravação, usar movimento com parcimônia, oferecendo também indicador textual visível.

## 11. Acessibilidade e usabilidade

- Contraste validado para textos, ícones e controles.
- Estados de foco destacados na web e navegação completa por teclado.
- Labels acessíveis, mensagens de erro associadas aos respectivos campos e anúncios adequados para leitores de tela.
- Conteúdos importantes disponíveis sem depender exclusivamente de áudio, cor ou animação.
- Áreas de toque confortáveis e suporte à ampliação de fonte.
- Mensagens de sistema acionáveis: explicar o que aconteceu e como resolver.
- Pedir permissão de microfone no momento em que seu uso fizer sentido; permitir saída do fluxo caso seja negada.

## 12. Tokens de implementação

A mesma **nomenclatura** de tokens deve existir nas duas interfaces. Como o repositório não usa Workspaces, manter tokens equivalentes em cada app e sincronizá-los por revisão, ou automatizar essa sincronização posteriormente.

### Web — exemplo CSS

```css
:root {
  --color-brand-primary: #EA580C;
  --color-brand-dark: #431407;
  --color-canvas: #FFF7ED;
  --color-card: #FFFFFF;
  --color-text-secondary: #57534E;
  --color-success: #15803D;
  --color-border: #E7E5E4;
  --color-error: #B91C1C;
  --radius-card: 16px;
  --space-page: 24px;
}
```

### Mobile — exemplo TypeScript

```ts
export const colors = {
  brand: { primary: '#EA580C', dark: '#431407' },
  surface: { canvas: '#FFF7ED', card: '#FFFFFF' },
  text: { primary: '#431407', secondary: '#57534E' },
  status: { success: '#15803D', error: '#B91C1C' },
  border: { default: '#E7E5E4' },
} as const;

export const spacing = {
  1: 4, 2: 8, 3: 12, 4: 16, 5: 20, 6: 24, 8: 32, 12: 48,
} as const;
```

### Organização recomendada dos arquivos de tema

```text
apps/
├── mobile/
│   └── src/theme/
│       ├── colors.ts
│       ├── typography.ts
│       ├── spacing.ts
│       └── radius.ts
└── web/
    └── src/styles/
        ├── tokens.css
        └── globals.css
```

## 13. Critérios para aprovar uma tela

- [ ] Usa tokens de cor e tipografia em vez de valores aleatórios.
- [ ] Possui hierarquia clara e uma ação principal identificável.
- [ ] Exibe estados de loading, vazio, sucesso e erro quando aplicáveis.
- [ ] Adapta-se aos tamanhos de tela previstos.
- [ ] Funciona com navegação por teclado (web) e leitor de tela.
- [ ] Tem contraste e áreas interativas adequadas.
- [ ] Usa textos curtos, compreensíveis e consistentes.
- [ ] Permite revisar dados sugeridos pela IA antes de confirmar.

## 14. Próximas decisões de design

1. Definir a arte final do mascote e testar legibilidade como ícone de aplicativo.
2. Validar pares de contraste dos botões, badges e campos.
3. Criar wireframes das telas de gravação, revisão e dashboard.
4. Consolidar componentes no Figma e implementar versões nativas de cada plataforma.
5. Definir futuramente a estratégia de tema escuro, sem presumir inversão automática da paleta.

---

**Fonte da identidade:** paleta e direção visual definidas para o Bivvo. Os demais tokens e padrões deste arquivo são recomendações iniciais para o produto.
