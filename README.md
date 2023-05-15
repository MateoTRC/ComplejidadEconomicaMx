# Economic complexity of Mexico

We developed a complex systems-based analysis of the economic activities of the 32 states of Mexico. The methodology we applied is based on the work of Hidalgo et. al. The product space conditions the development of nations [1].
 
 # Methodology
 
 Once we have the values of proximity and $RCA$ for each product in every state stored in the Excel file of each folder, we use the notebook `Read_data_and_compute_metrics` to compute the density of each product in every state. The density is defined as follows:
 
$$\omega^k_j=\frac{\sum_i x_i\phi_{ij}}{\sum_i\phi_{ij}}$$

where $\omega^k_j$ is the density around good $j$ given the export basket of the $k$-th country and $x_i = 1$ if $RCA_{ki} > 1$ and 0 otherwise. 

Then, using the `Statistics` notebook, we compute the probability distribution of the density of the products separated into two groups: those that developed $RCA$ in the specific period of time and those that remain underdeveloped, for each one of the states. To quantify the influence of density in the product's development, we compute the P-value of the distributions with the ANOVA and the Kurskal test. We observed that for most of the states, the P-value test neglected the null-hypothesis, meaning that the density can be a factor of development for the products.

As output of this analysis, we obtain a `.csv` file with the name of the states where the test failed (for each kind of testing). This allows us to classify the states into those where density is a decisive factor of product development and those where development occurred in a more random way. These files are stored in the `ANOVA_flag_1` and the `Kurskal_flag_1` folders, respectively.

 
[1] Hidalgo, C. A., Klinger, B., Barabási, A. L., & Hausmann, R. (2007). The product space conditions the development of nations. Science, 317(5837), 482-487.
