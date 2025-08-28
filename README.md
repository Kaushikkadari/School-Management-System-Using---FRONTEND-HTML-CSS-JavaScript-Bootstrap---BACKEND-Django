# 🏫 School Management System

A comprehensive web-based School Management System built with Django, designed to streamline educational institution operations including student management, teacher administration, course scheduling, attendance tracking, and academic reporting.

## ✨ Features

### 👨‍💼 **Admin Dashboard**
- **Student Management**: Add, edit, delete, and track student information
- **Teacher Management**: Manage teacher profiles, assignments, and performance
- **Course Management**: Create and manage courses, subjects, and curriculum
- **Financial Management**: Handle fee collection, invoices, and payment tracking
- **Academic Reports**: Generate comprehensive reports and analytics
- **System Settings**: Configure school parameters and user permissions

### 👨‍🏫 **Teacher Portal**
- **Dashboard**: Overview of classes, students, and teaching schedule
- **Course Management**: Upload materials, create assignments, and manage grades
- **Attendance Tracking**: Mark and monitor student attendance
- **Grade Management**: Record and update student grades and performance
- **Communication**: Send announcements and messages to students
- **Timetable Management**: View and manage class schedules

### 👨‍🎓 **Student Portal**
- **Dashboard**: Personal academic overview and progress tracking
- **Course Enrollment**: Browse and enroll in available courses
- **Assignment Submission**: Submit assignments and view grades
- **Attendance Tracking**: Monitor personal attendance records
- **Fee Management**: View fee statements and payment history
- **Timetable**: Access personal class schedule

### 📊 **Advanced Features**
- **Real-time Analytics**: Interactive charts and performance metrics
- **Multi-role Authentication**: Secure role-based access control
- **File Management**: Upload and manage course materials and documents
- **Calendar Integration**: Event scheduling and academic calendar
- **Export Capabilities**: Generate PDF and Excel reports
- **Responsive Design**: Mobile-friendly interface

## 🛠️ Technology Stack

- **Backend**: Django 4.2+ (Python)
- **Frontend**: HTML5, CSS3, JavaScript, Bootstrap 5
- **Database**: SQLite (Development) / PostgreSQL (Production)
- **Charts**: Chart.js
- **Calendar**: FullCalendar.js
- **PDF Generation**: ReportLab
- **Excel Export**: OpenPyXL

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Python 3.8+**
- **pip** (Python package installer)
- **Git** (for cloning the repository)

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/school-management-system.git
cd school-management-system
```

### 2. Create Virtual Environment
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Database Setup
```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create Superuser
```bash
python manage.py createsuperuser
```

### 6. Run the Application
```bash
python manage.py runserver
```

The application will be available at `http://127.0.0.1:8000/`

## 👥 User Roles & Access

### **Administrator**
- Full system access and control
- Manage all users, courses, and system settings
- Generate comprehensive reports
- Handle financial operations

### **Teacher**
- Manage assigned courses and students
- Track attendance and grades
- Upload course materials
- Communicate with students

### **Student**
- View personal academic information
- Submit assignments
- Track attendance and grades
- Access course materials

## 📁 Project Structure

```
school-management-system/
├── accounts/                 # Main Django app
│   ├── models.py            # Database models
│   ├── views.py             # View functions
│   ├── forms.py             # Form definitions
│   ├── admin.py             # Admin interface
│   ├── urls.py              # URL routing
│   ├── templates/           # HTML templates
│   └── static/              # Static files
├── SMS/                     # Django project settings
│   ├── settings.py          # Project configuration
│   ├── urls.py              # Main URL configuration
│   └── wsgi.py              # WSGI configuration
├── media/                   # User-uploaded files
├── staticfiles/             # Collected static files
├── requirements.txt         # Python dependencies
├── manage.py               # Django management script
└── README.md               # This file
```

## 🔧 Configuration

### Environment Variables
Create a `.env` file in the project root:

```env
DEBUG=True
SECRET_KEY=your-secret-key-here
DATABASE_URL=sqlite:///db.sqlite3
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_HOST_USER=your-email@gmail.com
EMAIL_HOST_PASSWORD=your-app-password
```

### Database Configuration
For production, update `settings.py`:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_db_name',
        'USER': 'your_db_user',
        'PASSWORD': 'your_db_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

## 📊 Sample Data

To populate the system with sample data:

```bash
python manage.py populate_sample_data
```

This will create:
- Sample students and teachers
- Course data and schedules
- Attendance records
- Grade information

## 🔐 Security Features

- **Password Protection**: Secure password hashing and validation
- **Session Management**: Secure session handling
- **CSRF Protection**: Cross-site request forgery protection
- **XSS Prevention**: Input sanitization and validation
- **SQL Injection Protection**: Django ORM protection
- **File Upload Security**: Secure file handling and validation

## 📱 Responsive Design

The application is fully responsive and works on:
- Desktop computers
- Tablets
- Mobile phones
- All modern browsers

## 🚀 Deployment

### Heroku Deployment
1. Create a `Procfile`:
```
web: gunicorn SMS.wsgi --log-file -
```

2. Add buildpacks:
```bash
heroku buildpacks:add heroku/python
heroku buildpacks:add heroku/nodejs
```

3. Deploy:
```bash
git push heroku main
```

### Docker Deployment
1. Build the image:
```bash
docker build -t school-management-system .
```

2. Run the container:
```bash
docker run -p 8000:8000 school-management-system
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Development Guidelines
- Follow PEP 8 Python style guidelines
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed

## 🐛 Bug Reports

If you find a bug, please create an issue with:
- Detailed description of the problem
- Steps to reproduce
- Expected vs actual behavior
- Screenshots (if applicable)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Kadari Kaushik**
- GitHub: [@yourusername](https://github.com/yourusername)
- Email: your.email@example.com

## 🙏 Acknowledgments

- Django community for the excellent framework
- Bootstrap team for the responsive UI components
- Chart.js for beautiful data visualization
- All contributors and testers

## 📞 Contact
- Email: kadarikaushik078@gmail.com
  
## 🔄 Version History

- **v1.0.0** - Initial release with core features
- **v1.1.0** - Added advanced reporting and analytics
- **v1.2.0** - Enhanced UI/UX and mobile responsiveness
- **v1.3.0** - Added file management and communication features

---

**⭐ Star this repository if you find it helpful!**

**© 2025 Kadari Kaushik. All rights reserved.**


