<div align="center">

# Hi, I'm Nam Nguyen

**.NET Backend Developer (Fresher)** · ASP.NET Core · PostgreSQL · AI/RAG Integration

I build REST APIs, design relational databases and wire backend services into real web & mobile products.

[![Email](https://img.shields.io/badge/Email-namnm309%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:namnm309@gmail.com)
![Focus](https://img.shields.io/badge/Focus-.NET%20Backend-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Open to work](https://img.shields.io/badge/Open%20to-Fresher%20%2F%20Junior%20roles-2EA44F?style=flat-square)

</div>

---

## About me

- Software Engineering student at **FPT University** (final semesters).
- **FPT Software internship (OJT)** — team project: cinema ticket booking platform.
- **Team lead** for my capstone project (IQGS) — task breakdown, Git workflow, code review, integrating BE / FE / AI service.
- Comfortable with **layered / Clean Architecture** (Domain · Application · Infrastructure · API), EF Core migrations, JWT auth and third-party integrations (VNPay, SePay, GHN, Clerk).
- Ship what I build: CI with **GitHub Actions**, deploys to **Azure App Service**, Docker for local services.

---

## Tech stack

**Backend & databases**

[![Backend](https://skillicons.dev/icons?i=cs,dotnet,postgres,redis,supabase,python,fastapi,java,spring&perline=9)](https://skillicons.dev)

**Frontend & mobile**

[![Frontend](https://skillicons.dev/icons?i=ts,js,react,nextjs,tailwind,html,css&perline=9)](https://skillicons.dev)

**DevOps & tools**

[![Tools](https://skillicons.dev/icons?i=git,github,githubactions,docker,azure,vercel,postman,vscode,visualstudio&perline=9)](https://skillicons.dev)

| Area | Technologies |
| --- | --- |
| **Backend (main)** | C#, **ASP.NET Core Web API** (.NET 8), ASP.NET Core MVC / Razor, **Entity Framework Core**, LINQ, AutoMapper, FluentValidation, Serilog |
| **Database & cache** | **PostgreSQL**, SQL Server, **pgvector**, Redis, Supabase |
| **Auth & realtime** | JWT, Google OAuth, Clerk (webhooks via Svix), **SignalR** |
| **Background & files** | **Hangfire**, Azure Blob Storage, Cloudinary, MailKit, PDF/DOCX parsing |
| **Payments & 3rd-party** | VNPay, MoMo, SePay webhooks, GHN shipping API |
| **Testing** | xUnit, Moq, Testcontainers (PostgreSQL integration tests) |
| **AI** | Python, **FastAPI**, RAG, embeddings, vector search, Ollama, ChromaDB |
| **Frontend & mobile** | TypeScript, React, **Next.js**, Tailwind CSS, shadcn/ui, **React Native (Expo)** |
| **Also used** | Java, Spring Boot (Spring Security, JPA), JSP/Servlet |

---

## Featured projects

### IQGS — AI-Powered Interview Question Generation System · *Capstone (Team Lead)*

![.NET](https://img.shields.io/badge/.NET%208-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%20%2B%20pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Hangfire](https://img.shields.io/badge/Hangfire-5C2D91?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

Dual-sided SaaS for recruiters and job seekers: upload JDs / CVs, generate interview plans and question sets grounded in a knowledge base via RAG, candidate practice & coaching, subscription plans.

- ASP.NET Core Web API in **Clean Architecture**, ~45 controllers split by role (Admin / HR / Candidate / Studio).
- **PostgreSQL + pgvector**, **Hangfire** background jobs for long-running AI generation, Azure Blob for documents, SePay subscription payments.
- Separate **Python FastAPI RAG service** (ingest → chunk → embed → retrieve by scope → generate), called by the .NET backend through an internal API key.
- Unit tests (xUnit, Moq) and integration tests with **Testcontainers**; CI/CD deploy workflow.

[Backend](https://github.com/hienn12454/IQGS-SEP490-Backend) · [RAG / LLM Service](https://github.com/namnm309/IQGS-SEP490-RAG-LLM-SERVICE) · [RAG prototype](https://github.com/namnm309/RAG_IQGS)

### Finmate — Personal Finance Platform · *Backend + Web + Mobile*

![.NET](https://img.shields.io/badge/.NET%208-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Clerk](https://img.shields.io/badge/Clerk-6C47FF?style=flat-square&logo=clerk&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React Native](https://img.shields.io/badge/React%20Native-20232A?style=flat-square&logo=react&logoColor=61DAFB)

Track income/expenses, money sources, savings books and goals; community feed with follows; premium plans paid through SePay.

- 3-layer .NET API (Controller · BLL · DAL), EF Core migrations, **Clerk JWT** auth + Clerk webhooks.
- **SignalR** hub for real-time transaction updates, **SePay webhook** for premium orders.
- Deployed on **Azure App Service** via GitHub Actions; Next.js web dashboard and Expo mobile app.

[Backend](https://github.com/namnm309/Finmate-BE) ([Swagger](https://finmatecontroller20260116165929-dvckfkfvgqendpbk.eastasia-01.azurewebsites.net/swagger/index.html)) · [Web](https://github.com/namnm309/FinmateWeb) ([Live](https://finmate-web-five.vercel.app)) · [Mobile](https://github.com/namnm309/Finmate-Mobile)

### Cinema Ticket Booking — *FPT Software Internship (team)*

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Cloudinary](https://img.shields.io/badge/Cloudinary-3448C5?style=flat-square&logo=cloudinary&logoColor=white)

Movies, showtimes, cinema rooms, real-time seat selection, vouchers, concessions, points and payments.

- Real-time seat locking with **SignalR** + background service that releases expired seats.
- Redis caching, Cloudinary image upload, MVC/Razor admin areas; xUnit + Moq tests.
- Contributed backend features, Razor pages, branch merging and integration debugging.

[Repository](https://github.com/namnm309/OJT_SUMMER25_MOVIEWEBSITE)

### TechStore — E-commerce Backend & Mobile App

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![VNPay](https://img.shields.io/badge/VNPay-005BAA?style=flat-square)
![GHN](https://img.shields.io/badge/GHN-F26522?style=flat-square)
![React Native](https://img.shields.io/badge/React%20Native-20232A?style=flat-square&logo=react&logoColor=61DAFB)

Products & variants, cart, orders, vouchers, membership, wishlist, reviews, support chat.

- **VNPay** payment, **GHN** shipping + webhook, Clerk auth; deployed to Azure with GitHub Actions.

[Backend](https://github.com/namnm309/PRM392-Mobile-BE) ([Swagger](https://techstorebe-fzaza5cvgbhah6fg.eastasia-01.azurewebsites.net/swagger/index.html)) · [Mobile](https://github.com/namnm309/PRM392-Mobile)

---

## Other projects

| Project | What it does | Stack |
| --- | --- | --- |
| [EV Charging Station Management](https://github.com/namnm309/EV_Station_Management) | Stations, charging spots & sessions, reservations, QR, maintenance, subscriptions, VNPay/MoMo | ASP.NET Core, EF Core, PostgreSQL, SignalR |
| [FPTU Lab Events](https://github.com/namnm309/FPTU_Lab_Events) | Lab, room, equipment & event booking with notifications | ASP.NET Core, Clean Architecture, Redis, GitHub Actions |
| [Child Growth Tracking](https://github.com/namnm309/Child_Growth_Tracking_System_BE) | Growth records, BMI vs WHO data, doctor consultations, paid packages | ASP.NET Core, PostgreSQL, Redis, VNPay, Docker |
| [Child Vaccination Scheduling](https://github.com/namnm309/SWP391O-Online-System-for-Child-Vaccination-Schedule-Management) | Vaccination booking for parents, staff & admin | Spring Boot, Spring Security, PostgreSQL, Next.js |
| [Saga Pattern Demo](https://github.com/namnm309/Saga_Pattern_Orchestration_Demo) | Orchestrated multi-step workflow with compensation on failure | .NET 8, Minimal API, Next.js |
| [Microservice Web](https://github.com/namnm309/Microservice-Web) | API gateway + user / movie / booking services (learning project) | ASP.NET Core, PostgreSQL |
| [Ninja Street 3D – web](https://github.com/namnm309/NinjaStreet3D) | Companion site: login, score submission, leaderboard | Next.js, TypeScript |

<details>
<summary>Earlier coursework (Java)</summary>

Hotel / Tour / Event management apps, MVC architecture with JSP/Servlet, Spring Boot practice and JUnit test cases.

</details>

---

## Currently

- Deepening backend fundamentals: database design & transactions, API reliability, testing.
- Looking for a **Fresher / Junior .NET Backend** position.

<div align="center">

**Backend first — comfortable collaborating across the stack.**

</div>
