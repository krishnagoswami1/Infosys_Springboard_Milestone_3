# Infosys_Springboard_Milestone3

##  Problem Statement

The objective of **Milestone 3** in the *Infosys CodeGenieAI* project is to build an **end-to-end intelligent Code Generation and Explanation System** with secure user management and database integration.

The system should:
- Allow users to **sign up, log in, and recover passwords** securely using **MongoDB Atlas** and **SMTP Email Services**.  
- Enable users to **generate code** from natural language prompts using multiple **Hugging Face code models**.  
- Provide detailed **code explanations** to help users understand generated or custom code.  
- Maintain a **user profile and interaction history**, storing all prompts, model outputs, and explanations in the database.  
- Offer a simple, interactive **Streamlit-based UI** for smooth user experience and visualization of model outputs.

This milestone focuses on combining **AI-based code intelligence**, **user authentication**, and **database-backed history tracking** into one unified web application.
## System Architecture
Include a simple diagram or explanation showing how different components (Frontend - Streamlit, Backend - Python, Database - MongoDB Atlas, and Hugging Face models) interact with each other.

Example:
User → Streamlit UI → Hugging Face Token and Ngrok Token → MongoDB Atlas

##  Technologies Used
- **Frontend:** Streamlit  
- **Backend:** Python  
- **Database:** MongoDB Atlas
- **Authuntication:** JWT
- **Email Service:** SMTP (for password recovery)  
- **AI Models:** Hugging Face models (DeepSeek, Phi-2, Gemma, Stable-Code, Replit)  
- **Deployment:** ngrok (for public link generation)

##  Features
- Secure **Login/Signup** with password hashing  
- **Forgot Password** via email verification  
- **Code Generation** using 5 Hugging Face models  
- **Code Explanation** for understanding logic  
- **User Profile Page** showing personal info  
- **History Page** displaying past prompts and outputs  
- **MongoDB integration** for persistent data storage


##  User Authentication System

### 1.  Login and Signup
- Secure **user registration** and **login system** integrated with **MongoDB Atlas**.  
- **Passwords** are **hashed and securely stored** to ensure user privacy and data protection.  
- **Login credentials** are **verified with the backend** before granting access to the user dashboard.  

### 2.  Forgot Password
- Includes a **password recovery feature** using **SMTP Email Service**.  
- Users can **reset their password securely** via **email authentication**.  
- Ensures a smooth and safe way to regain account access in case of forgotten credentials.  

###  3. Login and Signup
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/1.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/2.png" width="600">

###  4. Forgot Password and Dashboard
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/3.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/4.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/5.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/6.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/7.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/8.png" width="600">

###  5. Code Generation and explanation

<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/9.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/10.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/11.png" width="600">

###  6.  Pofile and History

<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/13.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/12.png" width="600">

##  Database Integration

### Database: **MongoDB Cloud (MongoDB Atlas)**

### Collection Structure

| **Collection** | **Purpose** |
|-----------------|-------------|
| `users` | Stores user authentication details such as **username**, **email**, and **hashed password**. |
| `prompts` | Stores all **prompts entered by users** along with the **model name**, **generated output**, and **timestamp**. |
| `history` | Tracks **past interactions** and **usage history** for each user. |


###  7. MongoDB and Backend Connections
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/14.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/15.png" width="600">
<img src="https://github.com/krishnagoswami1/Infosys_Springboard_Milestone_3/blob/main/16.png" width="600">

### 8. Model Comparison

The project integrates **five advanced Hugging Face code models**, each with unique strengths in **code generation** and **explanation tasks**.  
Below is the comparison based on **model type, parameter size, response quality, and performance** observed during testing.

| **Model Name** | **Developer** | **Parameters** | **Strengths** | **Limitations** | **Overall Performance** |
|-----------------|----------------|----------------|----------------|------------------|--------------------------|
|  **DeepSeek-Coder-1.3B-Instruct** | DeepSeek AI | 1.3B | Fast and efficient for short code prompts; performs well in Python and C++ | Struggles with longer logic or multi-step reasoning |  Great for quick, lightweight code generation |
|  **Phi-2 (2.7B)** | Microsoft | 2.7B | Very good at understanding natural language prompts; produces readable and clean code | Slightly slower response time compared to smaller models |  Excellent balance between clarity and accuracy |
|  **Gemma-2B-IT** | Google | 2B | Strong in structured code explanation and logical reasoning; performs well with Java/Python | Code generation speed moderate; less creative in syntax variations |  Best for step-by-step code explanations |
|  **Stable-Code-3B** | Stability AI | 3B | Excels in multi-line and complex program generation; handles large prompts effectively | High resource usage; slower response for small tasks |  Best for complex and lengthy code generation |

###  Summary
- **Best for Beginners:**  *Phi-2 (Microsoft)* — simple, clear, and easy to understand.  
- **Best for Explanations:**  *Gemma-2B-IT (Google)* — detailed and logical explanations.  
- **Best for Complex Code:**  *Stable-Code-3B (Stability AI)* — handles advanced programming tasks well.  
- **Best Overall Balance:**  *Replit-Code-3B (Replit)* — reliable, practical, and versatile in multiple coding domains.  
- **Fastest Response:** *DeepSeek-Coder-1.3B* — lightweight and efficient.  

This multi-model integration allowed the system to **compare and visualize the strengths of each model**, ensuring diverse and high-quality code generation for every prompt.


##  Conclusion

The **CodeGenieAI Milestone 3 Project** successfully integrates **AI-powered code generation**, **secure user authentication**, and **cloud-based data management** into a single, interactive web platform.  

Through the use of multiple **Hugging Face models**, the system demonstrates how different AI models can generate, compare, and explain code efficiently across programming domains. The inclusion of **MongoDB Atlas** ensures secure and scalable storage of user data, prompts, and interaction history, while the **SMTP-based password recovery system** adds a professional layer of security and accessibility.  

The intuitive **Streamlit interface** provides a smooth user experience, allowing seamless transitions between login, code generation, explanation, and history tracking.  

Overall, this milestone showcases a well-rounded application combining **AI, database systems, and web technologies**, laying the foundation for a full-fledged **intelligent code assistant** that bridges the gap between human creativity and machine intelligence.  

