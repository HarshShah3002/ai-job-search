# Search Queries for Job Scraper

## Search Sites

Primary (US job market, country-agnostic tooling):
- **linkedin-search skill** (`.agents/skills/linkedin-search/`) - built on LinkedIn's public jobs-guest endpoints, run with `-l "United States"` or a specific city
- **linkedin.com/jobs** - direct LinkedIn search as a fallback
- Company career pages (Greenhouse, Lever, Ashby, Workday boards) via direct `site:` Google searches for target companies

Note: the `jobbank-search`, `jobdanmark-search`, `jobindex-search`, and `jobnet-search` CLI tools in this repo are Denmark-specific and not relevant to Harsh's US search. Skip installing/using them; rely on `linkedin-search` and direct site searches instead.

Secondary (H1B-specific verification, not scraping):
- **myvisajobs.com** - historical sponsorship data by employer (verify against live postings, don't trust timestamps blindly)
- **USCIS H1B Employer Data Hub** - official sponsorship filing history by employer

## Query Categories

Queries are grouped by priority. Location is "United States" broadly since Harsh is open to relocating anywhere; sponsorship likelihood matters more than geography.

### Priority 1: Data Analyst / BI Analyst

These match his strongest and most desired career direction.

```
site:linkedin.com/jobs "Data Analyst" United States
site:linkedin.com/jobs "Business Intelligence Analyst" United States
site:linkedin.com/jobs "BI Analyst" SQL Tableau United States
linkedin-search -l "United States" -q "Data Analyst"
```

### Priority 2: Data Engineer / Analytics Engineer

These match his growing domain expertise in pipelines and ETL.

```
site:linkedin.com/jobs "Data Engineer" entry level OR junior United States
site:linkedin.com/jobs "Analytics Engineer" SQL Python United States
linkedin-search -l "United States" -q "Data Engineer"
```

### Priority 3: Technical Product Manager / Product Analyst

Adjacent roles leveraging his product management internship and pivot narrative.

```
site:linkedin.com/jobs "Technical Product Manager" data United States
site:linkedin.com/jobs "Product Analyst" SQL United States
linkedin-search -l "United States" -q "Product Analyst"
```

### Priority 4: Broader Analytics / Consulting

Wider net for general technical/analytics roles.

```
site:linkedin.com/jobs "Data Analyst" OR "Analytics" new grad United States
site:linkedin.com/jobs "technical consultant" analytics United States
linkedin-search -l "United States" -q "Business Analyst"
```

## Target Companies to Monitor

- Tech / SaaS: Tesla, OpenAI, Brex, Clay, Upgrade, Peregrine Technologies, Amigo AI, Goose, Omni
- Retail / e-commerce / consumer: Etsy, Ollie, T-Mobile, Sony Interactive Entertainment

When scraping, add explicit queries for these company career pages, e.g. `site:boards.greenhouse.io "Tesla" data analyst`.

## Location Filter

Harsh is open to relocating anywhere in the US, so there is no strict commute filter. Instead, weight postings by realistic H1B sponsorship likelihood:
- **Ideal:** Large tech hubs with strong sponsorship track records (SF Bay Area, Seattle, NYC, Austin) and fully remote roles at companies with a sponsorship history
- **Acceptable:** Other major metros (Chicago, Denver, Boston, Dallas) at mid-size or larger companies
- **Borderline:** Smaller companies or markets with no clear sponsorship history; flag for manual verification before applying
- **Too far:** Not location-based here; instead, treat "explicitly states no sponsorship" as the equivalent of "too far" (skip)

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus. For example:
- "/scrape data engineer" -> Priority 2 queries + custom data-engineer-specific queries
- "/scrape [company name]" -> direct career-page search for that company plus a sponsorship-history check
