HydroGPTdataProcessingApp v1.1

Released by Zhonghao Zhang & Caterina Valeo

HydroGPT‑Fuzzy Application
Functional Overview & What’s New

This Python/Tkinter GUI unifies a complete hydrological data workflow—from raw data retrieval and cleaning through fuzzy uncertainty analysis and GPT‑based modeling—into a single, user‑friendly application.

Core Features
Card‑Based Login
<img width="513" height="436" alt="image" src="https://github.com/user-attachments/assets/9d56b74d-8bb6-44da-a3c4-63816c289342" />


Secure entry via smart‑card number & password

Remote server authentication to prevent unauthorized use

Hydrodata Mining

Weather Data Scraper: Fetch daily/hourly climate observations (e.g., rainfall, temperature) from public sources; parse, clean, and export to CSV.

Flow Gauge Scraper (NEW!): Download river flow measurements from gauge networks; auto‑clean and export.

Hydrological File Processing

Data Cleaning: Load CSV/Excel, filter out invalid or null entries, and save cleaned data.

Extract & Merge: Select common columns across multiple files, merge by timestamp (pairwise or bulk), and export unified datasets.

GPT Processing

GPT Config: Define API keys, model parameters, and prompt templates.

Multi‑turn JSON: Transform tabular data into JSONL chat sequences for GPT‑based inference or fine‑tuning.

Call Fine‑tuning Model: Submit JSONL to OpenAI’s fine‑tuning endpoint and manage jobs.

JSONL Parser: Regex‑based extraction of structured outputs from GPT responses for downstream analysis.

Fuzzy Analysis

Support for triangular and trapezoidal membership functions on numeric columns.

Compute α‑cuts, membership values, and visualize uncertainty intervals interactively.

Export fuzzy‑interval data to CSV/Excel for further use.

Model Evaluation (NSE)

Load observed vs. simulated time series.

Calculate performance metrics: R², Nash‑Sutcliffe Efficiency (NSE), RMSE, MAE.

Generate observed‑vs‑simulated plots for visual validation.

What’s New in This Version
Flow Gauge Scraper tab integrated alongside the existing Weather Scraper to automate retrieval of river flow data from online gauge services.

Card‑Based Login mechanism added to secure the application and restrict access to authorized users.

Unified all major data‑processing steps—climate scraping, hydrological cleaning/merging, GPT workflows, fuzzy uncertainty analysis, and performance evaluation—into a single tabbed interface for seamless end‑to‑end operation.

Getting Started:

Login: Insert your card credentials.

Select a Tab from the menu or File/Workflow menus to run each pipeline stage.

Export results at any stage in CSV/Excel or JSONL formats.

For detailed instructions, please see the built‑in help in each tab or refer to the online README.
