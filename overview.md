# Reddit Mental Health Sentiment Analysis: COVID-19 Impact Study

Author: Anthony Behery

## Project Overview

This project analyzes sentiment patterns in Reddit mental health communities (r/depression, r/mentalhealth, r/Anxiety) over a 5-year period (2020-2025) to understand how the COVID-19 pandemic affected mental health discourse online. The analysis uses VADER sentiment analysis and tracks specific COVID-related terminology to measure changes in community sentiment before, during, and after the pandemic.

## Important Safety and Ethics Disclaimer

### Data Sensitivity Warning
This project analyzes data from mental health support communities where individuals share deeply personal experiences, including discussions of:

- Depression and anxiety

- Suicidal ideation

- Self-harm

- Trauma and crisis situations

- Medical and therapeutic experiences

**⚠️ CRITICAL SAFETY CONSIDERATIONS:**

1. **This analysis is for research purposes only** and should NOT be used to:
   - Diagnose or assess individual mental health conditions
   - Replace professional mental health services
   - Make clinical decisions
   - Identify or target vulnerable individuals

2. **Ethical Responsibilities:**
   - All data analysis must respect user privacy and anonymity
   - No attempts should be made to identify individual users
   - Results should be presented in aggregate form only
   - Findings should not stigmatize mental health conditions

3. **Content Warning:**
   - The raw data may contain triggering content
   - Researchers should practice self-care and take breaks when needed
   - If you're experiencing mental health challenges, please seek professional help

4. **Limitations:**
   - Online posts may not accurately represent clinical mental health states
   - Self-selection bias affects who participates in these communities
   - Sentiment analysis tools have limitations with nuanced emotional expression
   - Results cannot be generalized to all individuals with mental health conditions

## Project Structure

### Data Collection
- **`collecting_over_5_years.ipynb`**: Collects Reddit posts from mental health subreddits using the PullPush API
  - Fetches up to 100 posts per month per subreddit
  - Covers January 2020 to November 2025
  - Includes r/depression, r/mentalhealth, and r/Anxiety

### Data Processing
- **`data_cleaning.ipynb`**: Cleans and prepares the raw Reddit data
  - Handles missing values and data formatting
  - Removes deleted content
  - Prepares text for analysis

### Analysis Notebooks
- **`data_analysis.ipynb`**: Main sentiment analysis using VADER
  - Calculates compound, positive, negative, and neutral sentiment scores
  - Groups data by year and COVID period (Pre/During/Post)
  - Visualizes sentiment trends over time

- **`covid_specific_data.ipynb`**: Tracks COVID-related terminology
  - Monitors pandemic-specific vocabulary
  - Analyzes therapy and mental health service terminology
  - Measures changes in isolation/lockdown language

- **`data_word_frequency.ipynb`**: Word frequency analysis
  - Identifies common themes and topics
  - Tracks vocabulary changes over time

## Key Findings Structure

The analysis reveals sentiment patterns across three periods:
- **Pre-COVID** (before March 2020)
- **During COVID** (March 2020 - May 2023)
- **Post-COVID** (after May 2023)

## Dependencies

