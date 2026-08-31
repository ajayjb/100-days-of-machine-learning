# Types of Machine Learning

```
                              Types of ML
        ┌───────────────┬───────────────┬───────────────┐
        │               │               │               │
   Supervised     Unsupervised    Semi-Supervised   Reinforcement
```

## 1. Supervised Learning
Model learns from **labeled** data (input → known output).

- **Regression** – predicts continuous values (e.g., price, temperature)
- **Classification** – predicts discrete categories (e.g., spam vs. not spam)

## 2. Unsupervised Learning
Model learns from **unlabeled** data and finds patterns on its own.

- **Clustering** – groups similar data points (e.g., customer segments)
- **Dimensionality Reduction** – compresses features while preserving structure (e.g., PCA)
- **Anomaly Detection** – flags data points that deviate from the norm (e.g., fraud detection)
- **Association** – finds relationships between variables (e.g., market basket analysis)

## 3. Semi-Supervised Learning
A mix of a small amount of labeled data + a large amount of unlabeled data. Useful when labeling is expensive but more accuracy than pure unsupervised learning is needed.

## 4. Reinforcement Learning
An **agent** learns by interacting with an **environment**, taking actions, and receiving **rewards/penalties**.

- Used in robotics, game-playing (e.g., AlphaGo), and tuning LLMs (RLHF)

## 5. Self-Supervised Learning
Model generates its **own labels** from the raw data itself (e.g., predicting a masked word in a sentence, or a missing patch in an image). This is the backbone of modern LLMs and many vision models.

## 6. Online vs. Batch Learning
A different axis — about *how* training happens over time, not what kind of labels are used.

- **Batch Learning** – trained once on a fixed dataset, then deployed
- **Online Learning** – model updates incrementally as new data streams in

## 7. Transfer Learning
A model trained on one task/dataset is **reused/fine-tuned** for a related task (e.g., fine-tuning a pretrained image model on your own dataset).

## 8. Active Learning
The model identifies the most **informative unlabeled examples** and asks a human to label them — used to reduce labeling cost.

## 9. Ensemble Learning
Combines multiple models to get better performance than any single model.

- **Bagging** (e.g., Random Forest)
- **Boosting** (e.g., XGBoost, AdaBoost)
- **Stacking**

---

### Quick Reference Table

| Type              | Data              | Goal                          | Examples                          |
|-------------------|-------------------|--------------------------------|------------------------------------|
| Supervised        | Labeled           | Predict output for new input   | Regression, Classification         |
| Unsupervised      | Unlabeled         | Discover structure/patterns    | Clustering, Dim. Reduction, Anomaly Detection, Association |
| Semi-Supervised   | Partially labeled | Better accuracy with less labeling | Mix of above |
| Reinforcement     | Reward signal     | Learn optimal actions          | Game AI, Robotics, RLHF            |
| Self-Supervised   | Auto-generated labels | Learn representations      | LLMs, Vision pretraining           |
| Online/Batch      | Any                | *How* training happens (axis, not a category) | Streaming vs. fixed dataset |
| Transfer Learning | Pretrained model + small target data | Reuse learned knowledge | Fine-tuning pretrained models |
| Active Learning   | Unlabeled pool     | Minimize labeling cost         | Human-in-the-loop labeling         |
| Ensemble Learning | Any                | Combine models for accuracy    | Random Forest, XGBoost, Stacking   |
