# Expression Expert Platform (表达小达人)

An innovative AI-powered language expression training platform specifically designed for elementary school students to enhance their oral communication skills through intelligent tutoring and personalized feedback.

## 🌟 Project Overview
This platform addresses the challenges in traditional Chinese language education by leveraging advanced AI technologies to provide personalized, interactive learning experiences for young learners aged 6-9 years.

## 🎯 Key Features

### For Students
- **Real-time Speech Recognition**: Convert spoken language to text using advanced ASR technology
- **Multi-dimensional Assessment**: Evaluate expressions across three dimensions - completeness, logic, and emotional expression
- **Interactive AI Assistant**: Get instant feedback and guidance from intelligent tutoring system
- **Gamified Learning**: Engaging cartoon-style interface with progressive difficulty levels
- **Voice Input Support**: Eliminate typing barriers for young learners

### For Parents & Educators
- **Progress Tracking**: Monitor learning progress and achievement records
- **Learning Analytics**: Detailed reports on student performance and improvement areas
- **Daily Task Management**: Automated review scheduling based on spaced repetition
- **Historical Records**: Complete learning history with AI feedback archives

## 🛠 Technology Stack
- **Frontend**: Vue.js 2.0 with responsive design
- **Backend**: Spring Boot with RESTful APIs
- **Database**: MySQL with JPA/Hibernate
- **AI Integration**: 
  - Xunfei Speech Recognition API for real-time voice processing
  - GLM-4V Large Language Model for intelligent assessment and feedback
- **Real-time Communication**: WebSocket for live speech processing
- **Security**: JWT authentication with Spring Security

## 🏗 Architecture Highlights
- **Multi-layered Architecture**: Presentation → Security → Business Logic → Data Access
- **Component-based Design**: Modular components for user management, task processing, AI assistance, and speech recognition
- **Real-time Processing**: WebSocket-based audio streaming with instant feedback
- **Scalable Design**: Microservices-ready architecture for future expansion

## 📱 Core Modules

### 1. User Management
- Secure registration and authentication
- Role-based access control
- Profile management and preferences

### 2. Task Learning System
- Picture-based expression tasks
- Multi-stage learning progression
- Adaptive difficulty adjustment
- Performance analytics

### 3. AI Assessment Engine
- Three-dimensional evaluation framework
- Personalized feedback generation
- Learning path optimization
- Intelligent hint generation

### 4. Speech Recognition
- Real-time audio processing
- Noise reduction and enhancement
- Multi-format audio support
- Cross-platform compatibility

## 🎨 User Experience
- **Child-friendly Interface**: Colorful, cartoon-style design optimized for young learners
- **Accessibility Features**: Pinyin support for character recognition
- **Multi-platform Support**: Web-based platform compatible with desktop and mobile devices
- **Intuitive Navigation**: Simple, icon-based navigation suitable for elementary students

## 📊 Educational Impact
- **Personalized Learning**: Adaptive content based on individual progress
- **Immediate Feedback**: Real-time assessment and correction
- **Skill Development**: Comprehensive language expression skill building
- **Confidence Building**: Positive reinforcement and achievement recognition

## 🚀 Technical Innovation
- **Hybrid AI Approach**: Combining speech recognition with natural language understanding
- **Multi-modal Learning**: Integration of visual, auditory, and interactive elements
- **Intelligent Tutoring**: Context-aware AI assistant providing personalized guidance
- **Progressive Assessment**: Dynamic evaluation system adapting to student capabilities

## 🔒 Security & Privacy
- JWT-based authentication system
- Encrypted data transmission (HTTPS/WSS)
- Privacy-compliant data handling
- Secure API endpoints with rate limiting

## 🎓 Educational Standards Compliance
- Aligned with Chinese elementary education curriculum standards
- Evidence-based pedagogical approaches
- Age-appropriate content and interaction design
- Measurable learning outcomes

## 📈 Future Roadmap
- Mobile app development (iOS/Android)
- Advanced analytics dashboard
- Multi-language support expansion
- Integration with classroom management systems
- Voice emotion analysis enhancement

## 👥 Target Audience
- **Primary Users**: Elementary school students (grades 1-3)
- **Secondary Users**: Parents seeking to support their children's language development
- **Educational Partners**: Teachers and schools looking for AI-assisted learning tools

## 📄 Documentation
- [Requirements Specification (Chinese)](./docs/SRS.md)
- [System Design Document (Chinese)](./docs/SDD.md)
- [API Documentation](./docs/API.md)
- [Deployment Guide](./docs/DEPLOYMENT.md)

## 🤝 Contributing
We welcome contributions to improve the platform's functionality and educational effectiveness. Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting pull requests.

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🏆 Recognition
- Developed as part of Software Engineering coursework at Tongji University
- Supervised by Prof. [Supervisor Name]
- Team: 段培煜, 杨烜赫, 李紫浩, 刘佳朋

Built with ❤️ for empowering young learners' expression abilities through intelligent technology.