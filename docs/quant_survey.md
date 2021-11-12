# Quantitative Survey and Dataset


## Overview

This survey included which 2,769 redditors who identified as members of 2,151 different subreddits. Each particpant was asked, for each subreddit they consider themselves a member of, about 9 different values:

1. Quality of Content
1. Variety of Content
1. Trust
1. Community Engagement
1. Safety
1. Participation and Inclusion
1. Diversity
1. Size
1. Democracy

For each of the above values, we ask about 3 different dimensions:

1. The *Importance* of the value
1. The *Current State* of the value
1. The *Desired Change* of the value

For more details, see the [survey instrument](https://github.com/behavioral-data/reddit_values_surveys_public/raw/master/instruments/quant_survey_instrument.pdf).

We make these anonymized responses public, along with some additional questions about participants' overall reddit usage.

## Paper

For more details, see our [paper on arXiv](https://arxiv.org/pdf/2111.05835).

## Dataset

Download our dataset [here](https://github.com/behavioral-data/reddit_values_surveys_public/raw/master/subreddit_values.csv). If you use this dataset for your own academic work, please be sure to cite our paper:

```
@misc{weld2021makes,
      title={What Makes Online Communities 'Better'? Measuring Values, Consensus, and Conflict across Thousands of Subreddits}, 
      author={Galen Weld and Amy X. Zhang and Tim Althoff},
      year={2021},
      eprint={2111.05835},
      archivePrefix={arXiv},
      primaryClass={cs.SI}
}
```

Please note that a small number of responses have been removed at the request of the participants or for confidentiality concerns. 

### Schema

The downloadable dataset consists of 27 columns (9 values x 3 dimensions) plus 4 overall reddit usage questions.

#### Importance

The Importance columns are named *e.g.*, `quality_rank` for the Importance of Quality. Each value is on an integer scale 1-9, where 1 is the most important and 9 is the least important.

#### Current State

The Current State columns are named *e.g.*, `quality_current` for the Current State of Quality. Each value is on an integer scale 0-11, where 0 is the lowest possible current state, and 11 is the highest.

#### Desired Change

The Desired Change columns are named *e.g.*, `quality_change` for the Desired Change of Quality. Each value is on an integer scale -1 to +1, where -1 is decrease, 0 is "keep as is", and +1 is increase.

#### Overall Reddit Usage

In addition, we include 4 columns describing participants' overall reddit usage:

| `lurker`       | An integer in range \[0,3\] describing how much the the participant posts on reddit, where 3 is never and 0 is frequently.                                         |
| `aggregate`    | An integer in the range \[0,4\] describing how often the participant uses aggregate subreddits (*e.g.*, their front page), where 0 is never and 4 is exclusively.  |
| `platform`     | An integer in the range \[-2,2\] describing whether the participant uses reddit more from their computer (-2) or their phone (2).                                  |
| `usage_amount` | The approximate amount of time the participant spends on reddit, in minutes per day.                                                                               |


## Survey Instrument

The survey instrument is available [here](https://github.com/behavioral-data/reddit_values_surveys_public/raw/master/instruments/quant_survey_instrument.pdf).
