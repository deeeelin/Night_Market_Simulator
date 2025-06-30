# 🌃 Nightmarket Simulator

> Simulating and analyzing human flow in crowded spaces using GPU acceleration and visualization tools.

![Nightmarket Simulation](./demo.gif)

---

## 🚀 Introduction

In crowded events such as night markets or New Year's Eve celebrations, poor street designs often result in significant congestion and blockages. Our **Nightmarket Simulator** is designed to assess and visualize pedestrian flow under different street layouts to identify and improve crowd management efficiency.

### 🎯 Objective
- Evaluate and optimize street designs by simulating human traffic flow.
- Utilize GPU parallel computing for real-time and efficient crowd simulation.

---

## 🛠️ Key Features

- **GPU-Accelerated Simulation**: Efficient parallel processing to handle large-scale pedestrian simulations.
- **Configurable Preferences**: Customize pedestrian behavior, such as directional preferences (e.g., 80% probability moving right).
- **Collision Resolution**: Intelligent conflict resolution ensuring realistic pedestrian movement.
- **Visualization Pipeline**: Clear, intuitive visualization of simulation phases and pedestrian density.

---

## ⚙️ How It Works

### Simulation Flow:

1. **Initialization**:
   - Set pedestrians at random starting points.

2. **Decision Phase**:
   - Each pedestrian decides their next move based on configured directional preferences.

3. **Movement Phase**:
   - Pedestrians attempt to move to their next positions.

4. **Conflict Check**:
   - Positions with multiple pedestrians undergo a conflict resolution process, randomly selecting one pedestrian to occupy the space.

5. **Output Generation**:
   - Simulation results are periodically written to binary files representing the pedestrian map.

### Technical Implementation:

- CUDA-based parallelism for efficient simulation.
- GPU global memory stores pedestrian positions and updates.
- Python visualization scripts for result analysis.

---

## 🖥️ Visualization and Analysis

- Visualize pedestrian flow and crowd density using heatmaps.
- Analyze phase-to-phase pedestrian movement.
- Quantify throughput of pedestrians exiting the simulation area.

---

## 📈 Performance Insights

- Effective parallel computation with smooth scaling.
- Capable of simulating thousands of pedestrians with minimal setup overhead.
- Larger map sizes (2048+) may introduce computational overhead due to GPU resource limits.

---

## 🚧 Challenges and Solutions

| Challenge | Solution |
|-----------|----------|
| Pedestrian collision at same location | Implement directional buffers for incoming pedestrians |
| Infinite conflict loop | Pre-decide moves to prevent recursive conflicts |
| Determining turning directions | Predefine turn sections to simplify pedestrian navigation |

---

## 📝 Future Work
- Further optimization for larger-scale simulations.
- Enhanced real-time visualization capabilities.

---

Thank you for exploring our Nightmarket Simulator! Feel free to reach out with any feedback or inquiries. 🌟

