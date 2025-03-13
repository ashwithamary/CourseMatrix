# CourseMatrix

CourseMatrix is a full-featured online learning platform that connects educators and students through high-quality digital courses. The platform enables content creators to share their expertise while providing learners with a seamless educational experience across various subjects.

## 🌐 Live Demo

- **Frontend**: [https://course-matrix-frontend.vercel.app/](https://course-matrix-frontend.vercel.app/)
- **Backend**: [https://course-matrix-backend.vercel.app/](https://course-matrix-backend.vercel.app/)

## 🎯 Project Overview

CourseMatrix was developed as a comprehensive solution for online education, addressing the growing demand for accessible, high-quality learning experiences. Built with modern web technologies, this platform demonstrates full-stack development capabilities across user authentication, content management, payment processing, and media handling.

Key highlights:
- Fully responsive design that works across devices
- Comprehensive user roles (students and educators)
- Secure payment integration through Stripe
- Cloud-based content delivery
- Intuitive course creation and consumption
  
## 📖 Table of Contents
- [Live Demo](#-live-demo)
- [Project Overview](#-project-overview)
- [Features](#-features)
- [Tech Stack](#️-tech-stack)
- [Architecture](#️-architecture)
- [Screenshots](#-screenshots)
- [Installation & Setup](#-installation--setup)
- [Usage](#-usage)
- [API Documentation](#-api-documentation)
- [Future Enhancements](#-future-enhancements)
- [Contributing](#-contributing)
- [Contact](#-contact)
- [Skills Demonstrated](#-skills-demonstrated)
  
## ✨ Features

### For Students
- **Course Discovery**: Browse and search through a diverse catalog of courses
- **Detailed Course Info**: View comprehensive course information including ratings, curriculum, and pricing
- **User Authentication**: Secure account management through Clerk
- **Course Enrollment**: Seamless payment process via Stripe
- **Learning Dashboard**: Track enrolled courses and progress
- **Video Playback**: Stream course content with an integrated video player
- **Course Rating**: Provide feedback through a 5-star rating system

### For Educators
- **Course Creation**: Intuitive interface for creating structured courses
- **Content Management**: Organize courses by chapters and lectures
- **Revenue Tracking**: Dashboard with enrollment and earning metrics
- **Student Management**: View and manage enrolled students
- **Analytics**: Track course performance and student engagement

## 🛠️ Tech Stack

### Frontend
- **React**: UI library for building components
- **React Router**: For navigation and routing
- **Tailwind CSS**: For styling and responsive design
- **Clerk**: For authentication and user management
- **Axios**: For API requests
- **React-Toastify**: For displaying notifications
- **QuillJS**: Rich text editor for course descriptions
- **YouTube Player**: For video content delivery

### Backend
- **Node.js**: Runtime environment
- **Express**: Web application framework
- **MongoDB**: NoSQL database with Mongoose ODM
- **Clerk API**: User authentication and management
- **Stripe API**: Payment processing
- **Cloudinary**: Cloud storage for images and media
- **JWT**: For secure API authentication
- **Multer**: For file uploads

## 🏗️ Architecture

CourseMatrix follows a modern client-server architecture:

1. **Client**: React-based SPA (Single Page Application) deployed on Vercel at [course-matrix-frontend.vercel.app](https://course-matrix-frontend.vercel.app/)
2. **Server**: Express API deployed on Vercel Serverless Functions at [course-matrix-backend.vercel.app](https://course-matrix-backend.vercel.app/)
3. **Database**: MongoDB Atlas for data persistence
4. **Authentication**: Clerk for user management and auth flows
5. **Payment**: Stripe for secure payment processing
6. **Storage**: Cloudinary for media assets

## 📸 Screenshots

![Home Page](https://github.com/user-attachments/assets/8f0ebc88-3bfe-410d-a489-316c7dd1c6af)
![Course Listing](https://github.com/user-attachments/assets/24d28678-474f-4a8f-a24f-874ea46f1edd)
![Course Details](https://github.com/user-attachments/assets/98d3f9c8-5c4e-4832-b386-6dd65714ba79)

### Educator Views:
![Educator Dashboard](https://github.com/user-attachments/assets/2d1bfbef-803b-4471-b351-b3b3d5f822e6)
![Add Course Page](https://github.com/user-attachments/assets/b8ecead1-4f10-4a96-b3fd-e1938fa3b699)
![My Courses Page](https://github.com/user-attachments/assets/04a3ee25-66e8-4d4c-acef-bffc4c9a4059)
![Students Enrolled Page](https://github.com/user-attachments/assets/94cbcefb-4d38-4f39-b551-7ceb31f52590)

## 🚀 Installation & Setup

### Prerequisites
- Node.js (v16 or higher)
- MongoDB Atlas account
- Clerk account
- Stripe account
- Cloudinary account

### Client Setup
```bash
# Clone the repository
git clone https://github.com/yourusername/coursematrix.git
cd coursematrix/client

# Install dependencies
npm install

# Create .env file with necessary environment variables
touch .env
# Add the following variables to .env
# VITE_CLERK_PUBLISHABLE_KEY=your_clerk_key
# VITE_BACKEND_URL=http://localhost:5000
# VITE_CURRENCY=$

# Start development server
npm run dev
```

### Server Setup
```bash
# Navigate to server directory
cd ../server

# Install dependencies
npm install

# Create .env file with necessary environment variables
touch .env
# Add the following variables to .env
# PORT=5000
# MONGODB_URI=your_mongodb_connection_string
# CLERK_SECRET_KEY=your_clerk_secret
# CLERK_WEBHOOK_SECRET=your_clerk_webhook_secret
# CLOUDINARY_NAME=your_cloudinary_name
# CLOUDINARY_API_KEY=your_cloudinary_key
# CLOUDINARY_SECRET_KEY=your_cloudinary_secret
# STRIPE_SECRET_KEY=your_stripe_secret
# STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret
# CURRENCY=USD

# Start development server
npm run server
```

## 💻 Usage

### Student Flow
1. Browse available courses on the homepage
2. Search for specific topics using the search bar
3. View detailed course information, including curriculum and reviews
4. Create an account or log in to enroll in courses
5. Purchase courses through secure checkout
6. Access enrolled courses through the "My Enrollments" dashboard
7. Watch lectures and track progress
8. Rate courses after completion

### Educator Flow
1. Log in and select "Become Educator" to gain creator privileges
2. Create courses through the intuitive course builder
3. Organize content into chapters and lectures
4. Upload course thumbnails and add detailed descriptions
5. Set pricing and discount options
6. Monitor enrollments and revenue through the educator dashboard
7. Track student progress and engagement metrics

## 📚 API Documentation

### Course Endpoints
- `GET /api/course/all` - Get all published courses
- `GET /api/course/:id` - Get course details by ID

### User Endpoints
- `GET /api/user/data` - Get user profile data
- `GET /api/user/enrolled-courses` - Get user's enrolled courses
- `POST /api/user/purchase` - Purchase a course
- `POST /api/user/update-course-progress` - Update lecture completion status
- `POST /api/user/get-course-progress` - Get user's progress in a course
- `POST /api/user/add-rating` - Add or update course rating

### Educator Endpoints
- `GET /api/educator/update-role` - Upgrade user to educator status
- `POST /api/educator/add-course` - Create a new course
- `GET /api/educator/courses` - Get all courses created by educator
- `GET /api/educator/dashboard` - Get educator dashboard statistics
- `GET /api/educator/enrolled-students` - Get all enrolled students data

## 🔮 Future Enhancements

- **Live Sessions**: Real-time video classes between educators and students
- **Discussion Forums**: Community engagement for each course
- **Certificates**: Course completion certificates
- **Subscription Model**: Monthly subscription option for accessing multiple courses
- **Mobile App**: Native mobile applications for iOS and Android
- **Advanced Analytics**: Detailed insights for educators to optimize content
- **Affiliate Program**: Allow users to earn by referring others

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Contact

Mary Ashwitha Gopu - [maryashwithagopu@gmail.com](mailto:maryashwithagopu@gmail.com)

Project Links:
- Live Frontend: [https://course-matrix-frontend.vercel.app/](https://course-matrix-frontend.vercel.app/)
- Live Backend: [https://course-matrix-backend.vercel.app/](https://course-matrix-backend.vercel.app/)
- Repository: [https://github.com/ashwithamary/coursematrix](https://github.com/ashwithamary/coursematrix)

## 💪 Skills Demonstrated

- **Frontend Development**: React, React Router, Context API, Tailwind CSS
- **Backend Development**: Node.js, Express, RESTful API design
- **Database**: MongoDB schema design, Mongoose ODM
- **Authentication**: Implementation of third-party auth with Clerk
- **Payment Processing**: Stripe integration with webhook handling
- **Cloud Services**: Cloudinary for media storage
- **Deployment**: CI/CD with Vercel for both frontend and backend
---

Made with ❤️ by Mary Ashwitha Gopu
