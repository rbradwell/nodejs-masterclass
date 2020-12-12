# [Brad Traversy] Node.js API Masterclass With Express &amp; MongoDB [2019, ENG]

**Original src:**  
https://github.com/bradtraversy/devcamper-api

---

<br/>

## 2. HTTP Intro - Headers, Body, Status Codes, etc

<br/>

## 3. Starting Our DevCamper Project

<br/>

### 2. Basic Express Server, dotenv & Git

    $ cd api
    $ npm init -y

    $ npm install --save express dotenv
    $ npm install --save-dev nodemon

    $ npm run dev

<br/>

### 3. Creating Routes & Responses In Express

<br/>

![Application](/img/pic-02-01.png?raw=true)

<br/>

### 4. Using The Express Router

<br/>

### 5. Creating Controller Methods

<br/>

### 6. Intro To Middleware

    $ npm install --save-dev morgan

<br/>

### 7. Postman Environment & Collections

<br/>

## 4. Getting Started With MongoDB & Bootcamps Resource

<br/>

### 1. MongoDB Atlas & Compass Setup

We made an account on mongodb.com

<br/>

### 2. Connecting To The Database With Mongoose

    $ npm install --save mongoose

<br/>

    MongoDB Connected: traversy-node-js-api-masterclass-shard-00-02-9n706.mongodb.net

<br/>

### 3. Colors In The Console

    $ npm install --save colors

<br/>

### 4. Creating Our First Model

<br/>

### 5. Create Bootcamp - POST

    $ curl -d '{
      "user": "5d7a514b5d2c12c7449be045",
    	"name": "Devworks Bootcamp",
    	"description": "Devworks is a full stack JavaScript Bootcamp located in the heart of Boston that focuses on the technologies you need to get a high paying job as a web developer",
    	"website": "https://devworks.com",
    	"phone": "(111) 111-1111",
    	"email": "enroll@devworks.com",
    	"address": "233 Bay State Rd Boston MA 02215",
    	"careers": ["Web Development", "UI/UX", "Business"],
    	"housing": true,
    	"jobAssistance": true,
    	"jobGuarantee": false,
    	"acceptGi": true
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps \
    | python -m json.tool

<br/>

    $ curl -d '{
      "user": "5d7a514b5d2c12c7449be046",
    	"name": "ModernTech Bootcamp",
      "description": "ModernTech has one goal, and that is to make you a rockstar developer and/or designer with a six figure salary. We teach both development and UI/UX",
      "website": "https://moderntech.com",
      "phone": "(222) 222-2222",
      "email": "enroll@moderntech.com",
      "address": "220 Pawtucket St, Lowell, MA 01854",
      "careers": ["Web Development", "UI/UX", "Mobile Development"],
      "housing": false,
      "jobAssistance": true,
      "jobGuarantee": false,
      "acceptGi": true
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps \
    | python -m json.tool

<br/>

    $ curl -d '{
      "user": "5c8a1d5b0190b214360dc031",
    	"name": "Codemasters",
    	"description": "Is coding your passion? Codemasters will give you the skills and the tools to become the best developer possible. We specialize in full stack web development and data science",
    	"website": "https://codemasters.com",
    	"phone": "(333) 333-3333",
    	"email": "enroll@codemasters.com",
    	"address": "85 South Prospect Street Burlington VT 05405",
    	"careers": ["Web Development", "Data Science", "Business"],
    	"housing": false,
    	"jobAssistance": false,
    	"jobGuarantee": false,
    	"acceptGi": false
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps \
    | python -m json.tool

<br/>

    $ curl -d '{
      "user": "5c8a1d5b0190b214360dc032",
    	"name": "Devcentral Bootcamp",
    	"description": "Is coding your passion? Codemasters will give you the skills and the tools to become the best developer possible. We specialize in front end and full stack web development",
    	"website": "https://devcentral.com",
    	"phone": "(444) 444-4444",
    	"email": "enroll@devcentral.com",
    	"address": "45 Upper College Rd Kingston RI 02881",
    	"careers": [
        "Mobile Development",
        "Web Development",
        "Data Science",
        "Business"
      ],
    	"housing": false,
    	"jobAssistance": true,
    	"jobGuarantee": true,
    	"acceptGi": true
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps \
    | python -m json.tool

