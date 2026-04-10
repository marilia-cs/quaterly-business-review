# 📊 QBR Template

Template profissional de **Quarterly Business Review (QBR)** desenvolvido para Customer Success Managers, com foco em demonstração de valor, saúde da conta e alinhamento estratégico.

> Gerado programaticamente com [PptxGenJS](https://gitbrent.github.io/PptxGenJS/). Totalmente customizável via código JavaScript.

---

## O que está incluído

O template cobre **11 slides** estruturados com base nas boas práticas atuais de QBR para times de Customer Success:

| # | Slide | Conteúdo |
|---|-------|----------|
| 1 | **Capa** | Nome do cliente, trimestre, CSM e data |
| 2 | **Agenda** | Pauta da reunião + informações do encontro |
| 3 | **Resumo Executivo** | 4 KPIs principais + destaque e ponto de atenção |
| 4 | **Resultados vs. Metas** | Comparativo meta × realizado por indicador |
| 5 | **Evolução dos Indicadores** | Gráfico de adoção + métricas operacionais |
| 6 | **Marcos & Conquistas** | Timeline do trimestre + estatísticas resumidas |
| 7 | **Saúde da Conta** | Health score por indicador + breakdown do NPS |
| 8 | **Valor Entregue / ROI** | Impacto financeiro + citação do cliente |
| 9 | **Roadmap & Novidades** | Próximas funcionalidades + solicitações do cliente |
| 10 | **Plano de Ação** | Tabela de ações, responsáveis, prazos e status |
| 11 | **Fechamento** | Encerramento com informações de contato |

---

## 🎨 Design

- Paleta **navy + dourado** — profissional e legível em qualquer projetor
- Slides escuros para capa e fechamento; slides claros para conteúdo
- Ícones via [react-icons](https://react-icons.github.io/react-icons/) + rasterização com [sharp](https://sharp.pixelplumbing.com/)
- Badges de status coloridos (verde / âmbar / vermelho)
- Gráfico de linha para evolução temporal de adoção

---

## 🚀 Como usar

### Pré-requisitos

- [Node.js](https://nodejs.org/) 18+
- npm

### Instalação

```bash
git clone https://github.com/seu-usuario/qbr-template-csm.git
cd qbr-template-csm
npm install
```

### Gerar o template em branco

```bash
node qbr_template.js
# Saída: QBR_Template_CSM.pptx
```

### Gerar com dados de exemplo

```bash
node qbr_exemplo.js
# Saída: QBR_Q1_2026_Exemplo.pptx
```

---

## ✏️ Como personalizar

Abra o arquivo `qbr_template.js` (ou `qbr_exemplo.js`) e edite as seções marcadas:

```js
// ── DADOS DO CLIENTE ──────────────────────────────────
const CLIENTE = "Néctar Distribuidora";
const TRIMESTRE = "Q2 · 2026";
const DATA = "10 de julho de 2026";
const CSM = "Marília Gomes";

// ── KPIs (Slide 3) ────────────────────────────────────
const kpis = [
  { label: "MRR ATUAL",      value: "R$ 28.400", delta: "↑ 5,2% vs Q1" },
  { label: "NPS",            value: "62",         delta: "↑ 8 pts vs Q1" },
  { label: "TAXA DE ADOÇÃO", value: "78%",        delta: "↑ 12pp vs Q1"  },
  { label: "TICKETS ABERTOS",value: "3",          delta: "14 resolvidos"  },
];
```

---

## 📐 Estrutura do projeto

```
qbr-template-csm/
├── qbr_template.js       # Template em branco (placeholders)
├── qbr_exemplo.js        # Exemplo preenchido com dados fictícios
├── package.json
└── README.md
```

---

## 🧠 Por que este template?

A maioria dos templates de QBR disponíveis foca apenas em métricas de uso e não conecta os dados ao impacto no negócio do cliente. Este template foi estruturado para cobrir o que realmente importa em uma QBR estratégica de CS:

- **Resultados vs. Metas** — porque mostrar números sem contexto de expectativa não gera accountability
- **Valor Entregue / ROI** — porque renovação e expansão dependem de valor percebido, não de volume de features
- **Roadmap** — porque mostrar que a voz do cliente influencia o produto é uma das melhores ferramentas de retenção

---

## 📦 Dependências

| Pacote | Uso |
|--------|-----|
| `pptxgenjs` | Geração do arquivo `.pptx` |
| `react` + `react-dom` | Renderização de ícones SVG |
| `react-icons` | Biblioteca de ícones (Font Awesome via `fi`) |
| `sharp` | Conversão de SVG para PNG |

---

## 📄 Licença

MIT — livre para uso pessoal e comercial.

---

Desenvolvido por [Marília Gomes](mailto:marilia.agms@gmail.com) · Customer Success Manager
