# Instance-Based Learning vs Model-Based Learning

This is a classification of ML algorithms based on **how a model generalizes from training data** — i.e., *how it learns*, as opposed to earlier classifications based on the amount of supervision required.

---

## Example Dataset (used throughout)

A student placement dataset:

| Column | Meaning |
|---|---|
| IQ | Feature |
| CGPA | Feature |
| Placement | Target (Yes/No) — classification problem |

Goal: given a new student's IQ and CGPA, predict whether they'll get placed.

---

## 1. Instance-Based Learning (a.k.a. Lazy Learning / Memory-Based Learning)

**Core idea:** Just memorize the training data. Don't try to find any underlying pattern.

### How it works (KNN-style example)
1. Plot all training points (placed vs not placed) in feature space (IQ vs CGPA).
2. When a **new query point** arrives:
   - Calculate the **distance** of the new point from every other point.
   - Pick the **k nearest neighbors**.
   - Take a **majority vote** among those neighbors to decide the class (e.g., if 2 of 3 nearest neighbors are "placed," predict "placed").
3. During training, the algorithm does essentially nothing — it just stores the data ("quietly sits with the data"). All the real work happens **at prediction time**.

### Key characteristics
- No mathematical model or rule is learned in advance.
- Training data must be **kept around forever**, since prediction depends directly on it.
- Prediction is made relative to the specific new point — the "rule" isn't fixed, it depends on which point comes in.
- **Generalization happens only when a new query point arrives** — there's no rule/pattern extracted beforehand. This is why it's also called **"lazy learning."**
- During training, the algorithm is essentially idle ("sits quietly with the data") — no computation/learning happens until prediction time.
- Classic example algorithm: **K-Nearest Neighbors (KNN)**.
- Other examples: **RBF Networks, Kernel-based methods**.

---

## 2. Model-Based Learning

**Core idea:** During training, extract an **underlying pattern/rule** (a mathematical function) from the data instead of memorizing individual points.

### How it works
1. Plot the training data (IQ vs CGPA vs Placement) same as before.
2. The algorithm runs on this data during training and learns a **mathematical function** — e.g., a **decision boundary** (a line/curve separating placed vs not-placed regions).
3. Once trained, the model **discards the need for training data**. It only keeps the learned function/parameters.
4. For a new point: just check which side of the decision boundary it falls on — no need to compare against old data points at all.

### Key characteristics
- Learns a **mathematical relationship between input and output** (a decision function/decision boundary for classification problems).
- Training data is **not required after training** — you can throw it away.
- What's stored is just the **model parameters** (e.g., slope & intercept for linear regression, weights for a neural network).
- **Generalization happens once, during training, before ever seeing a query point** — this is why it's also called **"eager learning."** The rule is fixed once learned and applied as-is to every future query.
- Because the rule is fixed in advance, prediction for a new point is fast — it's just a function evaluation, not a search/comparison over data.
- Examples: **Linear Regression, Logistic Regression, most other ML algorithms** — the majority of ML algorithms are model-based; instance-based ones are a smaller/specific set.

---

## 3. Key Differences

| Aspect | Instance-Based Learning | Model-Based Learning |
|---|---|---|
| **Data preprocessing** | Required (cleaning, encoding, etc.) | Required (same as instance-based) |
| **What's learned** | Nothing during training — data is just stored | A mathematical function/rule with parameters |
| **What's produced** | No trained "model" object — just stored data | A trained model with parameters (e.g., slope, intercept, weights) |
| **Prediction happens** | During training itself is a no-op; real work happens when a new query comes in | The model is trained once; then just applies the function to new inputs |
| **How the rule is derived** | New point is compared against *all* stored points every time | A generalized rule is derived once from training data, before ever seeing a query point |
| **When generalization happens** | Only when a new query point arrives (lazy learning) | Before seeing any query point, during training itself (eager learning) |
| **Dependence on new query point** | The output depends heavily on the incoming new point's neighbors | The rule stays the same regardless of which new point comes in |
| **Need to retain training data** | **Yes** — always needed for future predictions | **No** — training data can be discarded after training |
| **Storage requirement** | High — must store entire training dataset (e.g., 1GB training data = 1GB storage forever) | Low — only stores model parameters |
| **Prediction speed** | Slower (must compute distance to many/all points) | Faster (just evaluate the learned function) |
| **Alt. name** | Lazy learning (does nothing "actively" during training) | — |

---

## Quick takeaway

When learning a new ML algorithm, ask:
> "Does this algorithm build a rule/function during training and then discard the data (model-based)? Or does it just store the data and do all the work at prediction time by comparing against stored instances (instance-based)?"

That single question is enough to classify most algorithms into one of these two categories.