<br/>

### 6. Fetching Bootcamps - GET

    $ curl \
      -H "Content-Type: application/json" \
      -X GET localhost:5000/api/v1/bootcamps \
      | python -m json.tool

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -X GET localhost:5000/api/v1/bootcamps/5db62fd567c1170dd52c2c34 \
    | python -m json.tool

<br/>

### 7. Updating & Deleting Bootcamps - PUT & DELETE

    $ curl \
    -d '{
    	"housing": true
    }' \
    -H "Content-Type: application/json" \
    -X PUT localhost:5000/api/v1/bootcamps/5db62fd567c1170dd52c2c34 \
    | python -m json.tool

<br/>

    $ curl -d '{
    	"careers": ["UI/UX"]
    }' \
    -H "Content-Type: application/json" \
    -X PUT localhost:5000/api/v1/bootcamps/5db62fd567c1170dd52c2c34 \
    | python -m json.tool

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -X DELETE localhost:5000/api/v1/bootcamps/5db62fd567c1170dd52c2c34 \
    | python -m json.tool

<br/>

## 5. Custom Error Handling & Mongoose Middleware

<br/>

### 1. Error Handler Middleware

<br/>

### 2. Custom ErrorResponse Class

<br/>

### 3. Mongoose Error Handling [1]

<br/>

### 4. Mongoose Error Handling [2]

    $ curl \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps \
    | python -m json.tool

<br/>

### 4. Mongoose Error Handling [2]

<br/>

### 5. AsyncAwait Middleware

<br/>

### 6. Mongoose Middleware & Slugify

    $ npm install --save slugify

We deleted all documents in the database

    $ curl -d '{
      "user": "5d7a514b5d2c12c7449be045",
    	"name": "Devworks Bootcamp",
    	"description": "Devworks is a full stack JavaScript Bootcamp located in the heart of Boston that focuses on the technologies you need to get a high paying job as a web developer",
    	"website": "https://devworks.com",
    	"phone": "(111) 111-1111",
    	"email": "enroll@devworks.com",
    	"address": "233 Bay State Rd Boston MA 02215",
    	"careers": ["Web Development", "UI/UX", "Business"],
    	"housing": true,
    	"jobAssistance": true,
    	"jobGuarantee": false,
    	"acceptGi": true
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps \
    | python -m json.tool

<br/>

```
***
"slug": "devworks-bootcamp",
***
```

<br/>

### 7. GeoJSON Location & Geocoder Hook - MapQuest API

register

https://developer.mapquest.com/

Manage Keys --> My Application's Key --> Consumer Key --> insert to config

<br/>

    $ npm install --save node-geocoder

<br/>

We deleted all documents in the database

<br/>

    $ curl -d '{
      "user": "5d7a514b5d2c12c7449be045",
    	"name": "Devworks Bootcamp",
    	"description": "Devworks is a full stack JavaScript Bootcamp located in the heart of Boston that focuses on the technologies you need to get a high paying job as a web developer",
    	"website": "https://devworks.com",
    	"phone": "(111) 111-1111",
    	"email": "enroll@devworks.com",
    	"address": "233 Bay State Rd Boston MA 02215",
    	"careers": ["Web Development", "UI/UX", "Business"],
    	"housing": true,
    	"jobAssistance": true,
    	"jobGuarantee": false,
    	"acceptGi": true
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps \
    | python -m json.tool

<br/ >

## 6. Mongoose Advanced Querying & Relationships

<br/>

### 1. Database Seeder For Bootcamps

    // ImportData
    $ node seeder -i

    // DestroyData
    $ node seeder -d

<br/>

### 2. Geospatial Query - Get Bootcamps Within Radius

    $ curl \
    -H "Content-Type: application/json" \
    -X GET localhost:5000/api/v1/bootcamps/radius/02118/10 \
    | python -m json.tool

<br/>

### 3. Advanced Filtering

    $ curl \
    -H "Content-Type: application/json" \
    -X GET localhost:5000/api/v1/bootcamps?careers[in]=Business \
    | python -m json.tool

<br/>

### 4. Select & Sorting

http://localhost:5000/api/v1/bootcamps?select=name,description,housing&housing=true

