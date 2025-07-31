# **VCS Methodology Writing Guide**

## **1. Writing Style Requirements**

### **Tone & Voice**:
- ✅ **Present tense, active voice**: "VCS computes", "we use", "the algorithm selects"
- ✅ **Direct, technical tone**: No hedging ("may", "could", "potentially")
- ✅ **Objective, declarative**: State what the method does without justification
- ❌ **Avoid**: "We believe", "it seems", "arguably", "perhaps"

### **Person Usage**:
- ✅ **"We" for design decisions**: "We use NV-Embed-v2", "We define"
- ✅ **Third person for method actions**: "VCS computes", "the algorithm identifies"
- ✅ **Passive where appropriate**: "embeddings are extracted", "scores are normalized"

## **2. Structure & Organization**

### **Section Hierarchy**:
```
\paragraph{Component Name}
- Brief conceptual overview (1-2 sentences)
- Mathematical/algorithmic details
- Implementation specifics
- Connection to next component
```

### **Information Flow**:
1. **What it does** (function/purpose)
2. **How it works** (process/algorithm)  
3. **Technical details** (equations/parameters)
4. **Rationale** (why this approach)

### **Subsection Pattern**:
- **Input description**: "Given a [input type]..."
- **Process explanation**: Core computational steps
- **Output specification**: What is produced
- **Integration note**: How it connects to overall pipeline

## **3. Content Focus Guidelines**

### **Include**:
- ✅ **Implementation details**: Specific models, parameters, thresholds
- ✅ **Mathematical precision**: Formal notation, numbered equations
- ✅ **Technical specificity**: Model names, algorithmic choices
- ✅ **Computational steps**: Step-by-step process descriptions

### **Exclude**:
- ❌ **Extensive motivation**: Keep rationale brief and technical
- ❌ **Literature comparisons**: Save for Related Work
- ❌ **Experimental details**: Save for Experiments section
- ❌ **Implementation code**: Focus on algorithmic description

## **4. Mathematical & Notation Standards**

### **Equation Integration**:
- **Seamless flow**: Math should read naturally within sentences
- **Immediate context**: Introduce variables right before equations
- **Consistent notation**: Same symbols throughout (maintain symbol table)

### **Variable Conventions**:
- **Vectors**: Bold lowercase (𝐟, 𝐞)
- **Matrices**: Bold uppercase (𝐄, 𝐌)
- **Scalars**: Regular font (n, k, τ)
- **Sets**: Calligraphic when possible ({𝒞, 𝒮})

### **Equation Formatting**:
```latex
\begin{equation} \label{eq:descriptive_name}
Mathematical expression
\end{equation}
```

## **5. Key Phrase Patterns**

### **Process Introduction**:
- "Given a [input type] X, ..."
- "To enable [goal], VCS [action]..."
- "The [component] computes..."

### **Figure References**:
- "Figure X shows the [component] pipeline"
- "This process is illustrated in Figure X"
- "As shown in the upper/lower part of Figure X"

### **Algorithmic Explanation**:
- "By such [method], it is easy to [outcome]"
- "The algorithm identifies/selects/computes..."
- "This yields/produces/results in..."

### **Problem/Solution Transitions**:
- "To address [limitation], ..."
- "To remedy this, ..."
- "However, [issue] necessitates [solution]"

## **6. Section-Specific Guidelines**

### **Opening Section**:
- Start with high-level pipeline description
- Reference main figure
- Brief overview of three components
- No detailed technical content

### **Component Sections**:
- **Purpose statement**: What this component evaluates
- **Input specification**: What data it receives
- **Core algorithm**: Mathematical/computational process
- **Output description**: What scores/values it produces

### **Integration Sections**:
- **Combination logic**: How components are merged
- **Weighting schemes**: Mathematical aggregation
- **Final output**: Complete metric computation

## **7. Quality Checks**

### **Clarity Verification**:
- [ ] Can a technical reader implement from description?
- [ ] Are all variables defined before use?
- [ ] Is the computational flow clear?
- [ ] Are figure references accurate and helpful?

### **Consistency Checks**:
- [ ] Notation consistent throughout?
- [ ] Component names match introduction?
- [ ] Equation numbering sequential?
- [ ] Mathematical expressions properly formatted?
- [ ] **Terminology carries forward from previous paragraphs?**
- [ ] **Symbols and variables consistent with earlier definitions?**

### **Cross-Reference Requirements**:
- **ALWAYS review previous methodology paragraphs** before writing new sections
- **Reuse established notation**: $C_{ref}$, $C_{gen}$, $N_{ref}$, $N_{gen}$, $MW_{prec}$, $MW_{rec}$, etc.
- **Reference prior components**: "using the Mapping Windows defined above", "building on the chunk representations from Text Preprocessing"
- **Maintain component hierarchy**: GAS → Preprocessing → Mapping Windows → Best Matching → LAS → NAS

### **Completeness Validation**:
- [ ] All algorithmic steps covered?
- [ ] Parameters and thresholds specified?
- [ ] Edge cases addressed?
- [ ] Integration logic explained?

## **8. Common Pitfalls to Avoid**

### **Writing Issues**:
- ❌ **Mixing tenses**: Stay in present tense
- ❌ **Informal language**: Avoid contractions, colloquialisms
- ❌ **Redundant explanations**: Don't repeat information
- ❌ **Vague descriptions**: Be specific about computations

### **Technical Issues**:
- ❌ **Undefined variables**: Define all mathematical symbols
- ❌ **Missing parameters**: Specify all threshold values
- ❌ **Incomplete algorithms**: Cover all computational steps
- ❌ **Broken references**: Ensure figure/equation citations work

---

**Usage Instructions**: Reference specific sections when writing (e.g., "Apply Section 5 phrase patterns" or "Follow Section 2 structure guidelines") to maintain consistency with this established style.