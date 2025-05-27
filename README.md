# UFC Fight Statistics Dataset

## Overview

This dataset contains detailed statistics from **UFC (Ultimate Fighting Championship)** fights, scraped from [ufcstats.com](http://ufcstats.com/). It includes information about each event and fight, along with comprehensive performance metrics for every fighter — both overall and per round.

Whether you're building predictive models, analyzing trends, or exploring structured combat sports data, this dataset is built to support a wide range of applications.

---

## Key Details

- **Scraping Date:** 2025-05-26  
- **Data Source:** [ufcstats.com](http://ufcstats.com/)  
- **File Format:** CSV  
- **Filename:** `output.csv`  
- **Structure:** One row per fight (see column breakdown below)

---

## File Structure / Columns

### General Event & Fight Information

| Column                | Description                            |
|-----------------------|----------------------------------------|
| `event_name`          | Name of the UFC event                  |
| `event_date`          | Date of the event                      |
| `event_location`      | Location of the event                  |
| `event_details_url`   | Link to full event page on ufcstats    |
| `fight_stats_page_url`| Link to specific fight's stats         |
| `weight_class`        | Weight class of the fight              |

### Fight Header / Outcome Details  
(Prefixed as `fighter_a_` and `fighter_b_`)

| Column                    | Description                                |
|---------------------------|--------------------------------------------|
| `fighter_a_name`          | Fighter A’s name                           |
| `fighter_a_nickname`      | Fighter A’s nickname                       |
| `fighter_a_outcome`       | W/L/D outcome for Fighter A                |
| `fighter_b_name`          | Fighter B’s name                           |
| `fighter_b_nickname`      | Fighter B’s nickname                       |
| `fighter_b_outcome`       | W/L/D outcome for Fighter B                |
| `winner_name`             | Winner’s name or "Draw"/"N/A"             |
| `method_detailed`         | KO, TKO, Submission, Decision, etc.        |
| `round_detailed`          | Round when the fight ended                 |
| `time_detailed`           | Time into the round when it ended          |
| `time_format_detailed`    | Scheduled round format (e.g., "3 Rnd (5-5-5)") |
| `referee_detailed`        | Referee’s name                             |
| `finish_details_detailed` | Specific notes about the fight’s finish    |

### Fighter Statistics (Overall)  
(Prefixed by fighter: `fighter_a_`, `fighter_b_`)

| Column                 | Description                              |
|------------------------|------------------------------------------|
| `kd`                   | Knockdowns                               |
| `sig_str_landed`       | Significant strikes landed               |
| `sig_str_attempted`    | Significant strikes attempted            |
| `sig_str_pct`          | Sig strike accuracy (e.g., 0.55)         |
| `total_str_landed`     | Total strikes landed                     |
| `total_str_attempted`  | Total strikes attempted                  |
| `td_landed`            | Takedowns landed                         |
| `td_attempted`         | Takedowns attempted                      |
| `td_pct`               | Takedown accuracy (e.g., 0.33)           |
| `sub_att`              | Submission attempts                      |
| `rev`                  | Reversals                                |
| `ctrl_time_seconds`    | Control time (in seconds)                |

### Significant Strike Breakdown

Each of these appears twice (once per fighter), such as `fighter_a_sig_strikes_head_landed` and `fighter_b_sig_strikes_head_landed`.

- `sig_strikes_head_landed`, `sig_strikes_head_attempted`
- `sig_strikes_body_landed`, `sig_strikes_body_attempted`
- `sig_strikes_leg_landed`, `sig_strikes_leg_attempted`
- `sig_strikes_distance_landed`, `sig_strikes_distance_attempted`
- `sig_strikes_clinch_landed`, `sig_strikes_clinch_attempted`
- `sig_strikes_ground_landed`, `sig_strikes_ground_attempted`

### Per-Round Statistics

Per-round data may appear as:
- Flattened columns (e.g., `fighter_a_r1_kd`, `fighter_b_r3_sig_str_head_landed`)
- Multiple rows per fight (one per round)
- Omitted entirely depending on how `output.csv` is generated

Inspect the actual CSV to determine how round data is represented.

---


---

## Potential Uses

- Analyze trends in fight outcomes, finish types, and styles
- Build predictive models using fighter stats
- Research historical UFC performance
- Train machine learning models or LLMs with structured sports data
- Develop fan or fantasy sports apps

---

## Data Quality Notes

- Data was scraped from `ufcstats.com` as of 2025-05-26
- Accuracy depends on the source website
- Scraping errors may cause missing or malformed data for some fights
- Dataset is provided for research, analysis, and educational use only
- Please review [ufcstats.com](http://ufcstats.com)'s terms before redistributing or scraping

---

## How to Use

1. Download `output.csv`
2. Load it into Python, R, Excel, or another data tool
3. Inspect column names to understand actual field structure
4. Perform data cleaning or transformation as needed

---

## Questions or Contributions?

Feel free to open an issue or submit a pull request if you spot any problems or improvements. I had an LLM generate this description, and had another one review it for errors.

---