<br/>

http://localhost:5000/api/v1/bootcamps?select=name,description,housing&sort=name

<br/>

http://localhost:5000/api/v1/bootcamps?select=name,description,housing&sort=-name

<br/>

### 5. Adding Pagination

http://localhost:5000/api/v1/bootcamps?page=2

<br/>

### 6. Course Model & Seeding

    // DestroyData
    $ node seeder -d

    // ImportData
    $ node seeder -i

<br/>

### 7. Course Routes & Controller

http://localhost:5000/api/v1/courses

http://localhost:5000/api/v1/bootcamps/5d713995b721c3bb38c1f5d0/courses

<br/>

### 8. Populate, Virtuals & Cascade Delete

http://localhost:5000/api/v1/bootcamps

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -X DELETE localhost:5000/api/v1/bootcamps/5d725a1b7b292f5f8ceff788 \
    | python -m json.tool

<br/>

### 9. Single Course & Add Course

http://localhost:5000/api/v1/courses/5d725a4a7b292f5f8ceff789

http://localhost:5000/api/v1/bootcamps/

<br/>

    $ curl -d '{
      "title": "Front End Web Development",
      "description": "This course will provide you with all of the essentials to become a successful frontend web developer. You will learn to master HTML, CSS and front end JavaScript, along with tools like Git, VSCode and front end frameworks like Vue",
      "weeks": 8,
      "tuition": 8000,
      "minimumSkill": "beginner",
      "scholarhipsAvailable": true
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps/5d713995b721c3bb38c1f5d0/courses \
    | python -m json.tool

<br/>

    $ curl -d '{
      "title": "Full Stack Web Development",
      "description": "In this course you will learn full stack web development, first learning all about the frontend with HTML/CSS/JS/Vue and then the backend with Node.js/Express/MongoDB",
      "weeks": 12,
      "tuition": 10000,
      "minimumSkill": "intermediate",
      "scholarhipsAvailable": true
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/bootcamps/5d713995b721c3bb38c1f5d0/courses \
    | python -m json.tool

<br/>

http://localhost:5000/api/v1/bootcamps/

<br/>

### 10. Update & Delete Course

    // DestroyData
    $ node seeder -d

    // ImportData
    $ node seeder -i

<br/>

http://localhost:5000/api/v1/courses

<br/>

    $ curl -d '{
    	"tuition": 13000,
      "minimumSkill": "advanced"
    }' \
    -H "Content-Type: application/json" \
    -X PUT localhost:5000/api/v1/courses/5d725a4a7b292f5f8ceff789 \
    | python -m json.tool

<br/>

http://localhost:5000/api/v1/courses/5d725a4a7b292f5f8ceff789

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -X DELETE localhost:5000/api/v1/courses/5d725a4a7b292f5f8ceff789 \
    | python -m json.tool

<br/>

### 11. Aggregate - Calculating The Average Course Cost

<br/>

### 12. Photo Upload For Bootcamp

<br/>

    $ npm install --save express-fileupload

<br/>

    $ curl \
    -F "file=@/home/marley/1/pic1.jpg" \
    -X PUT localhost:5000/api/v1/bootcamps/5d725a1b7b292f5f8ceff788/photo \
    | python -m json.tool

<br/>

http://localhost:5000/uploads/photo_5d725a1b7b292f5f8ceff788.jpg

<br/>

![Application](/img/pic-06-12.png?raw=true)

<br/>

### 13. Advanced Results Middleware

http://localhost:5000/api/v1/bootcamps/

http://localhost:5000/api/v1/bootcamps?page=2

http://localhost:5000/api/v1/bootcamps?select=name,description

http://localhost:5000/api/v1/courses?select=title

http://localhost:5000/api/v1/courses?page=2&limit=2

<br/>

## 7. Authentication, Users & Permissions - Part 1

<br/>

### 1. User Model

    $ npm install --save jsonwebtoken
    $ npm install --save bcryptjs

<br/>

### 2. User Register & Encrypting Passwords

<br/>

    $ curl \
    -d '{"name": "John Doe",
         "email": "john@gmail.com",
         "password": "123456",
         "role": "publisher"}' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/register \
    | python -m json.tool

