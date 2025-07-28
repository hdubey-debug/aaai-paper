# **VCS Paper Terminology & Phrase Guide**

## **1. Core Evaluation Terminology**

### **Evaluation Dimensions** (use consistently):
- **Global thematic alignment** (global level evaluation)
- **Local semantic alignment** (local level evaluation)  
- **Chronological alignment** (temporal level evaluation)

### **NEVER use these alternatives**:
- ❌ thematic coherence/similarity/consistency
- ❌ semantic accuracy/correspondence/consistency
- ❌ chronological consistency/coherence/accuracy

### **Requirements Phrasing**:
An effective evaluation metric for long-form descriptions must:
- (i) assess **global thematic alignment**
- (ii) measure **local semantic alignment** 
- (iii) evaluate **chronological alignment** while detecting corrupted content

## **2. Description Type Terminology**

### **Always Use**:
- ✅ **"long-form descriptions"** (matches title)
- ✅ **"short-form descriptions"** (consistent naming)

### **NEVER use**:
- ❌ long descriptions, dense descriptions, extended descriptions, extended narratives
- ❌ short captions, short-form captions, shorter captions, brief captions

## **3. Experimental Terminology**

### **Test Sets**:
- **Corruption Detection Test Set** (for corruption detection)
- **Cross-Author Consistency Test Set** (for reference robustness)

### **Corruption Detection Categories**:
- ✅ **Valid variations**: paraphrasing, brevity, synonym replacement
- ✅ **Invalid corruptions**: hallucinations, content removal

### **Phrasing**:
- "distinguishing **valid variations** from **invalid corruptions**"
- NOT: "valid corruptions" or "invalid variations"

## **4. VCS Variants**

### **Naming**:
- **VCS** (for long-form descriptions)
- **VCS$_{\text{short}}$** (for short-form descriptions)

### **Phrasing**:
- "VCS$_{\text{short}}$, our implementation for short-form descriptions"
- NOT: "for short captions" or "short-form implementation"

### **Important Linguistic Rules**:
- VCS **produces/demonstrates/shows** scores (not "achieves" - VCS IS the score)
- Use "metric" not "metrics" (singular)

---

**Usage Instructions**: When prompting me for future edits, reference specific sections of this guide (e.g., "Use Section 1 evaluation terminology" or "Apply Section 3 experimental phrasing") to ensure consistency.