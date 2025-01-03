# Expression Tracker for Dyslexic Children

## Overview  
This project aims to help therapists, educators, and game developers understand children's emotional engagement during gameplay to improve game design and educational outcomes for dyslexic children. By tracking emotional responses through facial expression analysis, the platform provides insights to optimize learning experiences and support mental well-being.

---

## Objectives  

### Problem Addressed  
- Assist therapists and game developers in understanding emotional engagement and improving game design for dyslexic children.  

### Importance  
- Gain insights into emotional states to optimize learning experiences and support children's mental well-being.

---

## System Design  

### High-Level Architecture  
- **Frontend**: React.js app capturing webcam images and displaying analysis.  
- **Backend**: Node.js server managing file storage, API integration, and user roles.  
- **Database**: MongoDB storing session data, images, and analysis results.  
- **API**: HuggingFace for emotion detection.

---

## Component Descriptions  

### Frontend  
- **Framework/Library**: React.js with Bootstrap for styling.  
- **Key Components**:  
  - **Login/Registration Pages**: Role-based user authentication.  
  - **Game UI**: Tracks gameplay and captures webcam images/screenshots.  
  - **Analysis Dashboard**: Displays sentiment insights and screenshots.  

### Backend  
- **Framework**: Express.js with Node.js.  
- **Routes and Middleware**:  
  - Image uploads and storage.  
  - API integration with HuggingFace.  
  - Role-based authentication and access control.  

### Database  
- **Technology**: MongoDB (Atlas).  
- **Schema Design**:  
  - **Collections**:  
    - **Sessions**:  
      ```json
      {
        "session_id": "string",
        "sessionName": "string",
        "imagePaths": ["array of strings"],
        "screenshotPaths": ["array of strings"],
        "modelResponse": ["array of strings"],
        "timestamps": "date"
      }
      ```  
    - **Adminschemas**:  
      ```json
      {
        "admin_name": "string",
        "phone_number": "string",
        "admin_email": "string",
        "role": "string",
        "admin_professions": "string",
        "password": "hashed string",
        "status": "string",
        "children_accounts": ["array of strings"]
      }
      ```  
    - **Games**:  
      ```json
      {
        "gameId": "string",
        "name": "string",
        "questions": ["array of strings"]
      }
      ```  

### External API  
- **HuggingFace API**: Emotion detection model.  
- **Key Configurations**: Access tokens securely managed via `.env` files.  

---

## Technology Stack  
- **Frontend**: React.js, Bootstrap.  
- **Backend**: Node.js, Express.js.  
- **Database**: MongoDB with Mongoose.  
- **External API**: HuggingFace Transformers.  
- **Other Tools**:  
  - Playwright (testing).  
  - GitHub (version control).  

---

## Future Scope  

### Personalized Analysis  
- **Therapists**: Detailed emotional breakdowns and progress tracking.  
- **Game Developers**: Insights for game optimization based on emotional engagement.  

### Model Improvement  
- Fine-tune the model with datasets tailored for dyslexic children.  
- Add parameters like microexpressions and gaze detection.  

---

## Conclusion  
This project demonstrates the potential of combining AI and web development to address educational and emotional challenges in dyslexic children. It highlights the importance of secure, accessible systems for sensitive user data while offering a robust platform to track emotional engagement during gameplay.
