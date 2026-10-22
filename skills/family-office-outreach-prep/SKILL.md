---
name: family-office-outreach-prep
description: Use when the user wants to open a specific family office's full profile, find the right decision-maker to contact, check whether and how the firm accepts deal submissions, or prepare a first outreach message to a family office found in the Active Family Offices database.
---

# Family office outreach prep

This skill opens a family office profile from the Active Family Offices database, picks the right person to contact, and prepares a short first message based only on what the profile says.

## Tools (Active Family Offices connector)

- `my_trial_status`: profiles opened and profiles remaining on the account.
- `get_family_office`: opens one full profile by id (preferred) or name. Each new profile uses one of the account's profile opens; re-opening a profile already opened is free.
- `search_family_offices`: to find the firm's id first when the user gives only a partial name.

## Steps

1. Confirm which firm to open. If the user gave a name that could match several firms, run a narrow `search_family_offices` and ask which one.
2. If the account is close to its limit, call `my_trial_status` and tell the user how many profile opens remain before opening a new one.
3. Call `get_family_office`. Present: website, location, office type, family name, description, investment domains, AUM and team size when disclosed, year founded, and the deal submission channel.
4. Decision-makers: list each with position, and LinkedIn and verified work email where the profile includes them. Recommend the single most relevant contact for the user's purpose (for example the CIO or head of real estate for a real estate co-investment) and say why in one line.
5. Restricted countries: for firms in the EU, EEA, UK, Switzerland, Israel and Canada, decision-makers are listed by name and position only. Say so, and point the user to the firm-level contact details or the deal submission channel shown in the profile.
6. If the user asks for a message, draft a short first email (under 120 words) that references one or two specific facts from the profile (investment domains, location, recent focus in the description), states the user's ask in one sentence, and ends with a simple question. Do not invent shared connections, past deals or facts that the profile does not contain. Never send anything; the user sends it.

## Rules

- Base every fact on the tool result. Blank means unknown.
- Open only the profiles the user asks for.
- When the profile allowance is used up, say so and give the link the tool returns. Do not push it otherwise.
- Do not use em dashes in answers or drafts.
