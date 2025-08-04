<img width="1924" height="1084" alt="Screenshot 2025-08-02 153841" src="https://github.com/user-attachments/assets/e7a409ef-1836-440f-8996-9671d99df727" /># 🧠 AI_Nutrition_Assistant

**Problem Statement** – In an era where health awareness is growing, individuals increasingly seek personalized nutrition guidance. However, most existing tools provide generic diet plans, lack real-time adaptability, and fail to consider a person's holistic lifestyle, cultural preferences, allergies, and evolving health conditions. Furthermore, dieticians and nutritionists face limitations in scaling personalized consultations due to time and resource constraints.
<img width="6815" height="77" alt="image" src="https://github.com/user-attachments/assets/22fb64c3-4b8f-47cb-a042-7783e7213e0e" />


**The Smartest AI Nutrition Agent** – a personalized, adaptive nutrition coach built using IBM Cloud’s **Watsonx Agent Lab** with the **Mistral foundation model**, designed to suggest meals, explain nutrition, and track progress in a culturally-aware, fitness-sensitive way.

---

## 📋 Overview

### Features
- Conversational interface to configure health profile (age, weight, goals, dietary preferences)
- Meal planning with precise calories, macros, portion sizes
- Smart food swaps and nutritional reasoning (e.g. low-GI recommendations)
- Exercise suggestions with calorie‐burn estimations
- Multimodal support via search tool and optional upload features
- Adaptive behavior based on user feedback
- Friendly, motivational tone with health disclaimers

### Model
- Uses **Mistral‑large** (Watsonx foundation model)  
- Built via **Agent Lab** in IBM Cloud Lite account  

---

## 📂 Repository Structure

```text
📦AI_Nutrition_Assistant
 ┣ 📂screenshots
 ┃ ┣ agent_lab_config.png
 ┃ ┣ deployment_space.png
 ┃ ┗ preview_reply.png
 ┣ 📂tools
 ┃ ┗ sample_tool_interface.json
 ┣ 📂prompts
 ┃ ┗ agent_prompt.txt
 ┣ README.md
````

---

## 🚀 Setup & Deployment

1. Clone this repo:

   ```bash
   git clone https://github.com/your-org/AI_Nutrition_Assistant.git
   cd AI_Nutrition_Assistant
   ```

2. Log into IBM Cloud and open your **Watsonx.ai project** (`AI_Nutrition_Assistant`).

3. Update the **agent prompt** in Agent Lab with content from `prompts/agent_prompt.txt`.

4. Enable tools:

   * Google search
   * DuckDuckGo search
   * Wikipedia search
   * Webcrawler
   **Aditional custom tool(optional)**: calculator 

5. In the **tools/sample\_tool\_interface.json**, review the JSON schema for any custom tool configuration.

6. **Test** the agent in Agent Lab's Preview window using typical user queries.

7. Click **Save → Save as Agent**, then **Deploy**:

   * Create/obtain API Key
   * Create Deployment Space (`NutritionAI_Deployed`)
   * Deploy the agent

8. Validate deployment: open **preview tab**, send test message (e.g. “Create a 3‑day vegetarian meal plan”), and view output.

---

## 🖼️ Screenshots
**Agent Lab tools & prompt configuration**
![Agent Config](<img width="1924" height="1084" alt="Screenshot 2025-08-02 153841" src="https://github.com/user-attachments/assets/bb5ff828-1d29-4c9b-8501-9f67c901ef94" />
, <img width="1924" height="1084" alt="Screenshot 2025-08-02 153855" src="https://github.com/user-attachments/assets/7a413b9b-eb6f-49c6-8b89-be8f39f7b145" />
)

**Deployment space details (status: Ready)**
![Deployment Space](<img width="1923" height="759" alt="Screenshot 2025-08-02 143103" src="https://github.com/user-attachments/assets/bd5ebe32-0231-4056-9b69-0e5498f3152c" />
)

**Example nutrition assistant reply in Preview window**
![Preview Reply](<img width="1924" height="1084" alt="Screenshot 2025-08-02 151932" src="https://github.com/user-attachments/assets/7a855522-886b-449a-b0bc-eae9f6fdf859" />
, <img width="919" height="586" alt="Screenshot 2025-08-02 152825" src="https://github.com/user-attachments/assets/65769dc6-3c4a-47aa-a757-e28383180ca5" />
)

---

## 🧾 Agent Prompt (prompts/agent\_prompt.txt)

```text
You are NutrAI, a smart AI nutrition assistant.

• Ask clarifying questions: age, gender, weight, activity, goals, allergies, diet preferences.
• Calculate and recommend macros, calories, portion sizes per meal.
• Suggest healthy swaps (e.g. millet roti vs wheat roti), explain reasoning (low GI, high fiber).
• Include exercise guidance with approximate calorie burn.
• Provide cultural meal options (e.g. South‑Asian dishes like moong dal chilla, ragi dosa).
• Adapt suggestions based on user feedback (“Did you feel full?”).
• Offer hydration & micronutrient advice.
• Maintain supportive tone; include health disclaimer.
Always confirm understanding before finalizing recommendations.
```


---

## 🛠️ Tools Configuration (tools/sample\_tool\_interface.json)

Use this as reference if you create a custom tool to fetch nutrient data or perform calculations.

```json
{
  "name": "NutriSearch",
  "description": "Searches an internal nutrition database",
  "inputs": {
    "query": "string"
  },
  "outputs": {
    "answer": "string",
    "source": "string"
  }
}
```

---

## 📌 Usage

* 🎤 **Agent Lab Preview**: interactively test.
* 🔑 **API**: use the generated key for integration in mobile or web front-ends.
* 📥 **Client UI**: optionally consume the REST endpoint for chat-based frontend.

---

## 🧪 Sample Interaction

**User**:
> Hi, I want to lose weight. I’m 30, female, 68 kg, vegetarian.

**Agent**:
> Thanks! You prefer 3 meals + 1 snack per day. Zero eggs. Do you have any allergies?

---

## 📈 Future Work

* Integrate **Granite knowledge graphs** for more accurate nutrient-condition logic
* Enable **image or voice inputs** (food photo parsing, spoken meal logging)
* Include **feedback storage** in Cloudant and performance metrics tracking
* Export plans as PDF or link to kitchen appliance (smart fridge, wearables)

---

## 📚 References

* IBM watsonx.ai Agent Lab documentation
* IBM Cloud Lite plan details
* Nutrition APIs (USDA, Nutritionix) for food data
* Indian dietary guidelines (ICMR, NPCDCS)
* World Health Organization nutritional reference values

---

## ⚠️ Disclaimer

This project is for informational and educational purposes only. The agent is not a substitute for professional medical advice. Always consult a licensed healthcare provider for medical conditions or specialized diet plans.

---

Thank you for checking out **AI\_Nutrition\_Assistant**!
Feel free to raise issues, suggest improvements, or fork and build on top of this base.


