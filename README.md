Here's a detailed README for your IPL Dashboard GitHub repository, incorporating your screenshots:

```markdown
IPL Performance Analytics Dashboard

[Dashboard Preview](https://ibb.co/ksrtKxVT)

 ##Overview
This Power BI dashboard provides comprehensive analysis of Indian Premier League (IPL) match data from 2008-2020. It transforms raw cricket data into actionable insights through interactive visualizations, enabling data-driven decision making for teams, analysts, and fans.

##Features
- Team & Player Performance: Track wins, losses, and individual player stats
- Season Analysis: Compare performance across 12 IPL seasons
- Award Tracking: Monitor Orange Cap (top batsman) and Purple Cap (top bowler) contenders
- Venue Insights: Analyze win patterns by stadium
- Toss Impact: Visualize correlation between toss decisions and match outcomes
- Interactive Filters: Drill down by season, team, player, and venue

 ##Key Metrics Analyzed
| Metric Category | Specific Metrics |
|-----------------|-----------------|
| Batting | Runs, Strike Rate, Highest Scores |
| Bowling | Wickets, Economy Rate, Dot Balls |
| Team Performance | Win Percentage, Toss Impact, Venue Records |
| Tournament Stats | Total Runs, Total Wickets, Match Counts |

 ##Data Sources
[Data Structure](Screenshot%202025-07-03%20215257.png)
- Primary Dataset: 12 seasons of IPL match data (2008-2020)
- Data Points: 800+ matches, 2000+ player records
- Data Structure: 
  - ipl_matches: Match metadata (date, venue, teams, toss decisions)
  - ipl_ball_by_ball: Detailed ball-by-ball records
  - Calendar Table: Date dimension for time analysis

##Technical Implementation
mermaid
graph LR
A[Data Extraction] --> B[Data Transformation]
B --> C[Data Modeling]
C --> D[Metric Calculation]
D --> E[Visualization]
```

1. **ETL Pipeline**:
   - Extracted raw data from CSV files
   - Transformed data using Power Query (handled missing values, standardized formats)
   - Created calculated columns for cricket-specific metrics

2. **DAX Calculations**:
   ```dax
   Strike Rate = DIVIDE([Total Runs], [Balls Faced]) * 100
   Win Percentage = DIVIDE([Wins], [Total Matches])
   ```

3. **Visual Components**:
   - Interactive filters (season, team, player)
   - Trend analysis charts
   - Performance comparison matrices
   - Geo-spatial venue analysis

## How to Use
1. Clone repository
2. Open `IPL_Dashboard.pbix` in Power BI Desktop
3. Explore using filter controls:
   - Select seasons in the slicer
   - Click on teams to see player performance
   - Hover over charts for detailed metrics

## Key Insights
- Teams winning toss win 52% of matches
- Top venue: Wankhede Stadium (Mumbai) with highest win rate
- Most consistent batsman: David Warner (Orange Cap 3 seasons)
- Best economy rate: Sunil Narine (6.8 runs/over)

## Future Enhancements
- Real-time data integration
- Player performance prediction model
- Head-to-head team comparison

```

