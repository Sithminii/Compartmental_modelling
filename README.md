# Simple Plasma Glucose/Insulin Model, Riggs Iodine Model and Bolies' Plasma Glucose Model

## Repository Contents

This repository contains code and documentation which explores three different physiological models: the Simple Plasma Glucose/Insulin Model, the Riggs Iodine Model and the Bolies' Plasma Glucose Model. Below is a brief introduction to each model and the work conducted in this project:

## 1.  Simple Plasma Glucose/Insulin Model

In this section, I developed a simple plasma glucose/insulin model to simulate changes in insulin and glucose levels in response to external inputs. The model is represented by the following set of differential equations:

      𝑑𝑖/𝑑𝑡 = -0.8𝑖 + 0.2𝑔
      𝑑𝑔/𝑑𝑡 = -5𝑖 - 2𝑔 + 𝐴(𝑡)

Here, 𝑖 represents the deviation in insulin level from normal (in international units/kg), and 𝑔 represents the deviation in glucose level (g/kg). I initially simulated the response to a step input 𝐴(𝑡) = 1 g/kg/h for 𝑡 > 0 and later modified the equations to model a bolus input.

## Simulation Scenarios:
Simulated changes in 𝑖 and 𝑔 over a 4-hour period with 𝑖 and 𝑔 initially set to zero.
Modeled a diabetic subject and a diabetic subject with insulin infusion of 100 mU/kg/h in response to the step input.

## 2. Riggs Iodine Model

Riggs Iodine Model is a model implemented to simulate iodine metabolism in response to changes in iodine intake. The model is used to explore the effects of varying iodine intake on thyroid function. Specifically, I simulated a sudden drop in iodine intake from 150 μg to 15 μg per day. The set of equations used here are listed below. The coefficients were adjusted according to each scenario.

      𝑑𝐼/𝑑𝑡 = −2.52𝐼 + 0.08𝐻 + 15
      𝑑𝐺/𝑑𝑡 = 0.84𝐼 − 0.01𝐺
      𝑑𝐻/𝑑𝑡 = 0.01𝐺 − 0.1𝐻

## Simulation Scenarios:
  Simulated the response to a sudden drop in iodine intake from 150 μg to 15 μg per day.
  Produced plots for two time frames: 0-10 days and 0-300 days.
  Explored the simulation of thyroid diseases by altering model parameters, including:
    Hypothyroidism due to autoimmune thyroid disease
    Hypothyroidism due to low iodine intake
    Hyperthyroidism due to Grave's disease
  Investigated common causes of goitre and tumors and discussed how they can be simulated in the Riggs' model.
Please refer to the individual folders and code files in this repository for detailed implementation and results of each model and simulation scenario.

## 3. Bolies' Plasma Glucose Model

Bolies' plasma glucose model is a mathematical representation of the dynamics of plasma glucose (g) and insulin (i) concentrations in the body. This model allows us to explore how the interplay between insulin secretion, glucose uptake, and external inputs affects blood glucose levels. It is a powerful tool for studying glucose homeostasis and understanding the impact of different factors on blood glucose levels.

      𝑑𝑔(𝑡)/𝑑𝑡 = –𝑘4𝑔(𝑡) – 𝑘6𝑖(𝑡) + 𝐴(𝑡)
      𝑑𝑖(𝑡)/𝑑𝑡 = 𝑘3𝑔(𝑡) – 𝑘1𝑖(𝑡) + 𝐵(𝑡)

## Simulation Scenarios:
I have implemented Bolies' plasma glucose model equations into Simulink. These equations describe how plasma glucose and insulin levels change over time in response to various inputs.

Simulation with Different Coefficients: I have conducted simulations using different sets of coefficients to observe how changes in these coefficients influence the behavior of the model. This exploration allows us to understand the sensitivity of the model to different parameters.
I derived an analytical solution for Bolies' model equations and compared the simulation results with this solution. This comparison helps us assess the stability and accuracy of the model.

## Results
You will find the simulation results, including plots and data, obtained from running the three compartment models with various inputs and coefficients. These results provide insights into how different parameters affect glucose and insulin dynamics.
