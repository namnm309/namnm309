<div align="center">

# Hi, I'm Nam Nguyen

**.NET Backend Developer (Fresher)** · ASP.NET Core · PostgreSQL · AI/RAG Integration

I build REST APIs, design relational databases and wire backend services into real web & mobile products.

[![Email](https://img.shields.io/badge/Email-namnm309%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:namnm309@gmail.com)

</div>

---

## Tech stack

**Backend & databases**

[![Backend](https://skillicons.dev/icons?i=cs,dotnet,postgres,redis,supabase,python,fastapi,java,spring&perline=9)](https://skillicons.dev)

**Frontend & mobile**

[![Frontend](https://skillicons.dev/icons?i=ts,js,react,nextjs,tailwind,html,css&perline=9)](https://skillicons.dev)

**DevOps & tools**

[![Tools](https://skillicons.dev/icons?i=git,github,githubactions,docker,azure,vercel,postman,vscode,visualstudio&perline=9)](https://skillicons.dev)

**AI-assisted development**

![Claude Code](https://img.shields.io/badge/Claude%20Code-D97757?style=for-the-badge&logo=claude&logoColor=white)
![Codex](https://img.shields.io/badge/OpenAI%20Codex-412991?style=for-the-badge&logo=openai&logoColor=white)
![Cursor](https://img.shields.io/badge/Cursor-000000?style=for-the-badge&logo=cursor&logoColor=white)
![Antigravity](https://img.shields.io/badge/Google%20Antigravity-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Trae](https://img.shields.io/badge/Trae-FF4F3D?style=for-the-badge)

I use AI coding agents daily to scaffold features, write tests, refactor and review code — while keeping design decisions, data modeling and final review in my own hands.

| Area | Technologies |
| --- | --- |
| **Backend (main)** | C#, **ASP.NET Core Web API** (.NET 8), Razor Pages / MVC, **Entity Framework Core**, LINQ, AutoMapper, FluentValidation, Serilog |
| **Database & cache** | **PostgreSQL**, SQL Server, **pgvector**, Redis, Supabase |
| **Auth & realtime** | JWT, Google OAuth, Clerk (JWKS + webhooks), **SignalR** |
| **Background & files** | **Hangfire**, Azure Blob Storage, Cloudinary, MailKit, ClosedXML (Excel), PDF/DOCX parsing |
| **Payments & 3rd-party** | VNPay, SePay (IPN / webhook), GHN shipping, SerpApi (Google Maps) |
| **Testing** | xUnit, Moq, Testcontainers, pytest |
| **AI** | Python, **FastAPI**, RAG, embeddings, vector search, Ollama, ChromaDB |
| **Frontend & mobile** | TypeScript, React, **Next.js**, Tailwind CSS, shadcn/ui, **React Native (Expo)**, SQLite |
| **Also used** | Java, Spring Boot (Spring Security, JPA, MapStruct) |

---

## Featured projects

### IQGS — AI-Powered Interview Question Generation System
*Capstone project · Team Lead · May – Oct 2026 · my commits: ~165 / 402 (backend) + 24 / 46 (RAG service)*

![.NET](https://img.shields.io/badge/.NET%208-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%20%2B%20pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Hangfire](https://img.shields.io/badge/Hangfire-5C2D91?style=flat-square)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)

Dual-sided SaaS for the Vietnamese IT hiring market. HR uploads a JD and the system builds an interview plan and question sets grounded in a knowledge base (RAG). Candidates practice, get AI scoring and coaching, and can take hiring assessments.

**What I did**
- Set up the backend skeleton in **Clean Architecture (4 layers)** and the solution / CI wiring.
- **HR question generation:** JD upload → async **question generation jobs** with **Hangfire**, job history, question-set CRUD / reorder, save draft, regenerate one question, JD validation before saving.
- **Studio Interview Plan:** plan generation from JD, merge & provenance of topics, tech-skill catalog, AI configuration per studio.
- **Subscription MVP:** **SePay** payment, usage metering and plan limits, admin grant / revoke Premium, cancel-at-period-end logic.
- **Candidate features:** practice-session AI evaluation & feedback, bilingual AI insights, personal practice sets from CV + JD, CV Knowledge Coach & skill plan, anti-cheat rules, Hiring Assessment mode.
- Admin features: RAG service health check, marketplace, platform settings; Google account linking; Excel export of HR history (ClosedXML).
- **RAG / LLM service (Python FastAPI):** rebuilt it on **pgvector** as an internal API — answer evaluation, practice insights, retrieval filters (document IDs, metadata, scope), CV parsing, JD validation / analysis, document classification & JSONL Q/A chunking, async job store; covered with **pytest**.
- Unit tests for core services (xUnit, Moq).

[Backend](https://github.com/hienn12454/IQGS-SEP490-Backend) · [RAG / LLM Service](https://github.com/namnm309/IQGS-SEP490-RAG-LLM-SERVICE) · [RAG prototype (solo, ChromaDB + Ollama + Docker)](https://github.com/namnm309/RAG_IQGS)

---

### EV Charging Station Management
*Course project (SWP / PRN) · team of 4 · Oct – Nov 2025 · my commits: 36 / 63*

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core%208-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Razor Pages](https://img.shields.io/badge/Razor%20Pages-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![VNPay](https://img.shields.io/badge/VNPay-005BAA?style=flat-square)
![Google](https://img.shields.io/badge/Google%20OAuth-4285F4?style=flat-square&logo=google&logoColor=white)

Platform for EV drivers, station staff and admins.
- **Driver:** find stations on a map, reserve a charging spot by time slot, start a charging session, watch charging progress live (battery %, kW, kWh delivered, time remaining), pay with VNPay / MoMo, manage vehicles and subscription packages.
- **Staff:** monitor sessions and reservations at their station, update spot status.
- **Admin:** manage stations, spots, amenities, maintenance and error reports, users and roles; dashboard & revenue reports.

Architecture: 3 layers (Presentation · Business · DataAccess), Razor Pages UI + REST API controllers, EF Core + PostgreSQL.

**What I did**
- Created the solution structure, **authentication** (JWT, BCrypt) and **Google sign-in / register**.
- **Station map:** API that searches real charging stations via **SerpApi (Google Maps)** and a service that **merges external places with stations in our DB** (ratings, coordinates, live availability).
- Built the business services and APIs for **reservations, charging sessions & progress tracking, payments, subscriptions, vehicles, amenities, notifications and reporting**.
- **Real-time with SignalR:** notifier that pushes reservation / session / spot-availability / station-status updates to groups per user, station and session; user hub with an admin group for live dashboard updates.
- **VNPay payment** flow (create payment, return handling, status update).
- **Admin user management** (change role / status) and dashboard statistics service; refactored controllers to keep logic in the business layer.
- Integrated teammates' branches (station & spot management, staff dashboard, booking popup, MoMo) and fixed UI / payment issues before the final demo.

[Repository](https://github.com/namnm309/EV_Station_Management)

---

### Finmate — Personal Finance Platform
*Team of 2 · Jan – Apr 2026 · my commits: BE 51 / 92 · Web 27 / 45 · Mobile 32 / 46*

![.NET](https://img.shields.io/badge/.NET%208-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%20(Supabase)-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Clerk](https://img.shields.io/badge/Clerk-6C47FF?style=flat-square&logo=clerk&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![React Native](https://img.shields.io/badge/React%20Native-20232A?style=flat-square&logo=react&logoColor=61DAFB)

Track income / expenses across money sources, categories, savings books and goals; reports & charts; community feed with follows; Premium plans paid through SePay.

**What I did**
- **Backend:** initialized the 3-layer API; **Clerk** authentication (JWT + webhook user sync); CRUD for transactions, categories, account types, money sources; report endpoints; **SignalR** hub for live transaction history; community posts & user follows; savings book feature.
- **Payments:** **SePay** gateway + IPN webhook with signature verification, premium orders and admin filters by plan.
- **DevOps:** GitHub Actions build + deploy to **Azure App Service**, PostgreSQL on Supabase.
- **Web (Next.js):** landing page (hero, pricing, download links), admin dashboard and premium-orders page, SePay return / thank-you flow.
- **Mobile (Expo):** auth screens with Clerk, transactions, money sources, categories, savings, light / dark mode, SignalR updates; **local-first SQLite storage with a sync engine** (fixed initial-sync race condition and cross-account data leak); EAS build pipeline for APK.

[Backend](https://github.com/namnm309/Finmate-BE) ([Swagger](https://finmatecontroller20260116165929-dvckfkfvgqendpbk.eastasia-01.azurewebsites.net/swagger/index.html)) · [Web](https://github.com/namnm309/FinmateWeb) ([Live](https://finmate-web-five.vercel.app)) · [Mobile](https://github.com/namnm309/Finmate-Mobile)

---

### Cinema Ticket Booking
*FPT Software internship (OJT) · team of 7 · Jun – Aug 2025 · my commits: ~148 / 283*

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core%20MVC-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![VNPay](https://img.shields.io/badge/VNPay-005BAA?style=flat-square)

Cinema platform: movies, showtimes, cinema rooms, seat selection, vouchers / promotions, concessions, member points and payments, with admin / staff / member dashboards.

**What I did**
- Set up the solution and owned the main integration branch — merged and resolved conflicts from 5+ teammates' branches.
- **Movie management** CRUD (multiple actors & directors), homepage with banner, filter and recommendations.
- **Showtime scheduling** with calendar UI (only future showtimes, correct time display).
- **Ticket booking flow:** select movie → showtime → seat map → confirm booking for members (API + UI).
- **User / staff / member management** and admin dashboard.
- After a successful **VNPay** payment, automatically add loyalty points to the member.
- Generic repository, AutoMapper profiles, data seeding, 401 / role-based redirects.

[Repository](https://github.com/namnm309/OJT_SUMMER25_MOVIEWEBSITE)

---

### TechStore — E-commerce Backend & Mobile App
*Course project (PRM392) · team of 3 · Jan – Mar 2026 · my commits: BE 16 / 46 · Mobile 14 / 46*

![ASP.NET Core](https://img.shields.io/badge/ASP.NET%20Core-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![VNPay](https://img.shields.io/badge/VNPay-005BAA?style=flat-square)
![GHN](https://img.shields.io/badge/GHN-F26522?style=flat-square)
![React Native](https://img.shields.io/badge/React%20Native-20232A?style=flat-square&logo=react&logoColor=61DAFB)

Tech store: products & variants, cart, orders, vouchers, membership, wishlist, reviews, support chat.

**What I did**
- Initialized the backend; **Clerk** JWT validation (JWKS) and webhook verification.
- **VNPay** payment and **GHN** shipping integration — order process, GHN status mapping and webhook.
- GitHub Actions build + deploy to **Azure App Service**.
- Mobile: cart, checkout, VNPay payment & result screens, order tracking, movable chat popup, EAS APK build.

[Backend](https://github.com/namnm309/PRM392-Mobile-BE) ([Swagger](https://techstorebe-fzaza5cvgbhah6fg.eastasia-01.azurewebsites.net/swagger/index.html)) · [Mobile](https://github.com/namnm309/PRM392-Mobile)

---

## Other projects

| Project | What it does | My part | Stack |
| --- | --- | --- | --- |
| [FPTU Lab Events](https://github.com/namnm309/FPTU_Lab_Events) | Lab, room, equipment & event booking for FPT students and lecturers | Project setup, lab-member & booking management, roles; register only with `@fpt.edu.vn` + student-ID check and auto role detection; OTP / forgot password by email; **Redis caching** for APIs; GitHub Actions CI (23 / 48 commits) | ASP.NET Core, Clean Architecture, Redis |
| [Child Vaccination Scheduling](https://github.com/namnm309/SWP391O-Online-System-for-Child-Vaccination-Schedule-Management) | Vaccination booking for parents, staff & admin | Main backend developer: database design, JWT auth with **Spring Security** roles / permissions, vaccines, orders & order details, posts / reactions / feedback, Cloudinary, email notifications, Swagger, Maven CI (124 / 193 commits) | Spring Boot, PostgreSQL, Next.js |
| [Saga Pattern Demo](https://github.com/namnm309/Saga_Pattern_Orchestration_Demo) | Orchestrated multi-step workflow with compensation on failure | Solo | .NET 8, Minimal API, Next.js |
| [Microservice Web](https://github.com/namnm309/Microservice-Web) | API gateway + user / movie / booking services | Solo, learning project | ASP.NET Core, PostgreSQL |
| [Ninja Street 3D – web](https://github.com/namnm309/NinjaStreet3D) | Companion site: login, score submission, leaderboard | Solo | Next.js, TypeScript |

<details>
<summary>Earlier coursework (Java)</summary>

Hotel / Tour / Event management apps, MVC architecture with JSP/Servlet, Spring Boot practice and JUnit test cases.

</details>

---

## Currently

- Deepening backend fundamentals: database design & transactions, API reliability, testing.
- Looking for a **Fresher .NET Backend** position.

<div align="center">

**Backend first — comfortable collaborating across the stack.**

</div>
