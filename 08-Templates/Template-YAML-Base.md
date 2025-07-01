---
title: "Template YAML Base"
aliases:
  - "YAML Template"
  - "Metadata Template"
  - "Frontmatter Base"
tags:
  - type/template
  - theme/metadata
  - theme/yaml
  - status/active
  - component/foundation
type: "template"
status: "active"
dg-publish: true
dg-created: 2025-01-01 08:00
date_created: 2025-01-01 08:00
date_modified: 2025-01-01 12:00
project: "TCC-2025"
template_for: "all-notes"
parent: "Templates"
hierarchy_level: "3 - Template Foundation"
usage: "Base YAML structure for all vault notes"
version: "3.0.0"
---

# ⚙️ Template YAML Base

> **Metadata foundation para todo o vault**  
> **Estrutura**: YAML padronizado Digital Garden  
> **Uso**: Base para criação de qualquer nota

> [!abstract]+ **YAML FOUNDATION SYSTEM**
> Template foundational para metadata YAML de todas as notas do vault. Garante consistência, searchability e compatibilidade total com Digital Garden publishing.

## 🎯 **YAML STRUCTURE COMPLETE**

### 📋 **Universal YAML Template**

```yaml
---
# === BASIC IDENTIFICATION ===
title: "{{Note Title}}"
aliases:
  - "{{Alternative Name 1}}"
  - "{{Alternative Name 2}}"
  - "{{Alternative Name 3}}"

# === TAG TAXONOMY ===
tags:
  - type/{{note-type}}           # dashboard, canvas-note, experiment, project, etc.
  - theme/{{main-theme}}         # tcc, doe-llm, multi-agent, roi, etc.
  - theme/{{sub-theme}}          # Optional: specific sub-categorization
  - status/{{current-status}}    # active, completed, archived, draft
  - {{context-tag}}              # discovery/, method/, evidence/, impact/, presentation/

# === TYPE & STATUS ===
type: "{{note-type}}"            # Matches type/ tag
status: "{{status}}"             # Matches status/ tag

# === DIGITAL GARDEN SETTINGS ===
dg-publish: true                 # true for public, false for private
dg-created: {{date:YYYY-MM-DD HH:mm}}
dg-home: false                   # true only for main index
dg-pinned: false                 # true for pinned navigation

# === TEMPORAL DATA ===
date_created: {{date:YYYY-MM-DD HH:mm}}
date_modified: {{date:YYYY-MM-DD HH:mm}}
date: {{date:YYYY-MM-DD}}        # Optional: for daily notes

# === PROJECT CONTEXT ===
project: "TCC-2025"
sprint: "Sprint {{number}}"      # Current sprint/phase
source: "{{Source Description}}" # Where content originated

# === HIERARCHY & NAVIGATION ===
parent: "{{Parent Note}}"        # Direct parent in hierarchy
grandparent: "{{Grandparent}}"  # Optional: second level up
hierarchy_level: "{{Level}} - {{Description}}" # Navigation depth

# === CONTENT SPECIFIC (Choose relevant) ===
# For Experiments:
experiment_id: "{{ID}}"
model_tested: "{{LLM Model}}"
success_rate: "{{Percentage}}"
statistical_power: "{{Power}}"

# For Dashboards:
dashboard_type: "{{Type}}"
update_frequency: "{{Frequency}}"
coverage: "{{Scope}}"

# For Canvas Notes:
canvas_type: "{{Visualization Type}}"
complexity: "{{Simple/Medium/Complex}}"
connections: {{number}}

# For Projects:
project_phase: "{{Phase}}"
completion: "{{Percentage}}"
priority: "{{High/Medium/Low}}"

# === RELATIONSHIPS ===
topics:
  - "[[Topic 1]]"
  - "[[Topic 2]]"
  - "[[Topic 3]]"

related:
  - "[[Related Note 1]]"
  - "[[Related Note 2]]"

references:
  - "{{External Source 1}}"
  - "{{External Source 2}}"

# === METRICS (Optional) ===
word_count: {{number}}
read_time: "{{minutes}} min"
difficulty: "{{Beginner/Intermediate/Advanced}}"
confidence: "{{High/Medium/Low}}"

# === CUSTOM FIELDS (As Needed) ===
author: "{{Author Name}}"
reviewer: "{{Reviewer Name}}"
version: "{{Version Number}}"
language: "{{Language Code}}"
---
```

