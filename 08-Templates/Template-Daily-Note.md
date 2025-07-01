---
title: "Template Daily Note"
aliases:
  - "Template Nota Diária"
  - "Daily Note Template"
tags:
  - type/template
  - theme/productivity
  - theme/daily-workflow
  - status/active
  - component/template
type: "template"
status: "active"
dg-publish: true
dg-created: 2025-01-01 08:00
date_created: 2025-01-01 08:00
date_modified: 2025-01-01 12:00
project: "TCC-2025"
template_for: "daily-notes"
parent: "Templates"
hierarchy_level: "3 - Template Components"
usage: "Create standardized daily notes"
---

# 📝 Template Daily Note

> **Template padronizado para notas diárias**  
> **Estrutura**: Produtividade + reflexão + tracking  
> **Uso**: Copiar estrutura para novas daily notes

> [!abstract]+ **TEMPLATE OVERVIEW**
> Template completo para criação de daily notes padronizadas no vault TCC. Inclui seções para priorities, progress tracking, learning, reflection and navigation.

## 🎯 **TEMPLATE STRUCTURE**

### �� **YAML Frontmatter Template**
```yaml
---
title: "Daily Note - {{date:YYYY-MM-DD}}"
aliases:
  - "{{date:DD MMMM YYYY}}"
  - "{{date:dddd}}"
tags:
  - type/daily-note
  - theme/tcc
  - theme/sprint{{sprint-number}}
  - date/{{date:YYYY-MM-DD}}
  - status/active
type: "daily-note"
status: "active"
dg-publish: true
dg-created: {{date:YYYY-MM-DD HH:mm}}
date: {{date:YYYY-MM-DD}}
date_created: {{date:YYYY-MM-DD HH:mm}}
date_modified: {{date:YYYY-MM-DD HH:mm}}
project: "TCC-2025"
sprint: "Sprint {{sprint-number}}"
week_number: {{week-number}}
mood: "{{mood}}"
energy_level: "{{energy}}"
---
```

### 🏗️ **Content Structure Template**

```markdown
# 📅 Daily Note - {{date:YYYY-MM-DD}}

> **{{Custom Description}}**  
> **Focus**: {{today-focus}}  
> **Mood**: {{mood-emoji}} {{mood}} | **Energy**: {{energy-emoji}} {{energy}}

> [!abstract]+ **DAILY SUMMARY**
> {{Brief summary of the day's focus and main activities}}

## 🎯 **TODAY'S PRIORITIES**

> [!warning]+ **Critical Actions - {{Sprint/Project}}}**
> - [ ] 🎯 Priority 1 - {{description}}
> - [ ] 📊 Priority 2 - {{description}}  
> - [ ] 🔬 Priority 3 - {{description}}
> - [ ] 💡 Priority 4 - {{description}}

## ⚡ **{{PROJECT}} STATUS UPDATE**

### 🏆 **Conquistas Hoje**
1. **Achievement 1**: {{description}}
2. **Achievement 2**: {{description}}
3. **Achievement 3**: {{description}}

### 📊 **Métricas do Dia**
- **{{Metric 1}}**: {{value}}
- **{{Metric 2}}**: {{value}}
- **{{Metric 3}}**: {{value}}
- **{{Metric 4}}**: {{value}}

---

## 🔬 **RESEARCH & DISCOVERIES**

> [!discovery]+ **Insights do Dia**
> {{Key insights and discoveries from today's work}}

### 💡 **Key Insights**
- **Insight 1**: {{description}}
- **Insight 2**: {{description}}
- **Insight 3**: {{description}}

---

## 📚 **LEARNING & DEVELOPMENT**

### 🎓 **Skills Desenvolvidas**
- **Skill 1**: {{description}}
- **Skill 2**: {{description}}
- **Skill 3**: {{description}}

### 📖 **Resources Consultados**
- [[Resource 1]] - {{description}}
- [[Resource 2]] - {{description}}
- {{External resource}} - {{description}}

---

## 🔄 **WORKFLOW OPTIMIZATION**

> [!method]+ **Process Improvements**

### ⚡ **Efficiency Gains**
- {{Process improvement 1}}
- {{Process improvement 2}}
- {{Process improvement 3}}

### 🎯 **Template/System Updates**
- {{System update 1}}
- {{System update 2}}

---

## 🤝 **COLLABORATION & COMMUNICATION**

### 👥 **Team Interactions**
- **{{Person/Role}}**: {{interaction description}}
- **{{Person/Role}}**: {{interaction description}}

### 📢 **Communications**
- **{{Communication type}}**: {{description}}
- **{{Communication type}}**: {{description}}

---

## 🎯 **TOMORROW'S PRIORITIES**

### 🚀 **Immediate Actions**
- [ ] {{Tomorrow priority 1}}
- [ ] {{Tomorrow priority 2}}
- [ ] {{Tomorrow priority 3}}

### 📈 **Strategic Focus**
- [ ] {{Strategic item 1}}
- [ ] {{Strategic item 2}}
- [ ] {{Strategic item 3}}

---

## 📊 **METRICS & ANALYTICS**

### 📈 **Daily Performance**
- **Hours Worked**: {{hours}}h {{type}} time
- **Tasks Completed**: {{completed}}/{{total}} items ({{percentage}}%)
- **Quality Level**: {{quality description}}
- **Energy Management**: {{energy assessment}}

### 🎯 **Progress Indicators**
- **{{Project/Sprint}}**: {{progress}} ({{direction}})
- **{{Metric 2}}**: {{value}} ({{change}})
- **{{Metric 3}}**: {{status}}
- **Morale**: {{mood level}}

---

## 🧠 **REFLECTION & INSIGHTS**

> [!tip]+ **Daily Reflection**

### 💭 **What Went Well**
- {{Success 1}}
- {{Success 2}}
- {{Success 3}}

### 🎯 **What Could Improve**
- {{Improvement area 1}}
- {{Improvement area 2}}

### 📝 **Lessons Learned**
- {{Lesson 1}}
- {{Lesson 2}}
- {{Lesson 3}}

---

## 🔗 **TODAY'S NAVIGATION**

### **📊 Created/Updated Today**
[[Note 1]] | [[Note 2]] | [[Note 3]]

### **🎯 Focus Areas**
[[Focus Area 1]] | [[Focus Area 2]] | [[Focus Area 3]]

### **🚀 Tomorrow's Focus**
[[Tomorrow Item 1]] | [[Tomorrow Item 2]] | [[Tomorrow Item 3]]

---

## 🏷️ **TAGS & CONNECTIONS**

**Daily Tags**: #{{tag1}} #{{tag2}} #{{tag3}} #{{tag4}}

**Connected Notes**: 
- [[Template Daily Note]] - Template source
- [[{{Main Project}}]] - Project tracking
- [[{{Sprint/Phase}}]] - Current phase
- [[{{Project Home}}]] - Project home

---

## 📋 **DAILY METADATA**

- **Weather**: {{weather emoji}} {{weather description}}
- **Energy Peak**: {{peak time}} ({{productivity description}})
- **Deep Work Hours**: {{hours}}h {{work type}}
- **Interruptions**: {{interruption level}}
- **Satisfaction Level**: {{rating}}/10 ({{description}})
- **Tomorrow Prep**: {{preparation status}}

---

**Navigation**: [[Yesterday]] ← **Today** → [[Tomorrow]] | [[Weekly Review]] | [[Monthly Goals]]

**Tags**: #daily-note #{{project}} #{{sprint}} #{{theme}} #type/daily-note #theme/productivity #status/{{status}} #date/{{date}}

---
[[{{Project Home}}]] | [[{{Sprint Status}}]] | [[Template Daily Note]]
```

