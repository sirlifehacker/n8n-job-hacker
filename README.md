# n8n-job-hacker

## The all-in-one automation to scrape jobs, customize your resume, and find hiring managers.

The Job Hacker is a full end-to-end automation workflow that helps you apply to hundreds of jobs in minutes by combining:

This template handles everything — scraping fresh job listings → customizing your resume → extracting hiring manager data → generating personalized outreach emails → storing everything in Notion → uploading your resume to Google Drive.

This workflow is the same system demonstrated in my YouTube video:
https://www.youtube.com/watch?v=00OMIR7tCD4

## ⚠️ Before You Use This Template

You must update these sections or the workflow will not work correctly.

**1. Replace the Sample Resume Template With Your Own**

The workflow includes a sample DOCX file based on a fictional Silicon Valley engineer.
This is only meant to illustrate how the DocX templating system works.

![Resume Template Preview](https://drive.google.com/uc?export=download&id=1AJFg-Lu_9Jd1W8pvzNwGZZcpe-qs2sMY)


You must:

Change the sample name "Justin Johnson" with your own.

Change all the job titles, skills, and education to your own. 

Save as a **docx file**

Upload your resume to Google Drive

If you skip this step, your resume output will be wrong.

**2. Update the AI Resume Agent With Your Own Experience**

The resume-customization AI agent currently uses a system message containing:

Sample summary

Sample bullet points

Sample skills

Sample tools

Sample work history

You must replace this JSON with:

Your real experience

Your actual skills & stack

Bullet points from your resume

Any additional context the agent should use

The agent rewrites your resume dynamically for each job — so your input JSON must reflect you, not the sample person.

**3. Add Your Own API Keys**

The template includes placeholder values for:

[Apify Linkedin Jobs Scraper](https://apify.com/cheap_scraper/linkedin-job-scraper?fpr=92rji7)

[Apify Leads Finder Scraper](https://apify.com/code_crafter/leads-finder?fpr=92rji7)

Perplexity

Google Drive

Notion

Gmail (optional)

Replace all API references before running the workflow.

## 🚀 How It Works (Step-by-Step)

1. User submits a LinkedIn job search URL

A form or manual trigger starts the workflow.

2. Apify scrapes all jobs from the search

Collects job title, salary, description, poster info, company name, etc.

3. AI customizes your resume for each job

The Resume Customizer Agent uses:

Job title

Job description

Your resume context

It outputs JSON formatted for DocX templating.

4. Resume is rendered into a DOCX file

The microservice merges:

Your DOCX template

The AI-generated content

Then re-uploads the file to Google Drive.

5. Hiring manager research runs

Using Perplexity + Apify Leads Finder, the workflow identifies:

Company domain

Validated emails

Seniority levels

Job function types

Decision-makers at the company

6. AI generates personalized outreach emails

Each email:

Is <700 characters

Is conversational

Mentions your resume link

Asks who to contact about interview prep

7. Everything logs to Notion

Every job becomes its own structured Notion record.

8. (Optional) Emails can auto-send

Using n8n’s Gmail or SMTP node.

## 🧠 Want More Automations Like This?

Join [my Skool community](https://www.skool.com/the-ai-entrepreneur-circle-5658/about) where I release:

New n8n workflows weekly

AI agent templates

Scraping systems

End-to-end business automations

3x Weekly Live Office Hours for Q&A & breakdowns

This is where the best automations get published first.
