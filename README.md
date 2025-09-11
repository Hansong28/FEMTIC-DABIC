# FEMTIC-DABIC
FEMTIC-DABIC is a 3-D magnetotelluric (MT) inversion code developed based on FEMTIC (v4.2).

FEMTIC-DABIC employs the Brent line search algorithm in each iteration to identify the statistically optimal regularization parameter (*α*), which maximizes the marginal likelihood function—itself a function of *α*.\
To quantify the magnitude of this marginal likelihood function, the Akaike’s Bayesian Information Criterion (ABIC) is used as a metric. Furthermore, to adapt ABIC for data-space inversion, we propose a data-space variant of ABIC, termed DABIC; the data-space inversion approach based on this DABIC is referred to as the D-DABIC inversion method.

For details on the methodology and workflow of the D-DABIC inversion method, please refer to:\
*Song, H., Yu, P., Usui, Y., Uyeshima, M., Diba, D., & Zhang, L. (2025). Three-dimensional Magnetotelluric Inversion based on a Data Space variant of Akaike’s Bayesian Information Criterion. Geophysics, [Volume], [Issue], [Page Range].*

For more information about the original FEMTIC code (e.g., forward modeling, mesh design), please refer to the FEMTIC repository: https://github.com/yoshiya-usui/femtic.

## Release note
***v1.3*** Sep. 11, 2025: Introduced a reference model (mr) into the inversion optimization workflow, which enables implementing depth of investigation (DOI) for model appraisal.

***v1.2*** Dec. 30, 2024: Added support for the Laplacian Filter (LF) in the maximization of the marginal likelihood function.

***v1.1*** Nov. 28, 2024: Basic version of FEMTIC-DABIC.
