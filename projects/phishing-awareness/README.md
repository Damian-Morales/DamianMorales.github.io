# Phishing Awareness Training Project

## Overview
This project is a **Phishing Awareness Training Simulator** built with **Flask**.  
It generates simulated phishing emails, provides awareness landing pages, and tracks user interactions (sent, clicked, reported) on an admin dashboard.

The goal of this project is to help raise security awareness and provide hands-on experience with phishing simulation workflows.

---

## Setup

1. **Create a virtual environment and install dependencies**
   ```bash
   python -m venv .venv
   .venv\Scripts\activate
   pip install -r requirements.txt
   ![Virtual Environment Setup](screenshots/Terminal%20.venv.png)
   
2. **Initialize the database**
   python manage.py init-db
   ![Database Initialized](screenshots/Database%20initialized.png)

4. **Configure environment file**
   Copy .env.example to .env and adjust campaign defaults.
   ![.env Configuration](screenshots/file%20.env%20opened.png)

## Running a Campaign
Run the campaign in preview-only mode (emails saved to /outbox folder).
   ![Outbox Emails](screenshots/outbox%20folder%20with%20HTML%20files.png)
  python manage.py send --csv recipients.csv --template emails/fake_invoice.html --campaign "October Drill"
  ![Campaign Processed](screenshots/Terminal%20Campaign%20processed%20in%20preview%20mode.png)
  
## Simulation Walkthrough
1.  **Open the phishing email (preview mode).**
   ![Training Email Opened](screenshots/opened%20training%20email.png)
3.  **Clicking View Invoice -> Phishing Awareness Debrief page.**
   ![Phishing Landing Page](screenshots/Landing%20Page.png)
4.  **Clicking Report Simulation -> Reported confirmation page**
   ![Reported Confirmation](screenshots/Reported%20Page.png)

## Admin Dashboard
The admin dashboard tracks campaign progress in real-time:
Emails **Sent**

Links **Clicked**

Reports **Submitted**
![Admin Dashboard](screenshots/Dashboard%20sent_clicked_reported%20updated.png)


## Reflections
Learned how phishing awareness simulations are structured.

Hands-on experience with Flask, database handling, and email templates.

Reinforced ethical use: this is for **training and awareness only**, never malicious purposes.
