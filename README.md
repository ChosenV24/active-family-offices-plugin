# Active Family Offices

Search a family office database from Claude, build shortlists, and open full profiles with decision-makers and verified work emails.

Every family office in the Active Family Offices database has a live website and was reviewed and verified by a team of humans. The database covers single family offices, multi family offices, family owned holding companies and family led investment firms worldwide.

## What the plugin includes

- **Active Family Offices connector** (remote MCP server at `https://mcp.activefamilyoffices.com/mcp`, OAuth sign-in). Five read-only tools:
  - `search_family_offices`: filter by country, region, US state, city, office type, investment domain, giant status, accepts deal submissions, verified email, wealth origin, team size, founding year and free text. Returns the top 15 matches per search.
  - `get_family_office`: open a full profile: website, company LinkedIn, location, description, investment domains, office type, family name, up to 3 decision-makers with position, LinkedIn and verified work email, company email and phone, year founded, deal submission channel, AUM, team size and wealth origin.
  - `get_database_stats`: sizes and breakdowns of the database and the data date.
  - `list_filter_values`: the exact allowed values for each filter.
  - `my_trial_status`: profiles opened, profiles remaining and calls left.
- **Skill: find-family-offices**: turns a plain request into precise filters and returns a ranked shortlist.
- **Skill: family-office-outreach-prep**: opens a profile, picks the right decision-maker, and drafts a short first message based only on the profile.

## Getting started

1. Install the plugin. The first time Claude calls a tool, you are asked to sign in.
2. Sign in with your work email and first name. A 6-digit code is emailed to you; enter it to finish.
3. Ask, for example:
   - "Find single family offices in Texas that invest in real estate."
   - "Which European countries have the most family offices investing in venture capital?"
   - "Open the profile of Crow Holdings and tell me who to contact about a real estate co-investment."

## Free allowance

Each account can open 10 full profiles. Re-opening a profile you already opened does not count again. Each search returns the top 15 matches, each account can view 60 search results a day, and there is a limit of 100 tool calls per day. The full database is available as an Excel file at [activefamilyoffices.com](https://activefamilyoffices.com).

## Data and privacy

- What the plugin sends: your search filters and the ids of the profiles you open go to the Active Family Offices MCP server (hosted on Cloudflare). Nothing else from your conversation or files is sent.
- What is stored: your email, first name, the profiles you opened and usage counts. Your email and first name are added to the Active Family Offices mailing list (Kit); you can unsubscribe at any time.
- Contacts restrictions: for firms in the EU, EEA, UK, Switzerland, Israel and Canada, decision-makers are listed by name and position only. No personal emails or LinkedIn profiles are shared for those countries.
- The plugin is read only. It never sends messages, books meetings or changes anything outside the database. It runs no local code, hooks or scripts.
- Privacy policy: https://mcp.activefamilyoffices.com/privacy
- Support and deletion requests: support@activefamilyoffices.com

## More

- How to connect in other AI apps: https://activefamilyoffices.com/pages/free-ai-connector
- Connector home: https://mcp.activefamilyoffices.com/

## License

MIT for the files in this repository. See [LICENSE](LICENSE).
