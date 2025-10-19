# LLM-Agent-for-ML-Prediction
# Autonomous AI Data Scientist: Predicting Disease Spread

A project demonstrating an LLM-based AI agent that autonomously plans, codes, debugs, and improves a machine learning solution for a real-world disease prediction task.

### Problem Statement

The goal, as defined in the assignment,  was to:
>"Given survey results in the past 3 days in a specific state in U.S., then predict the percentage of new tested positive cases in the 3rd day."

The evaluation metric is Mean Squared Error (MSE), with a "strong baseline" score set at **0.84773**.

### My Approach: The AI Agent

Instead of manually building a model, I used the AIDE (AI-Driven Exploration) framework. I configured and guided an LLM agent to act as a data scientist.

The agent's workflow:
1.  **Planning:** Analyze the problem and propose a solution.
2.  **Coding:** Write the Python code for data preprocessing, feature engineering, and modeling.
3.  **Executing:** Run the code and capture the results or errors.
4. **Debugging / Improving:** If the code fails or the MSE is high, the agent analyzes the feedback and *iteratively writes a new, better solution*.


### Results: Beating the Strong Baseline

The autonomous agent successfully generated, debugged, and optimized a solution.

* **Final Testing MSE:** **0.5107**
***Baseline Comparison:** This result significantly beats the "strong baseline" requirement of **0.84773**.

This project demonstrates the power of modern LLM agents in automating complex data science workflows.

### How to Run

1.  Clone this repository:
    ```bash
    git clone [https://github.com/YourUsername/Autonomous-AI-Data-Scientist.git](https://github.com/YourUsername/Autonomous-AI-Data-Scientist.git)
    cd Autonomous-AI-Data-Scientist
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Download the LLM model (Qwen 14B GGUF) used by the agent:
    ```bash
    wget [https://huggingface.co/DevQuasar/Qwen.Qwen2.5-14B-Instruct-1M-GGUF/resolve/main/Qwen.Qwen2.5-14B-Instruct-1M.Q2_K.gguf](https://huggingface.co/DevQuasar/Qwen.Qwen2.5-14B-Instruct-1M-GGUF/resolve/main/Qwen.Qwen2.5-14B-Instruct-1M.Q2_K.gguf)
    ```
    *(Note: This requires a GPU with sufficient VRAM.)*

4.  Open and run the `main.ipynb` notebook. The final, agent-generated script (`best_solution.py`) can also be run directly:
    ```bash
    python best_solution.py
    ```
