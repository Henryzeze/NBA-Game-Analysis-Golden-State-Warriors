# NBA-Game-Analysis-Golden-State-Warriors

![](NBA-game-analysis.jpg)

### Project Overview
This lab involves leveraging the NBA API to comprehensively analyze and evaluate the performance of the Golden State Warriors. The primary aim is to ascertain the winning or losing margin of the Golden State Warriors in each game. Additionally, the project includes exporting the obtained data as a csv file for further analysis and visualization in Microsoft Power BI. The key performance metrics to be explored include Winning Percentage, Scoring Efficiency, Defensive Performance, Ball Handling, Rebounding, Assists, Steals, and Blocks.

## Methodology
1. **ASK**: I need to understand the data before conducting meaningful analysis. So I had to do an extensive study on the NBA game and ask/research every question to fully understand what key metrics was needed for my analysis. 
2. **PREPARE**: After that, I connected to the NBA API using a Python script to get the necessary data.
3. **PROCESS**: Data Transformation was performed in Microsoft Excel. On initial analysis of the data, there were missing values in the following columns:
- FG_PCT: 1 missing value
- FG3A: 1 missing value
- FG3_PCT: 24 missing values
- FT_PCT: 1 missing value
- OREB: 2 missing values
- DREB: 2 missing values
- REB: 1 missing value
- PLUS_MINUS: 1122 missing values

On further analysis of the data, Using conditional formatting > Highlight cells by rules > Duplicate values, duplicate entries on GAME_ID 1520800001 were found and removed. This also handled the missing data in columns FG_PCT, FT_PCT, and REB.

FG3A: 1 missing value
the FG3A (three-point field goals attempted) column could be an important factor, especially for Scoring Efficiency. I believe there is no way the team did not attempt three-point shots, So I decided to fill the missing values with the median of the FG3A column which is 18. The median is often a better choice than the mean for filling in missing values, as it is less sensitive to outliers and skewed data.

ORED and DREB: 2 missing values:
the OREB (Offensive Rebounds) and DREB (Defensive Rebounds) columns are crucial, especially for Rebounding and Defensive Performance. It is highly unlikely that a team does not make any rebounds in a basketball game. So I filled the missing values with the median of the OREB and DREB columns which is 12 and 31 respectively. The median is often a better choice than the mean for filling in missing values, as it is less sensitive to outliers and skewed data.

Finally, I decided to leave the missing values in the FG3_PCT and PLUS_MINUS columns as they will be dropped during visualization in Microsoft Power BI.

4. **Analyze**: The tool used for visualization was Microsoft Power BI and the following KPIs were visualized and Analyzed.

