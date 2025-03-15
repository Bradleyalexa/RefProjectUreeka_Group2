# RefProjectUreeka_Group2
Application hasn't completed yet on connecting frontend and backend endpoints.

# Codigi Learning Management System
## Overview
Codigi is a comprehensive Learning Management System (LMS) designed to facilitate online education through course management, interactive learning materials, and assessment tools. The platform supports both student and admin interfaces, an interactive website for students to learn.

## Tech Stack
### Backend
- **Framework**: FastAPI (Python)
- **Database**: SQLAlchemy ORM
- **Authentication**: JWT (JSON Web Tokens)
- **Password Security**: Bcrypt hashing
- **API Documentation**: FastAPI Swagger UI

### Frontend
- **HTML/CSS/JavaScript**
- **Responsive Design**
- **Modern UI Components**
- **Interactive Dashboard**


## Features
### 1. User Management
- **Authentication System**
  - User registration with email verification
  - Secure login with JWT tokens
  - Password hashing for security
  - Role-based access control (Admin/Student)

### 2. Course Management
- **Course Operations**
  - Create new courses with detailed information
  - List and browse available courses
  - Update course content and metadata
  - Delete courses with proper authorization
  - Categorize courses by topics
  
- **Course Content**
  - Structured curriculum sections
  - Multiple content types (Video, Article, Caption)
  - Progress tracking
  - Interactive learning materials

### 3. Material Management
- **Content Organization**
  - Upload and manage learning materials
  - Different material types support
  - Progress tracking for materials
  - Material categorization

### 4. Quiz System
- **Assessment Tools**
  - Create and manage quizzes
  - Track quiz completion
  - Time-based assessments
  - Score tracking and feedback

### 5. Admin Dashboard
- **Administrative Features**
  - Course management interface
  - User management
  - Content moderation
  - System analytics
  - Material management
  - Quiz administration

### 6. Student Dashboard
- **Learning Interface**
  - Course enrollment
  - Progress tracking
  - Quiz participation
  - Material access
  - Profile management


## Implementation Details

### Backend Architecture
#### 1. Database Models
- **User Models**
  ```python
  - Student: username, email, password_hash, first_name, last_name
  - Admin: admin credentials and permissions
  ```
- **Content Models**
  ```python
  - Course: title, description, category, timestamps
  - Material: content type, course association
  - Quiz: questions, answers, scoring
  ```

#### 2. API Endpoints

##### Authentication Routes (`/auth`)
```python
POST /auth/register - New user registration
POST /auth/login - User authentication
```

##### Course Routes (`/course`)
```python
POST /course/create - Create new course
GET /course/ - List all courses
GET /course/detail/{course_id} - Get course details
PUT /course/update/{course_id} - Update course
DELETE /course/delete/{course_id} - Delete course
```

##### Material Routes (`/material`)
```python
- Material management endpoints
- Content delivery endpoints
```

##### Answer/Quiz Routes (`/answer`)
```python
- Quiz submission endpoints
- Answer validation endpoints
```

### Frontend Structure
#### 1. Admin Interface
- **Dashboard Components**
  - Navigation sidebar
  - Course management interface
  - Material upload system
  - Quiz creation tools
  - User management panel

#### 2. Student Interface
- **Learning Components**
  - Course catalog
  - Learning material viewer
  - Quiz interface
  - Progress tracking
  - Profile settings

### Security Implementation
1. **Authentication**
   - JWT token-based authentication
   - Token expiration (30 minutes)
   - Password hashing with bcrypt
   - Email verification system

2. **Authorization**
   - Role-based access control
   - Route protection
   - Resource access validation

### Data Management
1. **Database Operations**
   - SQLAlchemy session management
   - CRUD operations for all entities
   - Relationship management
   - Data validation with Pydantic

2. **File Handling**
   - Course material storage
   - User uploads management
   - Content delivery system
