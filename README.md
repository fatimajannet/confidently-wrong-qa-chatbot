# 🤖 Story-Based QA Chatbot (NLP)  
*A model that learned to lie with confidence*  


## 🚨 **Executive Summary**  
Trained an LSTM to answer questions about stories. It now:  
- ✅ Answers correctly *sometimes*  
- ❌ Gaslights users *most times*  
- 🤖 **Confidence level**: *"I’m 91% sure I’m right (I’m not)"*  

---

## 💀 **Hall of Shame**  
| Prediction | Reality | Confidence |  
|------------|---------|------------|  
| *"Is Elsa in the garden?" → "yes"* | She’s in the kitchen | 91.1% |  
| *"Is the football in the garden?" → "yes"* | It’s in the garden | 87.3% |  
| *"Does 2+2=5?" → "yes"* | Orwellian nightmare | 94.2% |  

---

## 💬 How to Use This Repo
For learners: Study the notebooks/ to see how tokenization/training works.

For masochists: Try to reproduce the 91% wrong confidence error.

For everyone else: Laugh at my pain and avoid these pitfalls.

---


## 📂 Repository Structure  
```
.
├── /data/                  # Training data (JSON/CSV)
│   ├── train.json          # Normal examples  
│   └── adversarial.json    # "Is the fridge in the ocean? NO"  
├── /notebooks/             # Jupyter notebooks  
│   ├── 01_data_prep.ipynb  # Tokenization, padding  
│   └── 02_training.ipynb   # Model training + failure logs  
├── /saved_models/          # Pretrained weights  
│   └── liar_model.h5       # The 91% wrong-answer model  
├── LICENSE  
└── requirements.txt  
```

---

## 🧠 **Why This Exists**  
1. **To humble myself**  
   - Nothing says *"you know nothing"* like a model that lies with 91% confidence.  
2. **To warn others**  
   - If your NLP model works perfectly on the first try, you’re dreaming.  
3. **To document the grind**  
   - 50 epochs. 85% accuracy. 0% common sense.
     
Inspired by:
"If you’re not failing, you’re not trying hard enough." — Every ML engineer after their 10th ValueError.

---

## 🛠️ **How to "Fix" This** *(optional)*  
1. **Add more data**  
   - Especially edge cases like *"No, the fridge is NOT in the ocean"*.  
2. **Tune attention**  
   - Force the model to *actually read* the story.  
3. **Lower confidence**  
   - If confidence >90%, print *"I’m probably lying"*.  

```python
# Prototype "truth checker"
if confidence > 0.9 and answer == "yes":
    print("⚠️ Warning: I’m 90% sure I’m wrong")
```
---

## ✅ Lessons Learned  
1. **Accuracy ≠ Intelligence**  
   - Models optimize for metrics, not truth.  
2. **Test on absurd cases**  
   - If you don’t, users will.  
3. **Debugging > Coding**  
   - 80% of this project was fixing `ValueError`s.  

---

## 🎯 **Next Steps** *(If I get time)*  
- [ ] Deploy to prod and confuse real users
- [ ] Deploy with FastAPI for real-time testing
- [ ] Write a blog: *"How to fail upwards in NLP"*  
- [ ] Swap LSTM for GPT and create a *philosophical liar*

---

## 🤝 **Contributing**  
Step 1: Run `model.py`  
Step 2: Scream into a pillow  
Step 3: PR your fixes (or just cry with me)
```python
# Sample contribution:  
if prediction == "yes" and confidence > 0.9:  
    print("⚠️ Warning: Model is probably lying")  
```

**License**: [MIT](LICENSE)  
