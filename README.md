<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1F9BD4,50:2E75B6,100:16265F&height=200&section=header&text=Power%20BI%20Visualizações%20v2&fontSize=42&fontColor=ffffff&fontAlignY=38&desc=Segunda%20Versão%20—%20Dashboards%20Refinados%20e%20Documentados&descAlignY=58&descSize=18" width="100%"/>

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Microsoft](https://img.shields.io/badge/Microsoft-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)](https://microsoft.com/)
[![v2](https://img.shields.io/badge/versão-2.0-success?style=for-the-badge)](https://github.com/fassir)

[![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![DOCX](https://img.shields.io/badge/Documentação-DOCX-2B579A?style=flat-square&logo=microsoftword&logoColor=white)](https://microsoft.com/)
[![Refined](https://img.shields.io/badge/Dashboards-Refinados-blueviolet?style=flat-square)](https://github.com/fassir)

</div>

---

## 🎯 Sobre o Projeto

Segunda versão do projeto de adequação de visualizações no **Power BI**, com dashboards aprimorados, novos casos de uso e documentação técnica detalhada em formato `.docx`. Esta versão incorpora o feedback da primeira iteração e expande os padrões de qualidade com visualizações mais sofisticadas e melhor rastreabilidade documental.

---

## 🗂️ Estrutura do Repositório

```
power_bi_adequando_visualizações---2/
├── *.pbix                     # Dashboards Power BI refinados (v2)
└── documentacao_v2.docx       # Documentação técnica completa
```

---

## 🔄 Evolução da v1 para a v2

<div align="center">

| Aspecto | Versão 1 | Versão 2 |
|---------|----------|----------|
| Documentação | README + checklist Markdown | + Arquivo `.docx` estruturado |
| Dashboards | Adequação básica | Refinamento visual avançado |
| Paleta de cores | Consistente | Otimizada para acessibilidade |
| Interatividade | Filtros básicos | Bookmarks + drillthrough |
| Mobile | Não verificado | Layout responsivo validado |
| Tooltips | Padrão | Customizados e informativos |

</div>

---

## 💡 Tecnologias

<div align="center">

[![My Skills](https://skillicons.dev/icons?i=windows&theme=dark)](https://powerbi.microsoft.com/)

</div>

| Tecnologia | Uso |
|------------|-----|
| Power BI Desktop | Criação e refinamento dos dashboards |
| Power Query (M) | Transformações de dados avançadas |
| DAX | Medidas calculadas e inteligência de tempo |
| Microsoft Word (DOCX) | Documentação técnica do projeto |
| Power BI Service | Publicação e colaboração |

---

## 📄 Documentação (documentacao_v2.docx)

<details>
<summary><strong>📋 Estrutura do documento</strong></summary>

```
1. Introdução e objetivos do projeto
2. Fonte de dados e transformações aplicadas
3. Decisões de design por página
   3.1 Justificativa para cada tipo de gráfico
   3.2 Paleta de cores e critérios de acessibilidade
   3.3 Hierarquia visual e layout
4. Medidas DAX documentadas
5. Checklist de qualidade final
6. Comparativo antes × depois com capturas de tela
7. Lições aprendidas e próximos passos
```

</details>

---

## 🎨 Refinamentos Visuais da v2

<details>
<summary><strong>🖌️ Melhorias de design aplicadas</strong></summary>

```
Paleta de cores:
  Primária:   #1F9BD4 (azul Power BI)
  Secundária: #2E75B6 (azul escuro)
  Destaque:   #F2C811 (amarelo Power BI)
  Neutro:     #F5F5F5 / #333333

Tipografia:
  Títulos:    Segoe UI Semibold, 14-18pt
  Subtítulos: Segoe UI, 12pt
  Labels:     Segoe UI, 10pt (mín.)

Espaçamento:
  Margem externa:  16px
  Gap entre cards: 8px
  Padding interno: 12px
```

</details>

<details>
<summary><strong>⚡ Recursos de interatividade (v2)</strong></summary>

```
✅ Bookmarks para alternância de visualizações
✅ Drillthrough para análise detalhada por entidade
✅ Tooltips de página (relatórios contextuais ao hover)
✅ Botões de navegação entre páginas
✅ Segmentadores sincronizados entre páginas
✅ Estado de filtro visível para o usuário
✅ Botão "Limpar filtros" em cada página
```

</details>

---

## 📊 Boas Práticas DAX (v2)

<details>
<summary><strong>🔢 Medidas documentadas</strong></summary>

```dax
-- Variação percentual período anterior
Variação % = 
VAR atual = [Total Vendas]
VAR anterior = CALCULATE([Total Vendas], PREVIOUSMONTH(Calendario[Data]))
RETURN
    DIVIDE(atual - anterior, anterior, 0)

-- Ranking dinâmico
Ranking = 
RANKX(
    ALLSELECTED(Tabela[Categoria]),
    [Total Vendas],
    ,
    DESC,
    DENSE
)

-- Meta vs Realizado
% Atingimento Meta = 
DIVIDE([Total Vendas], [Meta], 0)
```

</details>

---

## ✅ Checklist de Qualidade Final (v2)

```
Visuais
 [x] Tipo de gráfico adequado ao dado em 100% dos visuais
 [x] Sem gráficos de pizza com mais de 5 fatias
 [x] Rótulos de dados visíveis nos principais KPIs

Acessibilidade
 [x] Contraste WCAG AA em todos os textos
 [x] Texto alternativo configurado em todos os visuais
 [x] Cores testadas em modo deuteranopia e protanopia

Performance
 [x] Tempo de carregamento < 3 segundos
 [x] Consultas DAX otimizadas (sem iteradores desnecessários)
 [x] Modelo estrela (star schema) aplicado

Documentação
 [x] Arquivo .docx gerado e revisado
 [x] Todas as medidas DAX documentadas
 [x] Decisões de design justificadas
```

---

## 🚀 Como Usar

1. **Baixe** os arquivos `.pbix` e `documentacao_v2.docx`
2. **Abra** o Power BI Desktop
3. **Carregue** o arquivo `.pbix`
4. **Leia** a documentação `.docx` para entender cada decisão de design
5. **Aplique** os padrões aos seus próprios projetos

```
Requisito: Power BI Desktop (versão mais recente)
Download: https://powerbi.microsoft.com/pt-br/desktop/
```

---

## 👤 Autor

<div align="center">

**Fabio Piassi**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/fabio-piassi)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/fassir)

</div>

---

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:16265F,50:2E75B6,100:1F9BD4&height=120&section=footer" width="100%"/>
