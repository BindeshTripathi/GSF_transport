# fig_6_code_implementation.ipynb
Closure model is implemented in python to predict transport for all (r, Pr) in Fig. 6; see the file entitled "fig_6_code_implementation.ipynb".


# GSF_r_Pr_scan__Shear_eq_3.h5
The data output from the (r,Pr)-scan of the closure model is saved in the file named "GSF_r_Pr_scan__Shear_eq_3.h5".  The h5 file can be read by using the following lines of code:

```
import h5py
hf=h5py.File('/home/tripathi/2020/GSF/2D/preliminary_analysis_ONGOING/NEWEST/PAPER_plot_generator_predictions_vs_DNS/GSF_fig5_r_Pr_scan_Closure_data/GSF_r_Pr_scan__Shear_eq_3.h5', 'r')
ux_uy = hf['ux_uy/ux_uy/ux_uy'][()]
ux_th = hf['ux_th/ux_th/ux_th'][()]

Pr_exp = np.linspace(0.02, 7, 28)
Pr_array = 10**(-Pr_exp)

r_exp = np.linspace(0.02, 5, 20)
r_array  = 10**(-r_exp)
```
