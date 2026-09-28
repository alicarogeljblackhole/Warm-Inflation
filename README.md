# Warm-Inflation
Mathematica notebook simulating warm inflation/smooth reheating dynamics. Result: fully numerical power spectrum, spectral tilt, tensor-to-scalar ratio.



The theoretical foundations, as well as line-by-line description of the code, can be found in A. Rogelj' PhD thesis [doi:10.48620/101166](https://doi.org/10.48620/101166). The derivation of gauge-invariant evolution equations describing smooth reheating was first presented in [2407.17074](https://doi.org/10.1088/1475-7516/2024/10/040), with noise treatment originally derived in [2507.12849](https://doi.org/10.1088/1475-7516/2025/12/058). 


Properties of equations/solutions:

- fully gauge-invariant equations,
- smooth interpolation between the initial quantum state and subsequent classical domains,
- allows for time-dependent $\Upsilon$,
- dynamical treatment of inflaton equilibration, rather than assuming it from the start,
- no slow-roll approximation,
- obtain fully numerical, quantum-statistical power spectrum average


Input model parameters:

- dissipation coefficient $\Upsilon$, monomial inflaton potential $V$, radiation energy density $e_r$ and pressure $p_r$.



Outputs: 

- .wxf file with full time evolution of background quantities: $H$, $T$, $k/a$, $\Upsilon$, $e_r$, $p_r$, background energy density and pressure $\bar{e}$ and $\bar{p}$, $V$, background inflaton field $\bar{\varphi}$, $\dot{\bar{\varphi}}$, $\dot{T}$, $\dot{H}$,
- .wxf file with full time evolution of power spectrum of inflaton and plasma curvature perturbations: $\mathcal{R}_\varphi$, $\mathcal{R}_v$, $\mathcal{R}_T$,
- .wxf file with key background quantities computed at horizon exit, as well as the power spectra, $n_s$, and $r$ evaluated during the freeze-out,
- .pdf file with time evolution of background quantities: $H$, $\Upsilon$, $T$, $k/a$,
- .pdf file with time evolution of power spectra.


Quick instructions:

In ``Warm_Inflation_main.nb``, modify section ``Model-dependent inputs``. Then run the entire notebook. See selected results by opening the section ``Results`` $\rightarrow$ ``see results``. See Appendix A of [doi:10.48620/101166](https://doi.org/10.48620/101166) for more details. The notebook is by default set up to compute results for ``Warm inflation with the Standard Model'' proposal introduced in 2503.18829. 

For convenience, we provide explicit example notebooks obtained for various inflaton potentials and friction coefficients:

- Warm_Inflation_A: quartic potential, SM friction coefficient
  
$V=\lambda \varphi^4$, $\Upsilon=\frac{T^2}{2f_a^2}\left(\frac{1}{\alpha^5 N_c^5 T}+\frac{2N_f}{N_c H}\right)^{-1}$
- Warm_Inflation_B: quadratic potential, SM friction coefficient

$V=\frac{m^2}{2} \varphi^2$, $\Upsilon=\frac{T^2}{2f_a^2}\left(\frac{1}{\alpha^5 N_c^5 T}+\frac{2N_f}{N_c H}\right)^{-1}$
- Warm_Inflation_C: cosine potential, const.+T^3 friction coefficient
   
$V=m^2 f_a^2 \left(1-\cos{\frac{\varphi}{f_a}} \right)$, $\Upsilon=\frac{\kappa_T(\pi T)^3+\kappa_m m^3}{(4\pi)^3 f^2_a}$

Notebooks can of course be modified to explore parameter space, test new models, etc. Main nb is being continuously optimized (such that it works faster for more models). More nb examples shall be provided in due course. 


**NOTE**: 

For feedback, questions, requests or comments, please do not hesitate to email: ``alica.rogelj@gmail.com``. Many thanks for your inputs!
