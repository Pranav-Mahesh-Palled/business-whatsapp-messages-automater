# Business WhatsApp Messages Automator

## Overview

This workflow acts like a smart WhatsApp-style assistant for a restaurant business. It can answer FAQs, take orders, check stock, look up order status, and guide customers through the conversation using AI.

It is designed to simulate a real business support system on top of n8n.

---

## Problem Statement

Small businesses often receive many repeated customer messages such as:
- menu questions
- order requests
- stock availability
- opening hours
- order tracking

Handling all of these manually can be slow and repetitive.

---

## Solution

The workflow uses an AI agent to respond like a restaurant assistant. It can:
- greet new users
- ask for order details step by step
- check inventory before confirming an order
- answer FAQs
- look up order or stock information
- write accepted orders into Google Sheets

---

## Workflow Architecture

Chat Trigger  
↓  
AI Agent  
↓  
Gemini Model + Memory  
↓  
Google Sheets Inventory Lookup  
↓  
Google Sheets FAQ Lookup  
↓  
Orders Sheet Update  
↓  
WhatsApp-style Reply

---

## Technologies Used

- n8n
- Gemini
- Chat Trigger
- Memory Buffer
- Google Sheets
- AI Agent

---

## How It Works

### Step 1: User Sends a Message
The workflow starts when a message is received.

### Step 2: AI Understands the Intent
The AI agent decides whether the user wants:
- to place an order
- FAQ support
- order checking
- stock checking
- cancellation help

### Step 3: Inventory and FAQ Lookup
The agent checks Google Sheets tools for:
- available stock
- FAQ answers
- order history

### Step 4: Order Handling
If an item is available, the workflow confirms the order and writes it into the Orders sheet.

If the item is unavailable, it replies with available options.

### Step 5: Final Reply
The assistant responds in short WhatsApp-style text.

---

## Input Requirements

The workflow expects Google Sheets with:
- Inventory sheet
- FAQ sheet
- Orders sheet

---

## Output

The workflow produces:
- customer reply
- order confirmation
- stock response
- FAQ response
- stored order record

---

## Setup Instructions

1. Import the JSON into n8n.
2. Connect Gemini credentials.
3. Connect Google Sheets credentials.
4. Prepare Inventory, FAQ, and Orders sheets.
5. Update sheet IDs and columns.
6. Test with a few sample chat messages.

---

## Future Improvements

- Add payment confirmation
- Add delivery tracking
- Add multilingual replies
- Add order cancellation automation
- Add voice message support

---

## Author

Pranav Mahesh Palled
