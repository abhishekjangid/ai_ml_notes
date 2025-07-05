# Neural Network Forward Pass and Backpropagation Solution

## 1. Forward Pass

**Given:**
- Inputs: x₁ = 1, x₂ = 1
- Weights: w₁ = 1, w₂ = 2, w₃ = 1, w₄ = 2, w₅ = 1, w₆ = 1
- Activation: Sigmoid σ(z) = 1 / (1 + exp(-z))
- Desired output: y_target = 1

### Step 1: Calculate Hidden Layer Inputs (with clear steps)

**For Hidden Neuron H₁:**
- Net input:  
  z₁ = x₁·w₁ + x₂·w₂  
  = (1 × 1) + (1 × 2)  
  = 1 + 2 = 3
- Activation:  
  h₁ = σ(z₁) = 1 / (1 + exp(-3))  
  ≈ 0.9526

**For Hidden Neuron H₂:**
- Net input:  
  z₂ = x₁·w₃ + x₂·w₄  
  = (1 × 1) + (1 × 2)  
  = 1 + 2 = 3
- Activation:  
  h₂ = σ(z₂) = 1 / (1 + exp(-3))  
  ≈ 0.9526

**Summary:**
- h₁ = 0.9526
- h₂ = 0.9526

### Step 2: Output Layer Input

- Net input:  
  o₁_in = h₁·w₅ + h₂·w₆  
  = 0.9526 × 1 + 0.9526 × 1  
  = 1.9052
- Activation:  
  o₁ = σ(o₁_in) = 1 / (1 + exp(-1.9052))  
  ≈ 0.8705

### Step 3: Error Calculation

- Error (Mean Squared Error):
  
  E = 0.5 × (y_target - o₁)²  
  = 0.5 × (1 - 0.8705)²  
  ≈ 0.0085

---

## 2. Backpropagation: Update w₅ and w₆

### Step 1: Output Layer Delta

- δₒ₁ = (y_target - o₁) × o₁ × (1 - o₁)  
  = (1 - 0.8705) × 0.8705 × (1 - 0.8705)  
  = 0.1295 × 0.8705 × 0.1295  
  ≈ 0.0147

### Step 2: Weight Updates

- Δw₅ = η × δₒ₁ × h₁  
  = 0.24 × 0.0147 × 0.9526  
  ≈ 0.00336
- Δw₆ = η × δₒ₁ × h₂  
  = 0.24 × 0.0147 × 0.9526  
  ≈ 0.00336

### Step 3: Updated Weights

- w₅_new = w₅ + Δw₅  
  = 1 + 0.00336  
  = 1.00336
- w₆_new = w₆ + Δw₆  
  = 1 + 0.00336  
  = 1.00336

---

## Summary Table

| Step            | Value    |
|-----------------|----------|
| h₁, h₂          | 0.9526   |
| o₁              | 0.8705   |
| Error (MSE)     | 0.0085   |
| Δw₅             | 0.00336  |
| Δw₆             | 0.00336  |
| w₅_new          | 1.00336  |
| w₆_new          | 1.00336  |

---

**Conclusion:**
- The error after one forward pass is 0.0085.
- The updated weights are w₅ = 1.00336 and w₆ = 1.00336 after one backpropagation step.
