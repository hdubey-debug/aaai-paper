# **VCS Methodology Writing Guide**

## **1. Writing Style Requirements**

### **Tone & Voice**:
- ✅ **Present tense, active voice**: "VCS computes", "we use", "the algorithm selects"
- ✅ **Direct, technical tone**: No hedging ("may", "could", "potentially")
- ✅ **Explanatory cross-references**: "By such method, it is easy to...", "Note that X will not affect Y in Eq. (Z) since..."
- ✅ **"We" for design decisions**: "We use NV-Embed-v2", "We define", "We compute"
- ❌ **Avoid**: "We believe", "it seems", "arguably", "perhaps"

### **EMScore-Style Patterns**:
- **Limitation-driven transitions**: "only performing X may lose Y, which inspires us to design Z"
- **Motivational context**: "For these cases, it is hard to... thus we should..."
- **Problem-solution flow**: "Since X changes over time... we design Y"
- **Post-math explanations**: "By such matching in the calculation of precision, it is easy to figure out..."
- **Cross-reference notes**: "Note that weighting will not affect Eq. (6) since each element is equally important"

## **2. Structure: 6-Step Process (with Optional Step 0)**

### **Step 0. Context/Motivation (Optional)**:
- **When to use**: Novel concepts, transitions from limitations of previous components
- **Pattern**: "However, only performing X may lose Y, which inspires us to design Z"
- **Examples**: Moving from global to local alignment, introducing new algorithmic concepts

### **Step 1. Opening Statement**:
- **What it does/achieves**: "VCS computes [what] to [achieve what goal]"
- **Purpose-focused**: Start with the component's function

### **Step 2. Input Specification**:
- **Pattern**: "Given [inputs], we [initial action]"
- **Be specific**: List exact inputs from previous components

### **Step 3. Process Description**:
- **Step-by-step technical details**: "We first [step 1], then [step 2]"
- **Parameter specifications**: Include thresholds, methods, configurations

### **Step 4. Mathematical Formulation**:
- **Equations with proper labeling**: Use when specified (you'll decide case-by-case)
- **Variable definitions**: "where [var] is [definition]"

### **Step 5. Explanatory Analysis**:
- **What each part does conceptually**: "The precision evaluates..., while recall measures..."
- **Cross-reference insights**: "By such matching, it is easy to determine..."
- **Equation callbacks**: "Note that X does not affect Eq. (Y) since..."

### **Step 6. [Implicit Output]**:
- **Natural conclusion**: Final result emerges from context
- **No explicit "this produces"**: Let the output be implicit from the math and explanation

## **3. Cross-Reference Requirements**

### **Terminology Consistency**:
- **ALWAYS review previous methodology paragraphs** before writing new sections
- **Reuse established notation**: $C_{ref}$, $C_{gen}$, $N_{ref}$, $N_{gen}$, $MW_{prec}$, $MW_{rec}$, $\mathbf{E}_{C_{ref}}$, $\mathbf{E}_{C_{gen}}$
- **Reference prior components**: "using the Mapping Windows defined above", "from $\mathbf{E}_{C_{ref}}$ and $\mathbf{E}_{C_{gen}}$"
- **Maintain component hierarchy**: GAS → Preprocessing → Mapping Windows → Best Matching → LAS → NAS
- **Ensure backward compatibility**: New sections must use symbols/terminology established earlier

### **Component Transitions**:
- **Link limitations to solutions**: Each component should address limitations of previous ones
- **Build narrative flow**: "However, X cannot capture Y, which inspires us to..."
- **Reference figure parts**: "This process is shown in the upper part of Fig. X"

## **4. AAAI LaTeX Compliance**

### **Space Constraints**:
- **No overfull boxes**: Equations and text must not overflow column margins
- **Check log files**: Monitor for margin violations
- **Space efficiency**: Use concise mathematical notation

### **Equation vs. Inline Math**:
- **You will specify**: Case-by-case decision on what gets numbered equations vs. inline math
- **Inline for**: Simple definitions, parameters, set notation
- **Equations for**: Core formulas, complex calculations (when specified)

### **Font and Formatting**:
- **Use only approved fonts**: Avoid Type 3 fonts
- **Mathematics formatting**: Computer Modern acceptable for math only
- **Column constraints**: All content must fit within two-column format

## **5. Quality Checks**

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

### **EMScore-Style Flow**:
- [ ] **Contextual motivation** between components?
- [ ] **Explanatory analysis** after equations?
- [ ] **Cross-referencing** and equation callbacks?
- [ ] **Natural conclusion** without explicit output statements?

### **Completeness Validation**:
- [ ] All algorithmic steps covered?
- [ ] Parameters and thresholds specified?
- [ ] Edge cases addressed?
- [ ] Integration logic explained?

## **6. Common Pitfalls to Avoid**

### **Writing Issues**:
- ❌ **Mixing tenses**: Stay in present tense
- ❌ **Informal language**: Avoid contractions, colloquialisms
- ❌ **Explicit output statements**: Don't say "this produces" or "we output"
- ❌ **Missing transitions**: Each component should address previous limitations

### **Technical Issues**:
- ❌ **Undefined variables**: Define all mathematical symbols
- ❌ **Missing cross-references**: Include equation callbacks and explanatory notes
- ❌ **Broken narrative flow**: Ensure logical progression between components
- ❌ **Inconsistent notation**: Use established symbols throughout

---

**Usage Instructions**: Follow the 6-step process for each methodology section. Reference specific steps when writing (e.g., "Apply Step 5 explanatory analysis" or "Add Step 0 context for this transition") to maintain consistency with EMScore style while adapting to VCS needs.