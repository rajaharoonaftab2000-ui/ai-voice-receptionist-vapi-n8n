# AI Voice Receptionist — Vapi, n8n & MCP

An AI voice receptionist that handles appointment conversations, checks availability, and records bookings using Vapi, n8n, Google Calendar, and Google Sheets.

## Overview

This project demonstrates how a voice assistant can manage routine appointment requests through a natural conversation.

The receptionist collects the caller’s details, understands the booking request, and uses connected tools to check availability. When an appropriate slot is available and the caller confirms, the system creates a calendar appointment and saves the booking information in Google Sheets.

Vapi manages the voice conversation, while n8n provides the automation and integrations behind the assistant. The MCP server connects the assistant to the available workflow tools.

## What It Does

- Handles appointment-related voice conversations.
- Collects the caller’s name and contact information.
- Identifies the requested service or appointment purpose.
- Checks availability through connected calendar tools.
- Suggests another time when the requested slot is unavailable.
- Creates appointments in Google Calendar.
- Records booking details in Google Sheets.
- Reads back the appointment details to the caller.
- Uses configurable business information and conversation instructions.

## Workflow

**Caller → Vapi Voice Assistant → MCP Tools → n8n Workflows → Google Calendar / Google Sheets → Spoken Confirmation**

The voice assistant manages the conversation. Connected tools perform the calendar checks and booking actions.

## How It Works

### 1. Receive the Call

The receptionist greets the caller and asks how it can help.

### 2. Understand the Request

The assistant identifies the appointment purpose and collects the information required by the business.

### 3. Collect Booking Details

The caller provides their name, contact number, preferred date, and appointment time. Additional questions depend on the configured booking process.

### 4. Check Availability

The assistant calls the connected availability tool to check the requested calendar slot.

If the slot is unavailable, the assistant asks the caller to choose another time.

### 5. Create the Appointment

After the required information and caller confirmation are collected, the workflow creates the appointment in Google Calendar.

### 6. Save the Booking Record

The booking information is saved in Google Sheets for administrative tracking.

### 7. Confirm the Result

The assistant summarizes the confirmed appointment details and asks whether the caller needs further assistance.

## Technologies Used

| Technology | Purpose |
| --- | --- |
| Vapi | Voice conversations and assistant tool calls |
| n8n | Workflow automation and application integrations |
| MCP | Access to the connected workflow tools |
| Google Calendar | Availability checks and appointment creation |
| Google Sheets | Booking records and contact information |

## Setup Requirements

- A running n8n instance.
- A configured Vapi assistant.
- An accessible MCP server endpoint with the required tools.
- Google Calendar and Google Sheets connections.
- A calendar configured for the business.
- A spreadsheet prepared for booking records.
- Business information, appointment rules, and timezone settings.
- A supported calling or testing setup in Vapi.

## Configuration

1. Connect your own Google Calendar and Google Sheets credentials in n8n.
2. Configure the calendar and spreadsheet used by the booking workflows.
3. Set the business timezone, appointment duration, and availability rules.
4. Connect the required n8n tools through the MCP server.
5. Configure the Vapi assistant’s greeting, instructions, and tool descriptions.
6. Add the business information and appointment questions.
7. Test the conversation and verify the calendar and spreadsheet results.

The connected tools, calendar fields, and spreadsheet columns must match the workflow configuration.

## Example Test Conversation

**Caller:**  
“Hi, I would like to book an appointment.”

**Assistant:**  
“Certainly. What is the appointment for?”

**Caller:**  
“A routine consultation.”

The assistant then collects the caller’s details and preferred time, checks availability, and completes the booking when the slot is available and the caller confirms.

The exact wording depends on the configured assistant instructions.

## Suggested Test Cases

- Book an available appointment.
- Request an unavailable time.
- Provide incomplete contact details.
- Give a weekday without a specific date.
- Confirm that the assistant uses the correct timezone.
- Verify that the confirmed appointment appears in Google Calendar.
- Verify that the booking record appears in Google Sheets.

## Customization

The workflow can be adapted for clinics, salons, consultants, and other appointment-based businesses.

Customization can include:

- Business name and greeting.
- Voice and supported language.
- Services and appointment durations.
- Staff or provider calendars.
- Working hours and booking rules.
- Required caller information.
- Spreadsheet fields and additional integrations.

These changes require configuration and testing for the intended business.

## Important Notes

- Availability depends on the connected calendar and configured booking rules.
- The assistant should confirm a booking only after the booking tool reports success.
- n8n and the MCP endpoint must remain accessible while the assistant is in use.
- Hosting, calling, and AI service usage may incur separate charges.
- Public workflow exports should exclude credentials, private endpoints, and customer data.

## Project Status

Portfolio demonstration of a voice appointment receptionist connected to calendar and booking-record workflows.

## Author

**Haroon AI Automation**

Practical AI assistants and n8n workflows for business automation.

## Demo Video

[Watch the AI Voice Receptionist Demo](./Hospital-Voice-Receptionist-Clean-Call-Captions.mp4)