---

## 🔧 **FIELD SPECIFICATIONS**

> [!info]+ **Detailed Field Descriptions**

### 🎯 **Core Required Fields**
| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `title` | String | ✅ Yes | Human-readable note title |
| `tags` | Array | ✅ Yes | Minimum 4 tags (type, theme, status, context) |
| `type` | String | ✅ Yes | Primary note classification |
| `status` | String | ✅ Yes | Current lifecycle status |
| `dg-publish` | Boolean | ✅ Yes | Digital Garden publication flag |
| `date_created` | DateTime | ✅ Yes | ISO format creation timestamp |
| `project` | String | ✅ Yes | Project association |

### 🔍 **Classification Fields**
| Field | Values | Usage |
|-------|--------|-------|
| `type` | dashboard, canvas-note, experiment, daily-note, template | Primary categorization |
| `status` | active, completed, draft, archived, review | Lifecycle tracking |
| `hierarchy_level` | "0 - Home", "1 - Main", "2 - Detail", "3 - Support" | Navigation depth |
| `priority` | high, medium, low | Task/project prioritization |

### 🏷️ **Tag Taxonomy Standards**

#### **Type Tags (Required)**
- `type/dashboard` - Analytics and metrics displays
- `type/canvas-note` - Visual structure notes
- `type/experiment` - Scientific experiments and tests
- `type/daily-note` - Daily productivity tracking
- `type/template` - Reusable templates and patterns
- `type/project` - Project management and planning

#### **Theme Tags (Required)**
- `theme/tcc` - TCC project related content
- `theme/doe-llm` - Design of Experiments methodology
- `theme/multi-agent` - Multi-agent system architecture
- `theme/roi` - Return on investment and business metrics
- `theme/analytics` - Data analysis and insights
- `theme/productivity` - Personal productivity and workflow

#### **Status Tags (Required)**
- `status/active` - Currently being worked on
- `status/completed` - Finished and finalized
- `status/draft` - In progress, not final
- `status/archived` - Completed and stored
- `status/review` - Pending review or approval

#### **Context Tags (Scientific Method)**
- `discovery/` - New findings and breakthroughs
- `method/` - Methodologies and frameworks
- `evidence/` - Supporting data and validation
- `impact/` - Effects and consequences
- `presentation/` - Communication and reporting

---

## 📊 **TAG USAGE ANALYTICS**

> [!example]+ **Current Tag Distribution**

```dataview
TABLE 
  length(tags) as "Tag Count",
  type as "Type",
  status as "Status"
FROM "TCC_Apresentacao_Banca_2025"
WHERE tags
SORT length(tags) DESC
LIMIT 10
```

### 🎯 **Tag Quality Metrics**
- **Average Tags/Note**: 6-8 tags optimal
- **Required Coverage**: 100% type, theme, status
- **Context Tags**: 80%+ notes should have context tags
- **Consistency Score**: Measure tag standardization

---

## 🎯 **TEMPLATE VARIATIONS**

> [!note]+ **Specialized Templates by Type**

### 📊 **Dashboard YAML**
```yaml
---
title: "Dashboard {{Name}}"
tags: [type/dashboard, theme/{{domain}}, status/active]
type: "dashboard"
dg-publish: true
dashboard_type: "real-time analytics"
update_frequency: "auto-refresh"
coverage: "{{scope}}"
---
```

### 🔬 **Experiment YAML**
```yaml
---
title: "Experiment {{ID}}"
tags: [type/experiment, theme/doe-llm, status/completed, discovery/{{finding}}]
type: "experiment"
experiment_id: "{{unique-id}}"
model_tested: "{{llm-model}}"
success_rate: "{{percentage}}"
statistical_power: "{{power}}"
---
```

### 📝 **Daily Note YAML**
```yaml
---
title: "Daily Note - {{date}}"
tags: [type/daily-note, theme/productivity, date/{{date}}, status/active]
type: "daily-note"
date: {{date}}
mood: "{{mood}}"
energy_level: "{{energy}}"
sprint: "Sprint {{number}}"
---
```

### 🎨 **Canvas Note YAML**
```yaml
---
title: "Canvas {{Name}}"
tags: [type/canvas-note, theme/{{domain}}, status/active]
type: "canvas-note"
canvas_type: "structural visualization"
complexity: "{{level}}"
connections: {{number}}
visual_elements: {{count}}
---
```

