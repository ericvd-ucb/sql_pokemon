# AGENTS.md — Econ 148 Jupyter Notebook Agent Instructions

## Project Purpose
This repository contains Jupyter notebooks for Econ 148: Data Science for Economists. The intended audience is upper division economics students who are learning how to use data to study topics like labor markets, trade shocks, monetary policy, and public finance. All notebooks are teaching materials, not production code.

## The goal is to teach students how to write code that mirrors the way economists explain evidence: slow, clear, and grounded in real-world questions. Every notebook should connect the code to an economics concept so that a student with no prior coding experience can follow along and understand each step.


## Primary Rule
Always optimize for student comprehension, never for code elegance or efficiency.
These two goals are often in direct conflict. Always choose comprehension. A student should be able to read the notebook and understand each chunk of code.


## Mandatory Code Constraints
- All code must be written in the global scope, executed sequentially cell by cell.
- Prefer lines of code to functions unless the notebook lesson is specifically teaching functions.
- Never use list comprehensions. Always use explicit for-loops.
- Never use lambda expressions.
- Never abstract repeated code into helpers. Repetition is acceptable and often 
  pedagogically valuable — students benefit from seeing the same pattern twice.
- Imports go in the first cell only, one per line, with a comment explaining 
  what each library does.
- When necessary use try;except blocks to import libraries that may not be installed, but do not add any error handling beyond printing an error message.
- Use descriptive economics-oriented variable names such as `household_income_data`, `gdp_growth_rates`, or `tariff_change_table`; never fall back to names like `df`, `df1`, or `temp`.
- When repeating similar code for different economic indicators, narrate the change (for example, “Now we compute real wage growth” or “Next we compare inflation across regions”) so students always see the link between the numbers and the economics story.

## Notebook Structure the Agent Must Follow
1. Start with a markdown cell stating the learning objective in one sentence and naming the economics concept students will explore.
2. Alternate markdown and code cells throughout. Never put two code cells in a row 
  without a markdown explanation between them, and make each explanation describe how the upcoming code connects to an economics question (for example, “This code calculates the unemployment rate for recent graduates”).
3. End with a markdown cell summarizing what the student just did and how the results inform the economics topic.

## Language and Explanation Level
- Explain as if the reader has never seen a concept before.
- Define every technical term the first time it appears, including economics vocabulary such as “elasticity,” “real wage,” or “counterfactual.”
- Never assume context. Never say "as you know" or "recall that."
- Preferred sentence length: short. Preferred vocabulary: common English words.
- After every chart or table, include one or two sentences explaining the economic intuition behind the numbers so students practice interpreting evidence.

## What the Agent Should Never Do
- Never wrap the main demo logic in a `main()` function or any equivalent.
- Never add error handling (try/except) unless the lesson is about error handling.
- Never generate a README or extra files unless explicitly asked.
- Never refactor working code to be "cleaner" — clarity of the original steps 
  matters more than clean code.
- Don't name dataframes `df`. Use descriptive names like `employment_status_data`, `inflation_series`, or `trade_balance_table`.
- Don't use generic variable names like `x` or `temp`. Use descriptive names that indicate their purpose, such as `total_exports`, `real_wage_change`, or `policy_counterfactual_result`.

## Econ 148 Data Source Notes
- CPS microdata: column names should reference the population slice, such as `cps_recent_grads` or `cps_low_income_households`.
- BEA national accounts: refer to tables explicitly (for example, `bea_gdp_components` or `bea_price_index_data`).
- IMF or World Bank macro series: include the country or region in the name, such as `imf_inflation_brazil` or `worldbank_gdp_subsaharan_africa`.
- Course-specific surveys: state the question theme in the name, for instance `campus_budget_survey` or `student_expectations_poll`.
