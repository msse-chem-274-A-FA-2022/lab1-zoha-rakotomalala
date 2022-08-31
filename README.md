# Chem 274A - Lab 1

In this lab, you will be using the molecular simulation code we wrote in Chem 280 - Foundations of Molecular Modelling and Software Engineering.

## Exercises

### Section 1 - Makefile (Spend 30 minutes max on this)
1. Use the `makefile` to create an environment for this lab.
    ```
    cd mcsim_python
    make environment
    ```
2. Activate the environment created by the `makefile`
    ```
    conda activate chem274A_lab1
    ```
3. Use the `makefile` to install `mcsim`
    ```
    make install
    ```

4. Review the Makefile in `mcsim_python`. Write a comment above each target explaining what the target does.

### Section 2 - Runnning Simulations
1. Use the notebook `run_mcsim.ipynb` to run Monte Carlo simulations. Follow the instructions in the notebook.

#### Zoha's Answers to the Notebook's instructions

1. The energy per particle graph stabilizes around the 10 000's step, from a high energy per particle to 0 afterwards, which is steady.
I think the RDF graph shows that our material is a gas.

3. With the second type of parameters, as we have less steps and a lesser frequency, we have a less smooth graph of the evolution of the energy per particles by the number of steps. The movement is quite similar, as in both cases we do have a strong decrease toward 0, but here we actually see that it happens in steps. It seems that there are some plateaus before reaching a stable level, but nothing says we did finish the process, or if we ended up at blocked at still a non-negligeable level of energy by step 1000.

For the RDF graph, the graph does not look really good. The first issue is the closeness of particles, especially if I am right about it being a gas. I am not so versed in that subject, but if I remember well, particles can not enter one another, so they have to have some distance between them.

4. In this simulation we are in a similar situation to simulation 1, but the RDF graph is very different. First, the peak is happens much earlier and is very narrow. Then the rest of the curve is more in a 'sawtooth' form we would say in French, instead of the ample curves we first had. I think that if the gas is less dense, the chance to find another particle at a given distance is lower (which is confirmed by the graph), and I guess that it may be kind of random after a certain distance, but still low, which may explain the 'sawtooth' form.

5. (I kept the parameters of situation 4, with a density of 0.009) If we increase the temperature, there is not a steep increase but it does not form a peak that comes back to it's original point. Instead the pattern incrementally decreases and stabilizes itself at the same level as in step 4, with a very similar pattern as well. If I remember well, an increase in temperature means particles start moving more and take more space, but given the low density, it may not translate so obviously in this case, but I also tried with the first parameters and I have a similar result. I may be wrong I think, but I thought it would still be interesting to share.