CertTrack INTE301 | Online Certification Monitoring System

An end-to-end web application built for INTE301 to monitor student certification progress, verify proof submissions, and provide real-time administrative oversight.

🚀 Live Demo & Deployment

Frontend Host: Vercel

Backend & Database: Supabase (PostgreSQL + Row Level Security)

Target Deadline: November 16

🛠️ Tech Stack

Frontend: HTML5, Tailwind CSS (via CDN), JavaScript (ES6+), Supabase JavaScript Client SDK v2.

Backend / Database: Supabase PostgreSQL Database.

Authentication: Supabase Auth (Email & Password with RLS Security Policies).

🗄️ Database Architecture (Supabase)

The system utilizes two primary tables with Row Level Security (RLS) fully enabled:

profiles Table

Links directly to Supabase Auth users (auth.users).

Stores student and admin metadata (full_name, student_number, role).

certifications Table

Tracks individual student certifications (cert_title, issuer, progress_percent, target_date, proof_url, verification_code, status).

Status states: in_progress, pending_approval, verified, rejected.

✨ Core Features

Student Portal:

Secure registration and authentication.

Track ongoing or completed professional certifications (e.g., Cisco NetAcad, Coursera, AWS, CompTIA).

Dynamic completion progress bar (0% to 100%).

Direct proof submission link (Google Drive, Credly, certificate PDF link).

Professor / Admin Monitor Dashboard:

Centralized overview of all student certification milestones across the class.

Quick review of submitted proof links.

One-click approval (verified) or rejection workflows.

⚙️ Setup & Installation

Clone the Repository:

git clone https://github.com/your-username/inte301-cert-tracker.git


Configure Supabase:

Run the provided schema and RLS policy script in your Supabase SQL Editor.

Disable email confirmations under Authentication → Providers → Email for instant sign-ups.

Run Locally:

Open index.html in any modern web browser or deploy directly to Vercel.
