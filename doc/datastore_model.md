

<pre>
User
  - email -> String

Page
  - url
  - latestVersion -> Reference(PageVersion)
  - firstSeen -> DateTime
  
  + PageVersion
    - Page -> Reference(Page)
    - html -> Blog? Unicode something?
    - timeRetrieved -> DateTime

  + PageSummary

UserSaved
  - User -> Reference

  + UserSavedPage
    - User -> Reference
    - Page -> Reference
    - tags -> StringList
    - lastUpdated -> DateTime (updated on first creation, tag change, new quote)
    
    + UserSavedPageQuote
      - text -> Text
      - order -> Integer
      - datetime -> DateTime

      + UserSavedPageXpaths
        - xpathStart
        - xpathEnd
        - xpathsOrdered -> StringList


PageSummary
  - Page -> Reference
  - 

  + PageSummaryHighlighted

</pre>



**All highlighted text by page (build summaries, overlaps)**

<code>
SELECT * FROM 
</code>



**All highlighted by user, by page (chrome view page)**
  
  SELECT 

All popular highlighted by page (chrome view page)

All pages by user ordered by recency (user’s recent page)
All pages ordered by popularity (popular page)

Search by keyword (chrome google SERP)
Search by tag (frontend)
Popular tags
