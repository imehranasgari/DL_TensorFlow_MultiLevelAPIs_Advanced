# TensorFlow Multi-Level API Exploration

## 1. Project Title

**Exploring TensorFlow’s Multi-Level APIs: Low-Level Ops to High-Level Keras**

---

## 2. Problem Statement and Goal of Project

This notebook investigates **how TensorFlow’s different API layers** — from low-level tensor operations to high-level Keras abstractions — interact and can be composed.
The aim is to:

* Understand the flexibility of TensorFlow’s multi-level design.
* Demonstrate equivalent operations at different abstraction levels.
* Compare workflows for creating and training models using these APIs.

---

## 3. Solution Approach

The notebook follows an **incremental abstraction approach**:

1. **Low-level TensorFlow ops** – Define computations directly with `tf.constant`, `tf.Variable`, and math operations.
2. **Mid-level Layers API** – Build models using `tf.keras.layers` with manual weight initialization and forward passes.
3. **High-level Keras API** – Use `tf.keras.Sequential` and `tf.keras.Model` for rapid prototyping, training, and evaluation.
4. **Mix-and-match strategy** – Combine low-level control with high-level convenience for custom model building.
5. Explore **dataset pipelines** using `tf.data.Dataset` for feeding data to models.

---

## 4. Technologies & Libraries

From the code:

* **TensorFlow** – core ops, variables, optimizers, datasets.
* **Keras** (via TensorFlow) – `Sequential`, `Model`, `Dense`, `Flatten`, and other layers.
* **NumPy** – array creation and manipulation.

---

## 5. Description about Dataset

**Not provided** – The notebook generates synthetic data (NumPy arrays / tensors) for demonstrations. No external dataset is loaded.

---

## 6. Installation & Execution Guide

**Requirements:**

```bash
pip install tensorflow numpy
```

**Run the notebook:**

```bash
jupyter notebook multi_level_apis_me.ipynb
```

or in JupyterLab:

```bash
jupyter lab multi_level_apis_me.ipynb
```

Execute cells sequentially to reproduce the examples and outputs.

---

## 7. Key Results / Performance

### Model Construction at Different API Levels

* **Low-level:** Manual tensor math produced correct forward passes and weight updates.
* **Mid-level:** `tf.keras.layers.Dense` with manual calls yielded same functional results with less boilerplate.
* **High-level:** `Sequential` and `Model` APIs allowed rapid building, compilation, and fitting.

### Dataset Pipeline

* Creation of `tf.data.Dataset` from tensors demonstrated efficient batch processing.

### Output Examples

Representative console outputs from the notebook:

```
Eager execution results: [ ... ]
Layer API output shape: (batch_size, units)
Sequential model training: loss decreased over epochs
```

*(Exact values depend on random seeds and synthetic data.)*

---

## 8. Screenshots / Sample Out

(Extracted from notebook outputs)

**Low-Level Tensor Math:**

```
<tf.Tensor: shape=(...), dtype=float32, numpy=...>
```

**Keras Sequential Summary:**

```
Model: "sequential"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 dense (Dense)               (None, X)                 Y
 ...
=================================================================
```

---

## 9. Additional Learnings / Reflections

* TensorFlow offers **progressive abstraction layers** — allowing developers to trade off between control and convenience.
* The **Layer API** is a practical balance: low enough for customization, high enough to avoid manual graph wiring.
* The **Sequential / Model API** is ideal for rapid iteration but can be combined with low-level ops for advanced needs.
* `tf.data.Dataset` integrates seamlessly with all API levels, providing efficient input pipelines.

> 💡 *Some interactive outputs (e.g., plots, widgets) may not display correctly on GitHub. If so, please view this notebook via [nbviewer.org](https://nbviewer.org) for full rendering.*

---

## 👤 Author

**Mehran Asgari**
**Email:** [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)
**GitHub:** [https://github.com/imehranasgari](https://github.com/imehranasgari)

---

## 📄 License

This project is licensed under the MIT License – see the `LICENSE` file for details.

---
