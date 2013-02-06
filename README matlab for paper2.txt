Matlab code for paper 2 aka "Analytical expression for transient radial concentration of autocatalytic carboxylic acid end groups in PLGA microspheres"
Five files in directory MIT Postdoc\Drug Delivery\Analytical Solution Single Component\From Dissertation\full analytical derivation\

(1) analytical_single_component.m
c(r,t) general case for autocatalyst
produces fig. 1 c/ct0 vs. r vs. alpha t and kt plots for each phi value

(2) analytical_single_compare.m 
produces figs. 3 and 4
dimensionless autocatalyst concentration profiles c/ct0 at r=0 for cr1=0
used intermediate and large values of phi
adapated from single_i_verif_compare.m from dissertation
Reads analytical_compare_data.m

(3) DanPackFDspherical.m 
based on DanPackFD_NIHproposal.m from 2006 from Braatz for original proposal
numerical solution to the reaction-diffusion equation for a sphere 
with constant surface concentration and initially flat internal concentration,
with first-order generation reaction and constant diffusion coefficient
$\frac{\partial c}{\partial (alpha t)}=\frac{1}{r^2}\frac{\partial}{\partial r}\left(r^2\frac{\partial c}{\partial r}\right)+\Phi^2c$
not explicitly used, though referred to. only steady-state values shown (see steadystateplot.m)

(4) steadystateplot.m
produces fig. 5
steady-state dimensionless autocatalyst concentration profiles for cr1>0 and phi<pi 

(5) cr0t.m
called by analytical_single_compare.m to compute COOH_single_an=c(r=0,t) at cr1=0