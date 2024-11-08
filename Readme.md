## Cryptocurrencies data parser

### Description
This project implements a parser that extracts data of different types of cryptocurrencies, such as ETH, SOL, BTC etc.

### Technical description
The parser reades structured data from a file using grammar rules and then outputs parsed result to a csv file.

- digit: Matches any single ASCII digit (0-9)
- year: Matches a four-digit year by concatenating four digit rules (e.g., 2024)
- month: Matches either a two-digit month (e.g., 01 for January) or a month represented by one or more alphabetical characters (e.g., Jan, November)
- day: Matches a two-digit day (e.g., 01, 23).
- date: Matches various date formats, e.g.,  08.11.2024, 11/08/2024, Nov 8, 2024
- blockchain_name: Matches specific blockchain names: SOL, BTC, or ETH. This ensures only these blockchain names are parsed as valid
- currency: Matches specific currency codes: USD, EUR, or UAH. This limits the parsed currency to these three options
- number: Matches a numeric value, potentially with thousands separators (e.g., 1,000,000) and optional decimal places (e.g., 123.45)
- entry: Matches a complete entry for a blockchain record, which includes: Name: field with a blockchain name, Date: field with a date,
- Open:, Close:, High:, Low:, and Volume: fields, each followed by a number and a currency

### Applying
This parser can be used in applications related to blockchain and financial data processing

- The parser can be used to extract structured data from text files or logs that record blockchain or cryptocurrency market data. This is useful for preparing datasets for further analysis or storage in databases

- The parser can be used to read historical blockchain data from files and convert it into a structured format, such as CSV. Analysts can then use this data to identify trends, patterns, or perform time-series analysis

- This parser can be utilized in applications that help manage cryptocurrency portfolios by parsing data that includes market metrics like open, close, high, and low prices, and volumes for specific dates