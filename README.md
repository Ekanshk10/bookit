
# BookIt: Experiences & Slots - backend

A responsive, end-to-end web application for browsing, scheduling, and booking travel experiences, built to demonstrate full-stack proficiency, API integration, and clean UI design.

## Application is Live on ##

| Service      | URL                                                                                  |
| ------------ | ------------------------------------------------------------------------------------ |
| **Frontend** | [https://bookit-frontend-ten.vercel.app](https://bookit-frontend-ten.vercel.app)     |
| **Backend**  | [https://bookit-backend-wk1r.onrender.com](https://bookit-backend-wk1r.onrender.com/api/experiences) |


## Github Repositories ##

| Project      | Repository                                                                                   |
| ------------ | -------------------------------------------------------------------------------------------- |
| **Frontend** | [https://github.com/Ekanshk10/bookit-frontend](https://github.com/Ekanshk10/bookit-frontend) |
| **Backend**  | [https://github.com/Ekanshk10/bookit-backend](https://github.com/Ekanshk10/bookit-backend)   |

## 💡 Project Objectives & Technical Highlights

**🎯 Objective Fulfillment**

🎨 Pixel-perfect UI — Matched Figma design for both mobile & desktop using TailwindCSS

🔐 Booking Integrity — Promo code validation (CODE100, CODE200) + strict double-booking prevention

🔁 Smooth Flow — Completed end-to-end journey:
Home → Details → Checkout → Result with real-time data updates

🧠 Key Technical Challenges & Learnings
⚙️ API Architecture

Structured REST API for:

👤 Experiences

🕒 Slot availability & booking capacity

🎟️ Promo & discount validation

Full validation + safe transaction handling

⚡ State Management

Efficient multi-step form handling using React hooks

Smooth UX with proper loading, error feedback, and toast alerts

🌐 SSR, Hydration & SEO

Implemented Next.js Server-Side Rendering

Fetched data server-side & passed as props for:

Faster first paint

Better SEO

Avoided hydration mismatches by sanitizing date values and ensuring timezone consistency
## Tech Stack
a) Frontend:-

    1) Next.js (App Router, SSR, Dynamic Routing)

    2) React + TailwindCSS

    3) Axios for API communication

b) Backend

    1) Express.js REST API

    2)Prisma ORM

    3) PostgreSQL (Neon DB Hosting)

c) Deployment & Tools

    1)Database: Neon PostgreSQL Cloud

    2) Frontend: Vercel

    3) Backend: Render

    4) API Testing: Postman
## 🚀 Installation & Setup

```
mkdir bookit-Ekansh
cd bookit-Ekansh
```

# Clone Backend
git clone <https://github.com/Ekanshk10/bookit-backend> 

```backend
cd backend
npm install
npm run dev
``` 

# Clone Frontend
git clone <https://github.com/Ekanshk10/bookit-frontend> 

```frontend
cd frontend
npm install
npm run dev 
```

# Database Setup
```
cd backend
npx prisma migrate dev
```

# You can now access

| Service            | URL                                            |
| ------------------ | ---------------------------------------------- |
| Frontend (Next.js) | [http://localhost:3000](http://localhost:3000) |
| Backend API        | [http://localhost:1002/api](http://localhost:5000) |

## Environment Variables

To run this project, you will need to add the following environment variables to your .env file 

a) Backend

    DATABASE_URL = 'postgresql://neondb_owner:npg_pOWo1HzJUQ3h@ep-nameless-field-a14z02zz-pooler.ap-southeast-1.aws.neon.tech/neondb?sslmode=require&channel_binding=require


b) Frontend

    NEXT_PUBLIC_API_URL = 'http://localhost:1002/api' 


## API Reference

#### Get all Experiences

```http
  GET /api/experiences
```

#### Get Experiences

```http
  GET /api/experiences/${id}
```

| Parameter |  Description                       |
| :-------- |  :-------------------------------- |
| `id`      |**Required**. Id of item to fetch |

```http
  POST /api/booking
```

| Parameter         | Type   | Required | Description                               |
| ------------- | ------ | -------- | ----------------------------------------- |
| `name`        | string | ✅ Yes    | Customer full name                        |
| `email`       | string | ✅ Yes    | Customer email                            |
| `codeId`      | number | ❌ No     | Applied promo/discount code ID            |
| `bookingDate` | string | ✅ Yes    | User booking creation date (`YYYY-MM-DD`) |
| `finalPrice`  | number | ✅ Yes    | Final amount after discount               |
| `exprienceId` | number | ✅ Yes    | Experience ID being booked                |
| `slotDate`    | date | ✅ Yes    | Date of the experience (`YYYY-MM-DD`)     |
| `slotTime`    | string | ✅ Yes    | Time slot (e.g. `"07:00 AM"`)             |
| `quantity`    | number | ✅ Yes    | Number of seats/persons                   |

```http
    GET /api/promo
```

```http
    POST /api/promo/validate
```
| Field          | Type   | Required | Description             |
| -------------- | ------ | -------- | ----------------------- |
| `code`         | string | ✅        | Promo code              |
| `bookingValue` | number | ✅        | Original booking amount |

**Promo codes available to validate : code100 & code200**


## 👨‍💻 Author

**Ekansh Kanot**

- GitHub: [@Ekanshk10](https://github.com/Ekanshk10)
- LinkedIn: https://www.linkedin.com/in/ekansh-kanot
- Portfolio: *coming soon*

## License

[MIT](https://choosealicense.com/licenses/mit/)

