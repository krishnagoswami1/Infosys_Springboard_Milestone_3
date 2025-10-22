# Infosys_Springboard_Milestone_3

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
User → Streamlit UI → Backend (Python/Flask logic) → Hugging Face API → MongoDB Atlas

##  Technologies Used
- **Frontend:** Streamlit  
- **Backend:** Python  
- **Database:** MongoDB Atlas  
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