---

## 🎯 **USAGE INSTRUCTIONS**

> [!info]+ **Como Usar Este Template**

### 📋 **Daily Creation Process**
1. **Copy Template**: Copiar estrutura acima
2. **Replace Placeholders**: Substituir {{variables}} por valores reais
3. **Customize Sections**: Adaptar seções conforme necessidade do dia
4. **Update YAML**: Aplicar metadata correto
5. **Link Navigation**: Conectar com outras notas relevantes

### 🔧 **Customization Options**
- **Project Focus**: Adaptar seções para projeto específico
- **Sprint Context**: Personalizar para fase atual
- **Mood Tracking**: Usar emojis e descriptions consistentes
- **Metrics**: Definir KPIs relevantes para tracking

### ⚡ **Automation Potential**
- **Templater Plugin**: Auto-fill dates e basic info
- **QuickAdd**: Criar daily notes via hotkey
- **Calendar Plugin**: Visualização temporal
- **Dataview**: Queries automáticas para analytics

---

## 📊 **TEMPLATE ANALYTICS**

### 📈 **Usage Metrics**
- **Template Version**: 3.0.0 (Digital Garden optimized)
- **Sections Count**: 12 main sections
- **Estimated Fill Time**: 15-25 minutes
- **Maintenance Level**: Low (stable structure)

### 🎯 **Effectiveness Indicators**
- **Daily Completion Rate**: Target 80%+
- **Reflection Quality**: Detailed insights
- **Progress Tracking**: Quantified metrics
- **Navigation Usage**: Active linking

---

## 🔗 **TEMPLATE NAVIGATION**

### **📝 Related Templates**
[[Template YAML Base]] | [[Template Experimento]] | [[Template Projeto]]

### **🎯 Template System**
[[Template Daily Note]] | [[Template Weekly Review]] | [[Template Monthly Goals]]

### **📊 Template Analytics**
[[Template Usage Stats]] | [[Template Effectiveness]] | [[Template Evolution]]

---

**Tags**: #template #daily-note #productivity #structure #type/template #theme/productivity #component/template #status/active

---
[[TCC Multi-Agent Systems - Digital Garden]] | [[Template YAML Base]] | [[Daily Note Examples]] 