```python
asttokens                 3.0.0
attrs                     25.4.0
beautifulsoup4            4.14.2
bleach                    6.3.0
blinker                   1.9.0
certifi                   2025.10.5
charset-normalizer        3.4.4
click                     8.3.0
comm                      0.2.3
contourpy                 1.3.3
cycler                    0.12.1
dash                      3.2.0
debugpy                   1.8.17
decorator                 5.2.1
defusedxml                0.7.1
executing                 2.2.1
fastjsonschema            2.21.2
filelock                  3.20.0
Flask                     3.1.2
fonttools                 4.60.1
fsspec                    2025.10.0
hf-xet                    1.2.0
huggingface-hub           0.36.0
idna                      3.11
importlib_metadata        8.7.0
ipykernel                 7.1.0
ipython                   9.6.0
ipython_pygments_lexers   1.1.1
itsdangerous              2.2.0
jedi                      0.19.2
Jinja2                    3.1.6
joblib                    1.5.2
jsonschema                4.25.1
jsonschema-specifications 2025.9.1
jupyter_client            8.6.3
jupyter_core              5.9.1
jupyterlab_pygments       0.3.0
kiwisolver                1.4.9
MarkupSafe                3.0.3
matplotlib                3.10.7
matplotlib-inline         0.2.1
mistune                   3.1.4
mpmath                    1.3.0
narwhals                  2.10.0
nbclient                  0.10.2
nbconvert                 7.16.6
nbformat                  5.10.4
nest-asyncio              1.6.0
networkx                  3.5
nltk                      3.9.2
numpy                     2.3.4
nvidia-cublas-cu12        12.8.4.1
nvidia-cuda-cupti-cu12    12.8.90
nvidia-cuda-nvrtc-cu12    12.8.93
nvidia-cuda-runtime-cu12  12.8.90
nvidia-cudnn-cu12         9.10.2.21
nvidia-cufft-cu12         11.3.3.83
nvidia-cufile-cu12        1.13.1.3
nvidia-curand-cu12        10.3.9.90
nvidia-cusolver-cu12      11.7.3.90
nvidia-cusparse-cu12      12.5.8.93
nvidia-cusparselt-cu12    0.7.1
nvidia-nccl-cu12          2.27.5
nvidia-nvjitlink-cu12     12.8.93
nvidia-nvshmem-cu12       3.3.20
nvidia-nvtx-cu12          12.8.90
packaging                 25.0
pandas                    2.3.3
pandocfilters             1.5.1
parso                     0.8.5
pexpect                   4.9.0
pillow                    12.0.0
pip                       25.3
platformdirs              4.5.0
plotly                    6.3.1
praw                      7.8.1
prawcore                  2.4.0
prompt_toolkit            3.0.52
psutil                    7.1.2
ptyprocess                0.7.0
pure_eval                 0.2.3
Pygments                  2.19.2
pyparsing                 3.2.5
python-dateutil           2.9.0
pytz                      2025.2
PyYAML                    6.0.3
pyzmq                     27.1.0
referencing               0.37.0
regex                     2025.10.23
requests                  2.32.5
retrying                  1.4.2
rpds-py                   0.28.0
safetensors               0.6.2
scikit-learn              1.7.2
scipy                     1.16.3
setuptools                80.9.0
six                       1.17.0
soupsieve                 2.8
stack-data                0.6.3
sympy                     1.14.0
threadpoolctl             3.6.0
tinycss2                  1.4.0
tokenizers                0.22.1
torch                     2.9.0
tornado                   6.5.2
tqdm                      4.67.1
traitlets                 5.14.3
transformers              4.57.1
triton                    3.5.0
typing_extensions         4.15.0
tzdata                    2025.2
update-checker            0.18.0
urllib3                   2.5.0
vaderSentiment            3.3.2
wcwidth                   0.2.14
webencodings              0.5.1
websocket-client          1.9.0
Werkzeug                  3.1.3
wordcloud                 1.9.4
zipp                      3.23.0
```

## Usage Guidelines

1. **Before Running:**
   - Review all safety disclaimers
   - Ensure you have appropriate IRB approval if conducting academic research
   - Consider the ethical implications of your analysis

2. **Running the Analysis:**
   - Execute notebooks in order: collection → cleaning → analysis
   - Data collection respects API rate limits
   - Analysis focuses on aggregate patterns, not individual posts

3. **Interpreting Results:**
   - Remember correlation does not imply causation
   - Consider multiple factors affecting mental health discourse
   - Acknowledge limitations in methodology

## Data Privacy and Storage

- No personally identifiable information should be stored
- Follow Reddit's terms of service and API guidelines
- Store data securely and limit access
- Delete data when analysis is complete

## Resources for Mental Health Support

If you or someone you know is struggling with mental health:

- **National Suicide Prevention Lifeline**: 988 (US)
- **Crisis Text Line**: Text HOME to 741741
- **International Crisis Lines**: findahelpline.com
- **Reddit Crisis Resources**: reddit.com/r/SuicideWatch/wiki/hotlines

## Contributing and Contact

This project is for research purposes. Any contributions should:
- Maintain ethical standards
- Respect the sensitivity of the data
- Include appropriate disclaimers
- Focus on aggregate insights

---

**Remember**: Behind every data point is a real person seeking support. Treat this data with the respect and care it deserves.