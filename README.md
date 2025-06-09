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
confidently-wrong-qa-chatbot/  
├── data/
│   ├── test_qa                                    # Your test set
│   └── train_qa                                    # Your train set
├── models/
│   ├── chatbot_10.h5                             # Pretrained model 1
│   └── chatbot_120_epochs.h5                             # Pretrained model 2
├── notebooks/
│   └── chatbot_project.ipynb                       # Colab file
├── papers/
│   └── End-To-End_Memory_Networks_1503.08895v5.pdf   # Research Paper PDF
```


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
- [ ] Swap LSTM for GPT and create a *philosophical liar*

---

## 🤝 **Contributing**  
Step 1: Run `model.py`  
Step 2: Scream into a pillow  
Step 3: PR your fixes (or just cry with me)


**License**: [MIT](LICENSE)  
