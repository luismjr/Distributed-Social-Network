# 🌐 Distributed Social Network Platform

[![Django](https://img.shields.io/badge/Django-5.2.4-green.svg)](https://djangoproject.com/)
[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://python.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-blue.svg)](https://postgresql.org/)
[![Django REST Framework](https://img.shields.io/badge/DRF-3.16.0-red.svg)](https://www.django-rest-framework.org/)
[![Heroku](https://img.shields.io/badge/Deployed-Heroku-purple.svg)](https://heroku.com/)

> **A sophisticated distributed social networking platform implementing ActivityPub protocol standards, featuring cross-node communication, advanced privacy controls, and comprehensive social features.**

## 🚀 Project Overview

This project implements a **distributed social network** that enables users across different nodes to interact seamlessly. Built with Django and Django REST Framework, it demonstrates advanced web development concepts including distributed systems, API design, real-time communication, and scalable architecture patterns.

### 🎯 Key Achievements

- **Distributed Architecture**: Multi-node social network with cross-server communication
- **ActivityPub Compliance**: Implements industry-standard protocols for federated social networking
- **Advanced Privacy Controls**: Granular visibility settings (Public, Friends-only, Unlisted)
- **Real-time Features**: Live inbox notifications, follow requests, and social interactions
- **Scalable Design**: Production-ready with PostgreSQL, Redis, and Heroku deployment
- **RESTful API**: Comprehensive API with 50+ endpoints supporting all social features

## 🏗️ Technical Architecture

### Backend Stack
- **Framework**: Django 5.2.4 with Django REST Framework 3.16.0
- **Database**: PostgreSQL (production) / SQLite (development)
- **Authentication**: Django's built-in auth system with custom user models
- **API Design**: RESTful architecture with comprehensive serialization
- **Deployment**: Heroku with Gunicorn WSGI server
- **Static Files**: WhiteNoise for efficient static file serving

### Core Technologies
- **Python 3.x** - Backend development
- **Django ORM** - Database abstraction and management
- **UUID** - Unique identifier generation for distributed systems
- **Markdown** - Rich text content support
- **Pillow** - Image processing and management
- **Requests** - HTTP client for cross-node communication

## ✨ Features & Capabilities

### 🔐 User Management
- **User Registration & Authentication** with secure password validation
- **Profile Management** with customizable display names, descriptions, and GitHub integration
- **Profile Images** with URL-based image hosting
- **Soft Delete System** for data preservation and admin oversight

### 👥 Social Features
- **Follow System** with request/approval workflow
- **Friendship Management** with mutual following capabilities
- **Cross-Node Following** enabling users to follow accounts on different servers
- **Follow Request Management** with accept/reject functionality
- **Follower/Following Lists** with comprehensive relationship tracking

### 📝 Content Management
- **Rich Text Posts** supporting both plain text and Markdown
- **Image Posts** with automatic URL generation and processing
- **Content Visibility Controls**:
  - Public posts (visible to all)
  - Friends-only posts (mutual friends only)
  - Unlisted posts (direct link access only)
- **Post Editing & Deletion** with soft delete preservation
- **Content Type Detection** for automatic formatting

### 💬 Interaction Features
- **Commenting System** with threaded discussions
- **Like System** for posts and comments
- **Real-time Inbox** for notifications and activity feeds
- **Cross-Node Interactions** allowing users to interact with content from other servers

### 🌐 Distributed System Features
- **Multi-Node Architecture** supporting multiple independent servers
- **Cross-Server Communication** via HTTP APIs
- **ActivityPub Protocol** implementation for federated social networking
- **Remote Post Distribution** automatically sharing content with followers on other nodes
- **Node Authentication** with username/password credentials for server-to-server communication

### 📊 Advanced Features
- **Comprehensive API** with 50+ endpoints
- **Admin Dashboard** for system management
- **Data Serialization** for cross-platform compatibility
- **URL Normalization** for consistent resource identification
- **Timezone Handling** with MST/Edmonton timezone support

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.8+
- PostgreSQL (for production)
- Git

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Distributed-Social-Network.git
   cd Distributed-Social-Network
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Database setup**
   ```bash
   python manage.py migrate
   python manage.py createsuperuser
   ```

5. **Run development server**
   ```bash
   python manage.py runserver
   ```

See [the web page](https://uofa-cmput404.github.io/general/project.html) for a description of the project.

Make a distributed social network!

## License

## 📡 API Documentation

### Core Endpoints

#### Authors
- `GET /api/authors/` - List all authors
- `GET /api/authors/{serial}/` - Get specific author
- `POST /api/authors/{serial}/followers/` - Follow an author
- `GET /api/authors/{serial}/followers/` - Get author's followers

#### Posts/Entries
- `GET /api/authors/{serial}/entries/` - Get author's posts
- `POST /api/authors/{serial}/entries/` - Create new post
- `GET /api/authors/{serial}/entries/{entry_id}/` - Get specific post
- `POST /api/entries/{entry_id}/like/` - Like a post

#### Comments
- `GET /api/authors/{serial}/entries/{entry_id}/comments/` - Get post comments
- `POST /api/authors/{serial}/entries/{entry_id}/comments/` - Add comment
- `POST /api/comment/{comment_id}/like/` - Like a comment

#### Inbox & Notifications
- `GET /api/authors/{serial}/inbox/` - Get user's inbox
- `POST /api/authors/{serial}/inbox/` - Send activity to inbox

## 🎥 Demo Video

[![Watch the video on YouTube](https://img.youtube.com/vi/aaOTHRIbRf8/0.jpg)](https://www.youtube.com/watch?v=aaOTHRIbRf8)

## 👥 Team

This project was developed as part of CMPUT 404 - Web Applications and Architecture at the University of Alberta.

**Contributors:**
- Kevin Wan
- Abdullah Faisal  
- Maro Erivona
- Ahmed Shittu
- **Luis Martinez** (Primary Developer)
- Nina Han

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## 🔗 Related Links

- [Project Requirements](https://uofa-cmput404.github.io/general/project.html)
- [ActivityPub Specification](https://www.w3.org/TR/activitypub/)
- [Django Documentation](https://docs.djangoproject.com/)
- [Django REST Framework](https://www.django-rest-framework.org/)

---
