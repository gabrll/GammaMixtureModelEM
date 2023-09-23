# GammaMixtureModelEM
Gamma Mixture Model estimation with EM algorithm.
This code estimates the components of a finite mixture model following a Gamma distribution with the EM algorithm.
Author: Gonzalo Vegas Sánchez-Ferrero
----how to use it-----
Syntax: [w, alpha, beta] = GMMestimator(y,nl,maxIter,tol_error,flag_pinta,w_0,alpha_0,beta_0)
Inputs:
y - vector of samples
nl - number of mixture components.
maxIter - Maximum number of iterations
tol_error - Tolerance assumed for convergence
flag_pinta - Flag to show the evolution of fitting
w_0 = initial weights size (1 x nl). They should sum up to 1. (optional)
alpha_0 = initial alpha parameter of each Gamma component (size: 1 x nl) (optional)
beta_0 = initial beta parameter of each Gamma component (size: 1 x nl) (optional)

outputs:
w - vector of weights for component
alpha - vector of alphas
beta - vector of betas
The components are ordered by decresing weights.
example:
Y = [gamrnd(2,3,1,1000) gamrnd(2,5,1,1000) gamrnd(2,7,1,3000)];
[prob, alpha_gamma, beta_gamma] = GMMestimator(Y,3,70,1e-5,1);
If you use this sofware for research purpose, please cite

G. Vegas-Sánchez-Ferrero, M. Martín-Fernández, J. Miguel Sanches "A Gamma
Mixture Model for IVUS Imaging", Multi-Modality Atherosclerosis Imaging
and Diagnosis. Editors: Luca Saba, João Miguel Sanches, Luís Mendes
Pedro, Jasjit S. Suri ISBN: 978-1-4614-7424-1 (Print) 978-1-4614-7425-8
(Online), Pages 155-171. 2014.
