## Fig_6_code_implementation.ipynb
This notebook presents implementation of our closure model in python to predict turbulent transport for all $(r, \mathrm{Pr})$ in Fig. 6(a).


## GSF_r_Pr_scan__Shear_eq_3.h5
This file contains data output from the $(r, \mathrm{Pr})$-scan of the closure model, obtained using "Fig_6_code_implementation.ipynb".  The h5 data file can be simply read using the following lines of code:

```
import h5py
hf=h5py.File('~/GSF_r_Pr_scan__Shear_eq_3.h5', 'r')
ux_uy = hf['ux_uy/ux_uy/ux_uy'][()]
ux_th = hf['ux_th/ux_th/ux_th'][()]

Pr_exp = np.linspace(0.02, 7, 28)
Pr_array = 10**(-Pr_exp) #These are the values of Pr for which the transport is computed.

r_exp = np.linspace(0.02, 5, 20)
r_array  = 10**(-r_exp)  #These are the values of  r for which the transport is computed.
```
