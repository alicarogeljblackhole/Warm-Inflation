# Warm-Inflation
Mathematica .nb simulating warm inflation/smooth reheating dynamics. Result: fully numerical power spectrum, spectral tilt, tensor-to-scalar ratio.



Implements gauge-invariant evolution equations describing smooth reheating, derived in [2407.17074](https://doi.org/10.1088/1475-7516/2024/10/040), with noise treatment as derived in [2507.12849](https://doi.org/10.1088/1475-7516/2025/12/058). These theoretical foundations, as well as line-by-line description of the code, can be found in Appendix A of A. Rogelj' PhD thesis: $\text{Scalar perturbations in warm inflation and/or smooth reheating}$ [doi:10.48620/101166](https://doi.org/10.48620/101166).


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


In ``Warm_Inflation_main.nb``, modify section ``Model-dependent inputs``. Then run the entire notebook. See selected results by opening the section ``Results`` $\rightarrow$ ``see results``. The notebook is by default set up to compute results for $\textit{Warm inflation with the Standard Model}$ proposal introduced in 2503.18829.


For feedback, questions, requests, please email: ``alica.rogelj@unibe.ch``.


**NOTE**: 
Main nb is being continuously optimized (such that it works faster for more models). More nb examples shall be provided in due course. If you have suggestions for improvement, any questions, if you want help optimizing the code for your particular model, or anything else, please send me a quick email: alica.rogelj@gmail.com. Many thanks for your inputs!
