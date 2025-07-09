# Dynamic Pricing for Urban Parking Lots 🚗📈

## Overview

This project builds a real-time dynamic pricing engine for 14 urban parking spaces using real-time data streams and predictive models. It was developed as part of the Summer Analytics 2025 Capstone Project hosted by CAC × Pathway.

## Key Features

- 📊 Dynamic pricing models (3 levels)
- 🔄 Real-time simulation with Pathway
- 🧠 Demand estimation based on traffic, vehicle type, queue, and events
- 🗺️ Geo-based competitor awareness using haversine distance
- 📈 Bokeh visualizations for real-time pricing

## Models Implemented

### Model 1: Baseline Linear Model
Price increases linearly with occupancy:
Price = Previous_Price + α * (Occupancy / Capacity)

### Model 2: Demand-Based Pricing
Price adjusted using a weighted demand function of:
- Occupancy
- Queue Length
- Traffic
- Special Day
- Vehicle Type

### Model 3: Competitive Pricing
Includes influence of nearby parking lots within 0.5 km. Price adjusted based on competitor prices and lot occupancy.

## Tech Stack

- Python (Pandas, Numpy)
- Pathway (real-time simulation)
- Bokeh (visualization)
- Google Colab (execution)

## How to Run

1. Clone the repo.
2. Open `Capstone_Proj.ipynb` in Google Colab.
3. Upload the dataset and run all cells.
4. Modify pricing parameters or vehicle/traffic weights as needed.
5. Optional: Deploy with Pathway for live streaming.

## File Structure

├── Capstone_Proj.ipynb # Main notebook with all models and streaming logic
├── report.txt # Project report for submission
└── README.md # You're reading it!