<br/>

### 3. Sign & Get JSON Web Token

https://jwt.io/

    $ curl \
    -d '{"name": "John Doe",
         "email": "john@gmail.com",
         "password": "123456",
         "role": "publisher"}' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/register \
    | python -m json.tool

<br/>

### 4. User Login

    $ curl \
    -d '{
         "email": "john@gmail.com",
         "password": "123456"
         }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/login \
    | python -m json.tool

<br/>

### 5. Sending JWT In a Cookie

    $ npm install --save cookie-parser

<br/>

### 6. Auth Protect Middleware

    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkYmI0YTg5OWE1ODE1M2ZmNjEzYWEzOSIsImlhdCI6MTU3MjU1NTQwMSwiZXhwIjoxNTc1MTQ3NDAxfQ.2G0jVvVPpHPem-SEGLGg3-_JMmYqnOsIuY3RjhVkfQY"

<br/>

    $ curl -d '{
      "user": "5d7a514b5d2c12c7449be045",
    	"name": "Devworks Bootcamp",
    	"description": "Devworks is a full stack JavaScript Bootcamp located in the heart of Boston that focuses on the technologies you need to get a high paying job as a web developer",
    	"website": "https://devworks.com",
    	"phone": "(111) 111-1111",
    	"email": "enroll@devworks.com",
    	"address": "233 Bay State Rd Boston MA 02215",
    	"careers": ["Web Development", "UI/UX", "Business"],
    	"housing": true,
    	"jobAssistance": true,
    	"jobGuarantee": false,
    	"acceptGi": true
    }' \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkYmI0YTg5OWE1ODE1M2ZmNjEzYWEzOSIsImlhdCI6MTU3MjU1NTQwMSwiZXhwIjoxNTc1MTQ3NDAxfQ.2G0jVvVPpHPem-SEGLGg3-_JMmYqnOsIuY3RjhVkfQY" \
    -X POST localhost:5000/api/v1/bootcamps \
    | python -m json.tool

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkYmI0YTg5OWE1ODE1M2ZmNjEzYWEzOSIsImlhdCI6MTU3MjU1NTQwMSwiZXhwIjoxNTc1MTQ3NDAxfQ.2G0jVvVPpHPem-SEGLGg3-_JMmYqnOsIuY3RjhVkfQY" \
    -X GET localhost:5000/api/v1/auth/me \
    | python -m json.tool

<br/>

### 7. Storing The Token In Postman

<br/>

### 8. Role Authorization

Only user 'publisher' and 'admin' can do actions to create / update / delete

<br/>

## 8. Authentication, Users & Permissions - Part 2

<br/>

### 1. Bootcamp & User Relationship

    // DestroyData
    $ node seeder -d

    // ImportData
    $ node seeder -i

<br/>

http://localhost:5000/api/v1/bootcamps/

<br/>

### 2. Bootcamp Ownership

Only onwer or admin can modify bootcamp

<br/>

### 3. Course Ownership

Only onwer or admin can modify course

<br/>

### 4. Forgot Password - Generate Token

    $ curl \
    -d '{
      "email": "john@gmail.com"
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/forgotpassword \
    | python -m json.tool

<br/>

### 5. Forgot Password - Send Email

https://mailtrap.io/  
http://nodemailer.com/about/

    $ npm install --save nodemailer

<br/>

    $ curl \
    -d '{
      "email": "john@gmail.com"
    }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/forgotpassword \
    | python -m json.tool

<br/>

![Application](/img/pic-08-05-01.png?raw=true)

<br/>

![Application](/img/pic-08-05-02.png?raw=true)

<br/>

### 6. Reset Password

    $ curl \
    -d '{
      "password": "654321"
    }' \
    -H "Content-Type: application/json" \
    -X PUT http://localhost:5000/api/v1/auth/resetpassword/bcedda5593f1799bd34ba1a49608f92a0434d154 \
    | python -m json.tool

<br/>

    // Invalid
    $ curl \
    -d '{
         "email": "john@gmail.com",
         "password": "123456"
         }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/login \
    | python -m json.tool

<br/>

    // Valid
    $ curl \
    -d '{
         "email": "john@gmail.com",
         "password": "654321"
         }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/login \
    | python -m json.tool

eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk

<br/>

### 7. Update User Details

    $ curl \
    -d '{
         "email": "john@gmail.com",
         "name": "John Smith"
         }' \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X PUT localhost:5000/api/v1/auth/updatedetails \
    | python -m json.tool

<br/>

    $ curl \
    -d '{
         "currentPassword": "654321",
         "newPassword": "123456"
         }' \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X PUT localhost:5000/api/v1/auth/updatepassword \
    | python -m json.tool

<br/>

### 8. Admin Users CRUD

mongodb -> set role "admin" to user.

<br/>

    // Me
    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X GET localhost:5000/api/v1/auth/me \
    | python -m json.tool

<br/>

    // Get all user
    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X GET localhost:5000/api/v1/users \
    | python -m json.tool

<br/>

    // Get single user
    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X GET localhost:5000/api/v1/users/5c8a1d5b0190b214360dc032 \
    | python -m json.tool

<br/>

    // Get single user
    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X GET localhost:5000/api/v1/users/5c8a1d5b0190b214360dc032 \
    | python -m json.tool

<br/>

    // Create user
    $ curl \
    -d '{
    	"name": "Nate Smith",
        "email": "nate@gmail.com",
        "password": "123456"
    }' \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X POST localhost:5000/api/v1/users/ \
    | python -m json.tool

<br/>

    // Update user
    $ curl \
    -d '{
    	"name": "Nate Johnson"
    }' \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X PUT localhost:5000/api/v1/users/5dbbd7c42041035e7eb80426 \
    | python -m json.tool

<br/>

    // Delete user
    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVkN2E1MTRiNWQyYzEyYzc0NDliZTA0NSIsImlhdCI6MTU3MjU4NTY1OCwiZXhwIjoxNTc1MTc3NjU4fQ.vhxaMRCksKb0LHx5T91JqrX4xo0i2Im_BOuv3vShmXk" \
    -X DELETE localhost:5000/api/v1/users/5dbbd7c42041035e7eb80426 \
    | python -m json.tool

<br/>

## 9. Bootcamp Reviews & Ratings

<br/>

### 1. Review Model & Get Reviews

<br/>

### 2. Get Single Review & Update Seeder

    // DestroyData
    $ node seeder -d

    // ImportData
    $ node seeder -i

<br/>

    // Get all reviews
    $ curl \
    -H "Content-Type: application/json" \
    -X GET localhost:5000/api/v1/reviews \
    | python -m json.tool

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -X GET localhost:5000/api/v1/reviews/5d7a514b5d2c12c7449be020 \
    | python -m json.tool

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -X GET localhost:5000/api/v1/bootcamps/5d725a1b7b292f5f8ceff788/reviews \
    | python -m json.tool

<br/>

### 3. Add Review For Bootcamp

User with 'publisher' role shouldn't create reviews

    $ curl \
    -d '{
         "email": "greg@gmail.com",
         "password": "123456"
         }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/login \
    | python -m json.tool

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjOGExZDViMDE5MGIyMTQzNjBkYzAzMyIsImlhdCI6MTU3MjYwNjQ5NSwiZXhwIjoxNTc1MTk4NDk1fQ.lgUqJEJDp9dShq4HeA9-CiiTt9zfB-7ZVaRotI928l0" \
    -X GET localhost:5000/api/v1/auth/me \
    | python -m json.tool

<br/>

    $ curl \
    -d '{
         "title": "Nice Bootcamp",
         "text": "I learned a lot",
         "rating": 8
         }' \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjOGExZDViMDE5MGIyMTQzNjBkYzAzMyIsImlhdCI6MTU3MjYwNjQ5NSwiZXhwIjoxNTc1MTk4NDk1fQ.lgUqJEJDp9dShq4HeA9-CiiTt9zfB-7ZVaRotI928l0" \
    -X POST localhost:5000/api/v1/bootcamps/5d725a1b7b292f5f8ceff788/reviews/ \
    | python -m json.tool

<br/>

### 4. Aggregate - Calculate Average Rating

    // DestroyData
    $ node seeder -d

<br/>

    $ curl \
    -d '{"name": "John Doe",
         "email": "john@gmail.com",
         "password": "123456",
         "role": "user"}' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/register \
    | python -m json.tool

