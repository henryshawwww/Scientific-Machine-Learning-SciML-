# Scientific-Machine-Learning-SciML-

Final project code for **EN.560.652.01.FA25 – Scientific Machine Learning for Dynamics and Control**.

Goal: short-term forecasting of whole-building **HVAC power** using the **AlphaBuilding Synthetic Building Operation Dataset**, and comparing:

- Persistence baseline  
- Linear regression  
- Random forest  
- LSTM sequence model  
- **Euler-discretized Neural ODE (SciML method)**  

Results and figures in the final report are generated from this repo.

---

## 1. Main files

- `SciML_FINAL.ipynb` – main notebook (data loading, training, evaluation, plots).  
- `sciml_final.py` – same logic in script form (data loader + models + training loops).  
- `fig_mape_bar.png` – test MAPE comparison (used in report).  
- `fig_rmse_bar.png` – test RMSE comparison.  
- `fig_day_timeseries.png` – one representative test day: Ground truth vs LSTM vs Euler-NODE.

---

## 2. Dataset access (AlphaBuilding from S3)

The notebook reads directly from the public **OEDI** S3 bucket:

- HDF5 file:  
  `s3://oedi-data-lake/building_synthetic_dataset/A_Synthetic_Building_Operation_Dataset.h5`
