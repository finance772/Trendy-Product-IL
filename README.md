# Trendy-Product-IL
A practical tool that lets you quickly see, at a glance, which products are worth importing and selling in an online store in Israel, especially in the Korean skincare and beauty market
Ctrl+K
Ctrl+J



Skills and Connectors
Skills
Connectors
Search...
Personal
trending-products-israel
Use this skill to find the most trending products in the Israeli market and rank them in a table with scores for online store sales management potential. Triggers include מוצרים טרנדים בישראל, trending products Israel, best sellers Israel 2026, analyze e-commerce potential for products in Israel, rank products for online sales, products for dropshipping Israel.

Word Documents
Create, read, and edit Word documents (.docx)
PDFs
Create, merge, split, and extract from PDFs
Presentations
Create, read, and edit PowerPoint presentations (.pptx)
Skill Creator
Build new custom skills through conversation
Spreadsheets
Create, read, and edit spreadsheet files (.xlsx, .csv)
Upgrade to SuperGrok

trending-products-israel

SKILL.md

references

israeli-ecommerce-sites.md
trending-products-israel
Created by
Michal
Last Updated
Today
Files
2
Size
9.60 KB
Description

Use this skill to find the most trending products in the Israeli market and rank them in a table with scores for online store sales management potential. Triggers include מוצרים טרנדים בישראל, trending products Israel, best sellers Israel 2026, analyze e-commerce potential for products in Israel, rank products for online sales, products for dropshipping Israel.

Trending Products Israel
Overview
This skill enables discovery of current trending and best-selling products in Israel, followed by structured evaluation and ranking for suitability in managing an online store (e-commerce sales, dropshipping, or local fulfillment). It produces a prioritized table with a custom 1-10 score focused on realistic online sales viability.

Instructions
When the user asks about trending products in the Israeli market, best sellers, or evaluating products for an online store (in Hebrew or English), activate this workflow. Consult references/israeli-ecommerce-sites.md for a curated list of key platforms, trend sources, supplier directories, and Israel-specific regulatory considerations to guide searches and operational scoring.

Note the current date context (June 2026 or later) and focus on timely trends for the Israeli consumer market (population ~9.5M, strong e-commerce growth in electronics, home, beauty, fashion, baby/kids, and seasonal items).

Use the web_search tool (and browse_page where needed) to gather fresh data with these queries (mix English and Hebrew):

"trending products Israel 2026" or "מוצרים טרנדים בישראל 2026"
"best selling products Israel e-commerce" or "המוצרים הנמכרים ביותר בישראל"
"Google Trends Israel top searches" or "טרנדים בגוגל ישראל"
Site-specific: "best sellers zap.co.il", "ksp.co.il מוצרים פופולריים", "ivory.co.il trending"
Additional: "dropshipping products Israel profitable", "ספקים סיטונאים ישראל [category]", competition indicators like "כמה חנויות מוכרות [product] ישראל"
From results, extract 8-15 promising product candidates across categories (electronics/accessories, home & kitchen, beauty & personal care, fashion & apparel, baby products, sports/outdoor, smart home). Prioritize items with rising interest, not just evergreen.

For each candidate product, collect key data points via additional targeted searches and browsing:

Approximate search interest / trend strength (high/medium/low or specific mentions).
Competition level in Israel (number of sellers on major platforms, saturation).
Typical retail price range in ILS on Israeli sites.
Estimated sourcing cost (local wholesalers via searches, or AliExpress/China dropship landed cost to Israel including shipping ~7-14 days).
Estimated net margin after platform fees (5-15%), ads (if PPC), returns, and shipping (target >25-30% for viability).
Operational factors: ease of product description/photos, standardization (good for online), shipping weight/size, return rate typical for category, any Israel-specific regulations (e.g. Ministry of Health for cosmetics/supplements, electrical standards for electronics, no food perishables).
Israel market fit: cultural/seasonal relevance (e.g. summer cooling, Jewish holidays, back-to-school Aug/Sep, high-tech gadgets popular).
Calculate the Online Sales Potential Score (1-10) for each product using this rubric (be consistent and transparent):

Demand/Trend Strength (0-3 points): Strong rising trend + high mentions = 3; Solid popular demand = 2; Niche or declining = 1 or 0.
Competition Level (0-2 points): Low competition / blue ocean = 2; Medium = 1; High saturation / many big sellers = 0.
Profit Margin & Economics (0-2 points): Strong estimated net margin >35% after all costs = 2; Acceptable 25-35% = 1; Low <25% or high ad dependency = 0.
Operational Ease for Online Store (0-2 points): Easy sourcing/fulfillment/returns + minimal regulations + standardized product = 2; Some challenges manageable = 1; High friction (licenses, high returns, complex logistics) = 0.
Israel-Specific Fit (0-1 point): Good alignment with local demand, seasons, or consumer behavior = 1; Generic/global only = 0.
Total the points for the final score out of 10. Round to whole number. Be conservative on optimistic estimates.
Compile all evaluated products into a single Markdown table sorted by the Online Sales Potential Score (descending). Use these exact Hebrew column headers for the response: | מוצר | קטגוריה | ציון טרנד (1-3) | רמת תחרות | שולי רווח משוערים | ציון פוטנציאל מכירות אונליין (1-10) | סיבות עיקריות | מקורות מידע |

Fill "סיבות עיקריות" with 1-2 sentence summary of why the score (key pros/cons). Include inline citations where data comes from web_search or browse_page results.

After the table, provide:

Top 5 recommendations with brief why they are strong for starting or expanding an online store in Israel.
Any notable risks or Israel-specific considerations (e.g. payment gateways popular locally like PayPlus, Cardcom; platforms like Shopify + Hebrew support, Wix, or local Israeli e-commerce solutions; VAT/customs for imports).
Suggestions for next actions: validate specific suppliers, check current regulations via official sites, test small ad campaigns, or focus on niches with local fulfillment options.
If data is sparse for some products, note it and suggest deeper research.
Always respond in Hebrew (full natural Hebrew) when the user's query is in Hebrew or mentions Israeli market. Translate product names naturally (keep English brand/model where common) and make the entire output professional and actionable for an Israeli online seller. Use the table formatting that renders well in chat.

If the query is very specific (e.g. only one category like "טרנדים באלקטרוניקה"), narrow the search and scoring accordingly but still use the full rubric for fairness.

This workflow ensures data-driven, repeatable analysis without relying on outdated knowledge. Re-run searches for the absolute latest trends on every activation.

Skills and Connectors - Grok https://trendydrodil.netlify.app/
