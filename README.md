# Virat Kohli Performance Analysis and Prediction   

## Overview  
This project focuses on analyzing and predicting the performance of cricketer **Virat Kohli**. It includes:  
- Building predictive models using **Random Forest** and **Neural Networks** to achieve 85% prediction accuracy for Kohli's scores.  
- Creating **interactive Power BI dashboards** for visualizing Kohli's performance across various cricket formats (ODI, T20, TEST).  
- Deploying the prediction model on a **Dockerized Flask platform** for a real-time interactive experience.  

---

## Features  
1. **Performance Visualization**:  
   - Visualized Kohli's performance metrics like total runs, centuries, strike rates, and averages using **Power BI dashboards**.  
   - The dashboards provides various insights across the formats as below :
     
     https://private-user-images.githubusercontent.com/116452492/402375670-55ca6f73-dc29-4d15-9799-862d960fbf37.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzY3MDQxODIsIm5iZiI6MTczNjcwMzg4MiwicGF0aCI6Ii8xMTY0NTI0OTIvNDAyMzc1NjcwLTU1Y2E2ZjczLWRjMjktNGQxNS05Nzk5LTg2MmQ5NjBmYmYzNy5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwMTEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDExMlQxNzQ0NDJaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT01NmMxZTE5MDI2ZGI0MDhmOGMwYjM3YWQ4YWExOWE4M2NmZGJjNDU0MTAwMzJjMTJiZGYwZWU3YzU5ZDg0MjdmJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.k6f3kCi1TiqTH19hZ-mV5kK30cYw_Gg4ZJIuQHJRAw4

     https://private-user-images.githubusercontent.com/116452492/402375711-8f6b8e48-9454-4048-bd4a-f3835f8272f9.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzY3MDQxMzQsIm5iZiI6MTczNjcwMzgzNCwicGF0aCI6Ii8xMTY0NTI0OTIvNDAyMzc1NzExLThmNmI4ZTQ4LTk0NTQtNDA0OC1iZDRhLWYzODM1ZjgyNzJmOS5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwMTEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDExMlQxNzQzNTRaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT1jNGIxYmQ4MTdhOGFlMmVlMjQzOTdkYjA1ZWQxNmFmNWZiODRlM2ZiMDJhMWUwZjYzMjQwMDM1M2QxMzZiMDRlJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.hG8JaA1SIs4XsOb4pafwMmJRNVjbd8woe9gHmgLNryU

     https://private-user-images.githubusercontent.com/116452492/402375768-6c9dbb13-c5f5-4beb-ab21-008982fd0018.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MzY3MDQxODAsIm5iZiI6MTczNjcwMzg4MCwicGF0aCI6Ii8xMTY0NTI0OTIvNDAyMzc1NzY4LTZjOWRiYjEzLWM1ZjUtNGJlYi1hYjIxLTAwODk4MmZkMDAxOC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjUwMTEyJTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI1MDExMlQxNzQ0NDBaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT0xMDRiNjU0ZjUwMzZhMmEwNDY5Zjc4Y2M1MjdlNTA1MTg4OTRjNWM0OTYxYTUzOTM4OWEzYTBjZTBmOGViNjMyJlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCJ9.9-aMvWGunw9Wf2MANMWdzgEDScqOp14SSeYEpuIHgpE

     

2. **Predictive Modeling**:  
   - Built a machine learning model to predict Kohli's score based on:  
     - **Opponent**  
     - **Venue**  
     - **Match Format (ODI, T20, TEST)**  
   - Achieved an **85% prediction accuracy** using **Random Forest** and **Neural Network models**.  

3. **Deployment**:  
   - The prediction model is deployed on a **Dockerized Flask platform** for real-time interaction.  

---

## Technologies Used :

- Machine Learning: Random Forest, Neural Networks
- Data Visualization: Power BI
- Web Development: Flask
- Containerization: Docker

---

