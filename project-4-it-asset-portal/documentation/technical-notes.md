# IT Asset Request Portal — Technical Notes

## Data Import Flow
1. CSV file loaded into staging table
2. Transform Map created
3. Field maps matched
4. Coalesce configured on Email key to prevent duplicates
5. Transform executed against `sys_user` target table
