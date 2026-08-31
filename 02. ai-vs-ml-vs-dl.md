# AI vs Machine Learning vs Deep Learning

## 1. Introduction
- Common beginner question: what's the difference between AI, ML, and DL?
- Nested relationship: **AI** (outermost) → **ML** (subset of AI) → **DL** (subset of ML)
- Key takeaway: Deep Learning is a subset of Machine Learning, and Machine Learning is a subset of Artificial Intelligence.

## 2. What is AI?
- AI = the idea of bringing some form of intelligence into machines.
- "Intelligence" is a complex concept — includes problem-solving, creativity, imagination, emotional understanding.
- True human-like *general* intelligence is still hard to achieve; most research targets narrow, specific tasks.
- Most "successful AI" systems today solve limited/specific problems, not full human-like intelligence.

## 3. Early AI and Expert Systems
- Early AI research asked: can intelligence be built into a machine?
- **Expert systems**: human expert knowledge encoded as rule-based logic in software.
- These systems use a knowledge base + predefined rules to make decisions.
- **Limitation**: expert systems only work well on narrow, clearly defined problems.
- Tasks like image recognition and speech recognition are hard to solve with handcrafted rules — this is where expert systems fell behind.

## 4. The Need for Machine Learning
- **ML** = learning patterns / mathematical structure directly from data, instead of explicitly programming every rule.
- System extracts rules from data rather than being told the rules.
- Example: showing many labeled dog images lets the system learn what a "dog" is on its own.
- Strength: provide data → system learns, instead of manually writing rules.
- ML made a major comeback due to increased availability of data, hardware, and compute.
- Proven more effective than handcrafted AI in many practical applications.

## 5. Introduction to Deep Learning
- Question: if ML works well, why do we need Deep Learning?
- DL is fundamentally still part of ML — the difference is in the model architecture and learning approach.
- DL uses **neural network-style mathematical models** inspired by biological neurons (not an exact brain replica).
- Reason for DL's rise: certain problems weren't solved well enough by traditional ML.
- **Biggest issue with traditional ML: feature engineering** — humans must manually decide which input features to use.
- DL can automatically learn features, which helps a lot with complex data.

## 6. ML vs DL — Key Differences
| Aspect | Machine Learning | Deep Learning |
|---|---|---|
| Features | Must be manually selected (feature engineering) | Learned automatically from raw data |
| Domain knowledge | Often required to pick right inputs | Less dependent on manual feature selection |
| Structure | Simpler models | Multiple layers capture increasingly complex patterns |
| Example use | Placement prediction (needs chosen features) | Digit recognition (early layers learn simple patterns, later layers learn higher-level structure) |
| Scaling with data | Performance often plateaus | Tends to keep improving with more data |
| Best suited for | Structured problems, smaller datasets | Complex tasks, unstructured data (images, text) |

## 7. When to Use DL vs When to Use ML
- **DL is strong for**: image classification, text/NLP tasks, and other unstructured-data applications.
- **DL is not always necessary** — ML can be better or more practical in many cases.
- Prefer traditional ML when:
  - Data is limited
  - Compute is constrained
  - The problem is structured
- Example: banking and insurance often don't have massive datasets, so DL isn't always the best choice there.

## 8. Real-World Use Case Examples

### Machine Learning (structured/tabular data, fewer features needed)
- **Spam email detection** — classifying emails using features like sender, keywords, frequency
- **Credit scoring / loan approval** — predicting default risk from income, credit history, etc.
- **Customer churn prediction** — predicting which customers are likely to leave, based on usage patterns
- **Sales/demand forecasting** — predicting future sales from historical structured data
- **Fraud detection in banking** — flagging suspicious transactions using transaction-level features
- **Recommendation systems (basic)** — e.g. collaborative filtering for product suggestions
- **Placement/salary prediction** — predicting outcomes from structured features (CGPA, experience, skills)

### Deep Learning (unstructured data, automatic feature learning)
- **Image classification** — identifying objects, animals, or diseases in photos (e.g. medical imaging, X-rays)
- **Face recognition** — used in phone unlock, security systems
- **Speech recognition** — voice assistants like Siri, Alexa, Google Assistant
- **Natural language processing (NLP)** — chatbots, sentiment analysis, machine translation
- **Self-driving cars** — recognizing lanes, pedestrians, obstacles from camera/sensor data
- **Handwriting/digit recognition** — reading handwritten digits or text (e.g. OCR)
- **Large language models** — text generation, summarization, question-answering (e.g. ChatGPT-style models)
- **Video analysis** — action recognition, video captioning, content moderation

## 9. Conclusion
- AI is the broadest field.
- ML sits within AI.
- DL sits within ML.
- Choice between ML and DL depends on data availability, compute resources, and problem structure — not "DL is always better."
