# DataScience
Data sciecne projects including AI
Problem Statement
We have energy production data of Spain which is generating from multiple sources like solar system, wind system and other sources. We'll try to solve some use cases related to this data which we will discuss this below.

Business Context:

Day-ahead energy forecasting is critical for:

-> Grid balancing

-> Market bidding

-> Dispatch scheduling

-> Reserve planning

Usual key modeling challenges with these kind of data:
-> Strong daily seasonality (24h)

-> Annual seasonality (8760h)

-> High intermittency (solar zero at night)

-> Wind volatility

-> Extreme outliers (weather spikes)

-> Heteroscedastic variance

Going foreward we'll see which all are applicable with this data.

Modelling Strategy
We'll try to build multiple models using below data seperately:

Combined Model( Wind + Solar + Other)

Solar Model

Wind Model

Data Format Summary
. The dataset is a multivariate time series representing energy production.

. Frequency: Hourly observations (1-hour resolution).

. Time span: 2020–2025, split into train (2020–2023), validation (2024), and test (2025).

. Time index constructed using:

. Date

. Start_Hour

. End_Hour → Combined into a proper datetime index (start_datetime).

. Target variables:

. Solar generation

. Wind generation

. Total production (Solar + Wind)

Solar Energy Forecast
We'll first perform solar energy forecast. Daily Day ahead Energy forecast(aggregate) then map it to the hourly.
