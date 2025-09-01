# Probabilistic_learning
The project aims to **predict housing price categories** (Low, Medium, High, Luxury) using a **Bayesian Network model**.   It leverages **probabilistic reasoning** to handle uncertainty, missing data, and provide interpretable results rather than just a single-point prediction.


# 🏡 Housing Price Prediction using Bayesian Networks

## 📌 Objective
The project aims to **predict housing price categories** (Low, Medium, High, Luxury) using a **Bayesian Network model**.  
It leverages **probabilistic reasoning** to handle uncertainty, missing data, and provide interpretable results rather than just a single-point prediction.

---

## 🔑 Use Cases
- **Real Estate:** Assists buyers and sellers in evaluating property ranges.
- **Decision Support:** Provides probabilities instead of only one fixed prediction.
- **Educational Purpose:** Demonstrates Bayesian reasoning and probabilistic inference in practice.

---

## 📊 Data Description
**Features (Inputs):**
- Median Income  
- House Age  
- Number of Rooms  
- Number of Bedrooms  
- Population  
- Household Occupancy  
- Latitude  
- Longitude  

**Target (Output):**
- Price Category: {Low, Medium, High, Luxury}

---

## ⚙️ Methodology (Flow Steps)

1. **Input Layer**
   - User enters data via web interface (HTML/CSS/JS).
   - Missing inputs allowed for flexibility.

2. **Preprocessing Layer**
   - Convert continuous values into discrete bins (Low/Medium/High).  
   - Normalize numeric values like income.  
   - Handle invalid or missing data.

3. **Model Definition Layer**
   - Define a **Bayesian Network**:  
     - 8 feature nodes  
     - 1 target node (Price)  
   - Construct **Conditional Probability Tables (CPTs)**.  
   - Use **Markov Blanket** for computational efficiency.

4. **Inference Layer**
   - Apply **Bayes’ Theorem** to compute posterior probabilities.  
   - Update priors with observed evidence.  
   - Marginalize missing features.  
   - Use **Variable Elimination** for exact inference.  
   - Normalize probabilities to sum = 1.

5. **Output & Visualization Layer**
   - Display posterior probability distribution for price categories.  
   - Compute expected price (weighted average).  
   - Show formulas with MathJax, network diagrams, and progress bars.

---

## 📐 Mathematical Insights

### 1. Bayes’ Theorem
Posterior = (Prior × Likelihood) / Evidence

- **Prior:** Initial belief of each price class.  
- **Likelihood:** Probability of observing features given that class.  
- **Evidence:** Normalizing factor.  
- **Posterior:** Updated probability after including input features.

---

### 2. Joint Probability Factorization
P(Price and Features) = P(Price) × P(Feature1 | Price) × P(Feature2 | Price) × ...

- Bayesian Networks break complex joint distributions into simpler conditional probabilities.

---

### 3. Posterior Probability
P(Price | Features) = [P(Price) × P(Features | Price)] / Sum over all price category

- Gives a probability distribution across categories (Low/Medium/High/Luxury).

---

### 4. Expected Price
Expected Price = Σ (Posterior Probability × Representative Value of Category)

- Converts probabilistic output into a numeric price estimate.

---

## ✅ Why Bayesian Networks?
- Handles **uncertainty** and **missing inputs** gracefully.  
- Provides **interpretable probabilities** instead of black-box outputs.  
- Efficient computation using **Markov blankets** and **variable elimination**.  

---

## 🚀 Future Enhancements
- Add more features (crime rate, school rating, distance to amenities).  
- Integrate real datasets for dynamic training.  
- Compare with machine learning models (Decision Trees, Neural Nets).  

---

## 📂 Project Structure
├── index.html # Frontend user interface
├── style.css # Styling for input and output
├── app.js # Input handling and API calls
├── model.py # Bayesian Network implementation
├── cpt.json # Conditional Probability Tables
└── README.md # Project documentation


---

## 📸 Visualization
- Bayesian Network Diagram (Price node connected to features)  
- Probability Distribution Bar Chart for categories  
- MathJax formulas for Bayesian reasoning  
