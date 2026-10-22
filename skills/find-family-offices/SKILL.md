---
name: find-family-offices
description: Use when the user wants to find, search, filter, count or shortlist family offices (single family offices, multi family offices, family owned holding companies, family led investment firms) by country, region, US state, city, office type, investment domain, size, wealth origin or whether they accept deal submissions, or asks questions about the family office database as a whole. Uses the Active Family Offices connector.
---

# Find family offices

This skill turns a request like "single family offices in Texas that invest in real estate" into a precise search on the Active Family Offices database, and returns a short, ranked shortlist.

## Tools (Active Family Offices connector)

- `list_filter_values`: the exact allowed values for each filter (countries, regions, US states, office types, investment domains, wealth origins, team sizes).
- `search_family_offices`: filtered search. Returns teasers: the top 15 matches per search, no paging.
- `get_database_stats`: sizes and breakdowns of the whole database, and the data date.
- `my_trial_status`: the account, profiles opened, profiles remaining and calls left.
- `get_family_office`: opens one full profile. This uses one of the account's free profile opens, so it belongs to the outreach-prep skill and is only called when the user asks for a specific firm.

## Steps

1. Restate the target in one line: location, office type, investment domain and any other criteria. If the request is too broad to fit in 15 results (for example "family offices in the USA"), ask one question to narrow it, or suggest the narrowest useful filters.
2. If any filter value is uncertain (a domain name, a region label, a team size band), call `list_filter_values` first and use the exact value it returns. Never guess filter values.
3. Call `search_family_offices` with the most precise filters available. Prefer structured filters over the free text `query`; use `query` only for terms no filter covers.
4. Present the results as a short bullet list: firm name, city, office type, investment domains, and the one-line summary. State the total number of matches and that the list shows the top 15.
5. If there are more matches than shown, suggest one or two extra filters that would split the set (for example a city, a team size, or "accepts deal submissions"), rather than running many broad searches. Each account has a daily allowance of search rows, so every search should be precise.
6. For questions about the database as a whole ("how many family offices in Florida invest in healthcare", "which European countries have the most"), call `get_database_stats` instead of searching.
7. End by asking which firms the user wants to open in full, and mention how many profile opens remain (call `my_trial_status` if unknown).

## Rules

- Every fact comes from a tool result. Never invent firm names, people, emails, AUM figures or websites. Blank means unknown.
- Do not open profiles the user did not ask for.
- Do not use em dashes in answers.
