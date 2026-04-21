## 👥 👨‍💻 Contributors of the Project
This project was developed with the following contributors:
- Viyani Sushmitha MJ
- Suhaas Teja Vijjagiri
- Sudip Das

Original repository: (https://github.com/suhaasteja/CMPE295b)

CARLA Vision-Language Model (VLM) Decision Support System
📌 Project Overview

This project explores the use of Vision-Language Models (VLMs) as a decision-support layer for autonomous driving systems in the CARLA simulator. Instead of replacing traditional autonomy modules such as Model Predictive Control (MPC), the VLM is used as an auxiliary reasoning layer that enhances interpretability, robustness, and human-understandable decision-making.

The system processes camera images and lightweight vehicle telemetry to generate structured reasoning outputs that assist in autonomous driving decisions.

🧠 Key Idea

Rather than directly controlling the vehicle, the VLM acts as a high-level reasoning agent that:

Interprets the driving scene
Identifies risks and hazards
Suggests high-level driving actions with explanations

This enables a human-interpretable autonomous driving pipeline.

⚙️ System Architecture

The system is built as a three-stage prompting framework inside the CARLA environment:

1️⃣ Scene Perception
Input: Camera frame + telemetry
Output: Structured description of:
Road layout
Traffic participants
Control signals
2️⃣ Risk Assessment
Identifies:
Potential hazards
Traffic constraints
Environmental risks
Uses both visual + vehicle state information
3️⃣ High-Level Action Selection
Outputs:
Suggested maneuver (e.g., brake, turn, accelerate)
Control recommendations
Human-readable reasoning
🔄 Closed-Loop CARLA Integration
Built a closed-loop CARLA–VLM architecture
Runs on a single HPC node
Uses a lightweight handshake protocol between:
CARLA simulator
Vision-Language Model inference pipeline
Control decision layer (MPC-compatible)
🎯 Objectives

This project does NOT aim to replace autonomous driving systems.

Instead, it focuses on:

Enhancing interpretability of decisions
Improving debugging capability for AV systems
Increasing user trust in autonomous driving models
Providing a language-based reasoning layer over perception systems

🧪 Evaluation

The system includes evaluation outputs stored in:

eval_results.csv
ollama_results.parquet
ollama_results.html

These files capture:

Model reasoning quality
Action selection consistency
Structured output validation

🧩 Technologies Used
CARLA Simulator
Vision-Language Models (VLM)
LLaVA / Ollama-based inference (if applicable)
Python
OpenAI-style structured prompting
Pandas / Parquet / CSV evaluation pipeline
📊 Outputs

The system generates:

Scene descriptions
Risk summaries
Action recommendations
Structured evaluation metrics
💡 Future Improvements
Real-time multi-agent traffic reasoning
Stronger multimodal fusion (LiDAR + radar)
Reinforcement learning integration
Improved hallucination detection in VLM outputs