<br/>

    $ curl \
    -d '{"name": "Jack Smith",
         "email": "jack@gmail.com",
         "password": "123456",
         "role": "user"}' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/register \
    | python -m json.tool

<br/>

    $ curl \
    -d '{"name": "Mary Smith",
         "email": "mary@gmail.com",
         "password": "123456",
         "role": "user"}' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/register \
    | python -m json.tool

<br/>

    // Login
    $ curl \
    -d '{
         "email": "john@gmail.com",
         "password": "123456"
         }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/login \
    | python -m json.tool

<br/>

Did not test. Need to create a bootcamp, then create review and check average rating for 3 users. User with role 'user' has no premission to create bootcamp.

<br/>

### 5. Update & Delete Reviews

    // DestroyData
    $ node seeder -d

    // ImportData
    $ node seeder -i

<br/>

    // Login
    $ curl \
    -d '{
         "email": "greg@gmail.com",
         "password": "123456"
         }' \
    -H "Content-Type: application/json" \
    -X POST localhost:5000/api/v1/auth/login \
    | python -m json.tool

<br/>

    // Get all reviews
    $ curl \
    -H "Content-Type: application/json" \
    -X GET localhost:5000/api/v1/reviews \
    | python -m json.tool

<br/>

    $ curl \
    -d '{
         "title": "Had Fun",
         "text": "Super",
         "rating": 10
         }' \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjOGExZDViMDE5MGIyMTQzNjBkYzAzMyIsImlhdCI6MTU3MjYwOTE4NiwiZXhwIjoxNTc1MjAxMTg2fQ.3fY2OVWxj7YWxD3vfhr459MX0vb4ewtSm9BU8nWQrfc" \
    -X PUT localhost:5000/api/v1/reviews/5d7a514b5d2c12c7449be020 \
    | python -m json.tool

<br/>

    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjOGExZDViMDE5MGIyMTQzNjBkYzAzMyIsImlhdCI6MTU3MjYwOTE4NiwiZXhwIjoxNTc1MjAxMTg2fQ.3fY2OVWxj7YWxD3vfhr459MX0vb4ewtSm9BU8nWQrfc" \
    -X DELETE localhost:5000/api/v1/reviews/5d7a514b5d2c12c7449be020 \
    | python -m json.tool

<br/>

## 10. API Security

<br/>

### 1. Logout To Clear Token Cookie

    // Logout
    $ curl \
    -H "Content-Type: application/json" \
    -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjVjOGExZDViMDE5MGIyMTQzNjBkYzAzMyIsImlhdCI6MTU3MjYwNjQ5NSwiZXhwIjoxNTc1MTk4NDk1fQ.lgUqJEJDp9dShq4HeA9-CiiTt9zfB-7ZVaRotI928l0" \
    -X GET localhost:5000/api/v1/auth/logout \
    | python -m json.tool

<br/>

### 2. Prevent NoSQL Injection & Sanitize Data

    $ npm install --save express-mongo-sanitize

<br/>

### 3. XSS Protection & Security Headers

https://helmetjs.github.io/

    $ npm install --save helmet

https://github.com/jsonmaur/xss-clean

    $ npm install --save xss-clean

<br/>

### 4. Rate Limiting, HPP & CORS

    $ npm install --save express-rate-limit
    $ npm install --save hpp

https://github.com/expressjs/cors

    $ npm install --save cors

<br/>

## 11. Documentation & Deploy

**Steps to deploy:**  
https://gist.github.com/bradtraversy/cd90d1ed3c462fe3bddd11bf8953a896

<br/>

### 1. Documentation With Postman & Docgen

<br/>

### 2. Digital Ocean Droplet & Server Log In

<br/>

### 3. Prepare & Push To Github

<br/>

### 4. Clone Repo On Server

<br/>

### 5. PM2 Process Manager Setup

<br/>

### 6. NGINX Reverse Proxy Setup

<br/>

### 7. Domain, SSL & Wrap Up


<br/>

---

<br/>

**Marley**

Any questions on eng: https://jsdev.org/chat/  
Любые вопросы на русском: https://jsdev.ru/chat/
# Node.js-API-Masterclass-With-Express-MongoDB
