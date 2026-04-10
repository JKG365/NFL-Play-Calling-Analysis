# NFL-Play-Calling-Analysis

NFL teams make hundreds of play-calling decisions every game. But are they actually calling the right plays in the right situations? This project uses 3 seasons of NFL play-by-play data (2022-2024) to measure which play types, run or pass, generate the most valuable plays by down and distance using Expected Points Added (EPA) as the primary metric.

# Key Findings

**3rd and Long:** Running the ball outperforms passing by 0.309 EPA per play - yet teams pass here over 85% of the time.

**3rd and Medium:** Running generates 0.239 EPA, the highest of any situation in the dataset — teams rarely run here
- **1st and Short:** Passing loses 0.142 EPA on average while running gains 0.049 — teams consistently choose the wrong play
- **1st and Long:** The one situation where conventional wisdom is correct — passing outperforms running by 0.139 EPA

## The Big Picture
On 3rd down specifically, running the ball outperforms passing in every single distance bucket. Teams are systematically choosing a lower-value play type on the most important down in football.

## Tools Used
- Python (pandas, matplotlib, seaborn)
- NFL play-by-play data (2022–2024)
- JupyterLab

## Files
- `Nfl_Play_Calling.ipynb` — full analysis notebook
- `epa_heatmap.png` — heatmap visualization
- `nfl_playcalling_findings.csv` — summary findings table

## Methodology
Filtered 148,591 raw plays down to 103,262 meaningful offensive plays by removing punts, field goals, kneeldowns, spikes, and 4th down plays. Grouped remaining plays by down, distance bucket (short 1-3, medium 4-7, long 8+), and play type. Calculated average EPA and success rate for each combination with a minimum of 50 plays per bucket to ensure statistical reliability.
