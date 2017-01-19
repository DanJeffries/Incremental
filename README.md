

## Incremental 

<b>A program for incrementally testing Stacks parameters</b>


### Modules

Incremental_U - This module currently allows you to test the -M, -m and --max_stacks_per_locus flags in the "Ustacks" module of stacks. 

Incremental_C - This module currently allows you to test the -n and -m flags in the "Cstacks" module of stacks. 

Incremental_Pop - This module currently allows you to test the -p and -r flags in the "Populations" module of stacks. 



### The workflow

The workflows for each module are essentially the same (and very simple):

1. Takes as input, file or directory paths to the input for that module and the parameter values for the parameters to test.
2. The module will then constuct and execute Stacks commands.
3. The module parses various Stacks outputs and creates informative plots for the user.

The plots for each module should give the user an idea of how their data behaves in response to which parameters, and should allow them to make informed decisions on parameter values for their final analyses.

NOTE*** Due to the computation time required for Stacks analyses, this pipeline is intended for use with representative subsets on the order of 5-20 samples from each dataset. Any more than this and the time it takes to analyse each sample at each parameter at each parameter value becomes prohibitive. 


### Implementation

At the moment, the program exists as 3 separate python modules, with can be imported into python as usual. 

Cline versions under construction . . . . 

### DEPENDENCIES

1. Stacks - http://catchenlab.life.illinois.edu/stacks/ 
2. pyVCF - (Can be installed from command line with pip)
3. python 2.7

### Elite team of kick-ass developers

Dr. Daniel Jeffries - daniellee.jeffries@unil.ch  
Dr. Robert Lehmann - ...



