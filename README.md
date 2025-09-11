# FEMTIC-DABIC
FEMTIC-DABIC is a 3-D magnetotelluric (MT) inversion code developed based on FEMTIC (v4.2).

Unlike the original FEMTIC, FEMTIC-DABIC uses Brent line search in each iteration to find the statistically optimal regularization parameter (α) that maximizes the marginal likelihood function, which is a  function of α. 
We employ Akaike’s Bayesian Information Criterion (ABIC) to quantify the marginal likelihood function; furthermore, to adapt this method to data-space inversion, we propose a data-space variant of ABIC, termed DABIC, and the data-space inversion based on DABIC is referred to as D-DABIC inversion method.

For details on the methodology and workflow of the D-DABIC inversion method, please refer to:\
***Song, H., Yu, P., Usui, Y., Uyeshima, M., Diba, D., & Zhang, L. (2025). Three-dimensional Magnetotelluric Inversion based on a Data Space variant of Akaike’s Bayesian Information Criterion. Geophysics, [Volume], [Issue], [Page Range].*** 

For more information about the original FEMTIC code (e.g., forward modeling, mesh design), please refer to the FEMTIC repository: https://github.com/yoshiya-usui/femtic.

## Functional overview
Except for the method used to determine the regularization parameter, all other functionalities of FEMTIC-DABIC are consistent with those of the original FEMTIC. These inherited features include (but are not limited to) 3-D MT forward modeling for various mesh types, classic Gaussian-Newton optimization, and support for various data type.


## Release note
***v1.3*** Sep. 11, 2025: Introduced a reference model (mr) into the inversion optimization workflow, which enables implementing Depth of Investigation (DOI) for model appraisal.

***v1.2*** Dec. 30, 2024: Added support for the Laplacian Filter (LF) in the maximization of the marginal likelihood function.

***v1.1*** Nov. 28, 2024: Basic version of FEMTIC-DABIC.
