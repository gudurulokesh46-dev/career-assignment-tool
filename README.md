# Career Assignment Tool

A comprehensive web-based career assignment tool for students featuring user authentication, assignment submission, and AI-powered career recommendations.

## Features

- **Student Authentication**: Secure login and registration system
- **Assignment Management**: Create, submit, and manage assignments
- **Career Recommendations**: AI-powered career suggestions based on assignment performance
- **Admin Dashboard**: Manage students, assignments, and view analytics
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT Authentication
- bcryptjs for password hashing

### Frontend
- HTML5
- CSS3
- JavaScript (Vanilla)
- Responsive Design

## Project Structure

```
career-assignment-tool/
├── server.js
├── package.json
├── .env.example
├── models/
│   ├── User.js
│   ├── Assignment.js
│   └── Submission.js
├── routes/
│   ├── auth.js
│   ├── assignments.js
│   └── submissions.js
├── middleware/
│   └── auth.js
├── public/
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
│   ├── css/
│   │   └── style.css
│   └── js/
│       ├── auth.js
│       ├── dashboard.js
│       └── assignments.js
└── README.md
```

## Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### Steps

1. Clone the repository:
```bash
git clone https://github.com/gudurulokesh46-dev/career-assignment-tool.git
cd career-assignment-tool
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory:
```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/career-assignment-tool
JWT_SECRET=your_jwt_secret_key_here
```

4. Start MongoDB (if running locally):
```bash
mongod
```

5. Start the development server:
```bash
npm run dev
```

6. Open your browser and navigate to:
```
http://localhost:3000
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register a new student
- `POST /api/auth/login` - Login student
- `GET /api/auth/profile` - Get student profile (protected)

### Assignments
- `GET /api/assignments` - Get all assignments
- `GET /api/assignments/:id` - Get single assignment
- `POST /api/assignments` - Create new assignment (admin)
- `PUT /api/assignments/:id` - Update assignment (admin)
- `DELETE /api/assignments/:id` - Delete assignment (admin)

### Submissions
- `POST /api/submissions` - Submit assignment
- `GET /api/submissions/student/:studentId` - Get student submissions
- `GET /api/submissions/assignment/:assignmentId` - Get assignment submissions
- `PUT /api/submissions/:id/grade` - Grade submission (admin)

### Career Recommendations
- `GET /api/recommendations/:studentId` - Get career recommendations based on performance

## Usage

### For Students:
1. Register with email and password
2. Login to access your dashboard
3. View available assignments
4. Submit assignments with your responses
5. View graded assignments and career recommendations

### For Administrators:
1. Login with admin credentials
2. Create and manage assignments
3. Grade student submissions
4. View student performance analytics

## Career Recommendation Algorithm

The system analyzes:
- Assignment scores
- Subject preferences
- Performance trends
- Skills demonstrated

Based on this data, it recommends career paths from categories including:
- Technology (Software Development, Data Science, etc.)
- Engineering (Mechanical, Electrical, Civil, etc.)
- Medicine (Doctor, Nurse, Pharmacist, etc.)
- Business (Management, Marketing, Finance, etc.)
- Arts (Design, Writing, Music, etc.)

## Environment Variables

```env
PORT=3000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
NODE_ENV=development
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

MIT License - feel free to use this project for learning and development.

## Author

Developed by gudurulokesh46-dev

## Support

For issues and questions, please open an issue in the GitHub repository.

---

**Note**: This is an educational project. For production use, implement additional security measures, input validation, and error handling.
