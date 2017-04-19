

## Incremental 

<b>A program for incrementally testing Stacks parameters</b>

Restriction site Associated DNA sequencing (RADseq) has taken the world of molecular ecology by storm! It has allowed biologists to obtain hugely powerful datasets of genome-wide molecular markers for organisms with no pre-existing molecular resources. 

However, the analysis of RADseq data is not trivial, and is highly parameterised, with many factors to consider in order to get the best out of the data, without introducing systematic errors. Unfortunately we have not yet developed the ability to predict the future, as such, many preliminary trials are needed to inform the optimal choice of parameter values for RADseq analyses. But such tests require a lot of time and manual work.

Enter <b>Incremental</b>, a set of python scripts which make these preliminary tests easy and informative. Simply provide incremental with a test set of RADseq data, some parameter values to test, and it will bestow upon you a set of publication-ready plots which will allow you to make informed decisions on the optimal parameters for your final analyses.

So . . . how does incremental work . . . 

### The Modules

Incremental is made up of 3 modules, which reflect the major modules of Stacks.

<b>Incremental_U</b> - This module currently allows you to test the -M, -m and --max_stacks_per_locus flags in the "Ustacks" module of stacks. 

<b>Incremental_C</b> - This module currently allows you to test the -n and -m flags in the "Cstacks" module of stacks. 

<b>Incremental_Pop</b> - This module currently allows you to test the -p and -r flags in the "Populations" module of stack. 



### The workflow

The workflows for each module are essentially the same (and very simple):

1. Takes as input, file or directory paths required for the Stacks module and the parameter values for the parameters to be tested.
2. The module will then constuct and execute Stacks commands, saving commands and log files.
3. The module parses various Stacks outputs and creates informative plots for the user.

The plots for each module should give the user an idea of how their data behaves in response to which parameters, and should allow them to make informed decisions on parameter values for their final analyses.

NOTE*** Due to the computation time required for Stacks analyses, this pipeline is intended for use with representative subsets on the order of 5-20 samples from each dataset. Any more than this and the time it takes to analyse each sample at each parameter at each parameter value becomes prohibitive. 


### Implementation

At the moment, the program exists as 3 separate python modules, with can be imported into python as usual. 

Cline versions may follw . . . . 

### DEPENDENCIES

1. Stacks - http://catchenlab.life.illinois.edu/stacks/ 
2. pyVCF - (Can be installed from command line with pip)
3. python 2.7

### Contact

Dr. Daniel Jeffries - daniellee.jeffries@unil.ch  




