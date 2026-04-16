# Instagram Weekly Auto-Post Workflow (n8n)

## Overview

This workflow automates weekly Instagram posting using data from Google Sheets, AI-generated captions (Google Gemini), Cloudinary images, and Instagram Graph API.

## Flow

* **Schedule Trigger**: Runs every 7 days at 09:00
* **Google Sheets**: Fetches one row (File Name, Outline, Status)
* **AI Agent (Gemini)**: Generates Instagram caption from Outline
* **Instagram Graph API (Create Media)**: Uploads image + caption
* **Wait**: Ensures media processing is complete
* **Instagram Graph API (Publish Media)**: Publishes post
* **Google Sheets**: Updates status to `Posted`

## Data Source

* Google Sheets: *Instagram Weekly Upload*

  * File Name: Cloudinary image filename
  * Outline: Content idea
  * Status: Pending / Posted

## Requirements

* n8n
* Google Sheets API
* Google Gemini API
* Facebook Graph API (Instagram Business)
* Cloudinary
* Instagram Business/Creator account