---

## ⚡ **AUTOMATION & TOOLS**

> [!tip]+ **YAML Automation Setup**

### 🔧 **Templater Integration**
```javascript
// Auto-generate timestamps
dg-created: <% tp.date.now("YYYY-MM-DD HH:mm") %>
date_created: <% tp.date.now("YYYY-MM-DD HH:mm") %>
date_modified: <% tp.date.now("YYYY-MM-DD HH:mm") %>

// Auto-increment experiment IDs
experiment_id: <% tp.user.increment_experiment_id() %>

// Dynamic tag generation
tags: 
  - type/<% tp.user.note_type() %>
  - theme/<% tp.user.current_theme() %>
  - status/draft
```

### 🎯 **QuickAdd Macros**
- **New Dashboard**: Auto-populate dashboard-specific fields
- **New Experiment**: Generate experiment ID + baseline tags
- **New Daily Note**: Date-stamped with current sprint
- **New Canvas**: Visual structure template

### 📊 **Linter Configuration**
```yaml
# YAML Linter Rules
yaml-title: true
yaml-tags: enforce
yaml-dates: ISO-8601
yaml-booleans: lowercase
yaml-aliases: array-format
```

---

## 🔍 **QUALITY ASSURANCE**

> [!warning]+ **YAML Validation Checklist**

### ✅ **Pre-Publication Checklist**
- [ ] **Title**: Descriptive and unique
- [ ] **Tags**: Minimum 4 required tags present
- [ ] **Type**: Matches first type/ tag
- [ ] **Status**: Reflects current state
- [ ] **dg-publish**: Correctly set for intended audience
- [ ] **Dates**: Valid ISO format timestamps
- [ ] **Project**: Matches project naming convention
- [ ] **Hierarchy**: Parent/child relationships correct

### 🎯 **Common Errors & Fixes**
| Error | Fix |
|-------|-----|
| Missing type/ tag | Add appropriate type/{{category}} |
| Inconsistent status | Update both status field and status/ tag |
| Invalid date format | Use YYYY-MM-DD HH:mm format |
| Boolean as string | Use true/false, not "true"/"false" |
| Empty aliases | Remove aliases field or add meaningful alternatives |

---

## 📈 **METADATA ANALYTICS**

> [!abstract]+ **Vault Health Metrics**

### 📊 **Compliance Dashboard**
```dataview
TABLE 
  WITHOUT ID
  file.name as "Note",
  length(tags) as "Tag Count",
  type as "Type",
  status as "Status",
  choice(dg-publish, "✅ Public", "🔒 Private") as "Visibility"
FROM "TCC_Apresentacao_Banca_2025"
WHERE file.name != "Template-YAML-Base"
SORT length(tags) DESC
```

### 🎯 **Quality Indicators**
- **YAML Completeness**: % notes with all required fields
- **Tag Consistency**: % notes following tag taxonomy
- **Metadata Richness**: Average fields per note
- **Publication Readiness**: % notes marked dg-publish: true

---

## 🔗 **TEMPLATE SYSTEM NAVIGATION**

### **📝 Related Templates**
[[Template Daily Note]] | [[Template Experimento]] | [[Template Canvas Note]]

### **🎯 Template Guidelines**
[[YAML Best Practices]] | [[Tag Taxonomy Guide]] | [[Digital Garden Setup]]

### **📊 Vault Analytics** 
[[Vault Health Dashboard]] | [[Metadata Quality Report]] | [[Tag Usage Analytics]]

---

## 📋 **VERSION HISTORY**

### 🔄 **Template Evolution**
- **v1.0**: Basic YAML structure
- **v2.0**: Digital Garden compatibility
- **v3.0**: Scientific taxonomy + automation
- **v3.1**: Enhanced metadata richness

### 🎯 **Future Enhancements**
- [ ] Auto-validation hooks
- [ ] AI-generated tag suggestions
- [ ] Dynamic metadata fields
- [ ] Cross-vault compatibility

---

**Tags**: #template #yaml #metadata #foundation #type/template #theme/metadata #component/foundation #status/active

---
[[TCC Multi-Agent Systems - Digital Garden]] | [[Template Daily Note]] | [[Digital Garden Setup Guide]] 