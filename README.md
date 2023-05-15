# Economic complexity of Mexico
 We develope a complex systems-based analysis of the economic activities of the 32 states of Mexico. The methodology we applied is based on the work of Hidalgo et. al. The product space conditions the development of nations [1].
 
 # Methodology
 
 Once we have the values of proximity and $RCA$ for each product in every state stored in the excel file of each folder, with the notebook `Read_data_and_compute_metrics` we compute the density of each product in every state, wich is defined as
 
$$\omega^k_j=\frac{\sum_i x_i\phi_{ij}}{\sum_i\phi_{ij}}$$

where $\omega^k_j$ is the density around good $j$ given the export basket of the $k$th country and $x_i = 1$ if $RCA_{ki} > 1$ and 0 otherwise. 

Then, with the `Statistics` notebook, we compute the probability dirtribution of the density of the products separated in two groups, those that developed $RCA$ in the specific period of time and those that remain underdeveloped, for each one of the states. To quantify the influence of density in the products developement, we compute the P-value of the distributions. We observed that for most of the states the P-value test neglect the null-hypothesis, meaning that the density can be a factor of developement.
 
 
 
[1] Hidalgo, C. A., Klinger, B., Barabási, A. L., & Hausmann, R. (2007). The product space conditions the development of nations. Science, 317(5837), 482-487.
