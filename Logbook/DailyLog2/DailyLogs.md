# 7321 (September 26, 2011) #

## Plot making ##

* Redo fit result plots with legend and with CMS prelimiary and with better binning and with better minimum
and larger point size
    * <strike>WJet fit</strike>
    * <strike>Top fit</strike>
    * <strike>QCD fit</strike>
    * <strike>Electron overlay plots</strike>
    * <strike>Hadronic overlay plots</strike>
* Plot that shows improvement when we select higher threshold for b-jet counting
* We need new spaghetti plots
* <strike>Legend on the trigger plots larger</strike>
* <strike>Higher statistics for the example 2D plot</strike>
* Check with Alex to see if he has updated trigger plots (?)
* <strike>Add CMS preliminary to the limit plot</strike>
* Maybe obsolete now, but could try to make 2D signal box optimization plot (if there's extra time).
Not a high priority I'll say

## Note ##

* Checking through one round of the note and do updates
    * Chapter 1
    * Chapter 2
    * <strike>Chapter 3<strike>
    * <strike>Chapter 5</strike>
    * Chapter 6
    * Chapter 7
* Update the yield table to new statistics

## Fitting ##

* Start redoing the fits for JES up and down
* Leave the normalization ones for later
* Swap Wjet and ttjet

## Code reading ##

* Re-read and make sure of the algorithm to generate limits - expected limits for now

## Others ##

* Skim events with delta phi around zero
* Skim events in the signal region and start scanning by eye

## Recap of current understanding of the CLs "official tool" --- expected limit ##

* First we build signal and background models as follows
   * Background is constrained to be around the input value with some error
   * Signal yield is written as lumi x efficiency x cross section x extra factor
   * The extra factor is constrained to be centered at 1, with width dictated by input
   * "B" = constrain on background yield
   * "S+B" = constraint on background yield x constraint on signal extra factor x constraint on total yield
   * Each constraint can be Gaussian or log-normal (or some other stuff....) but the script force us
   to use the same for all constraints
* Given a signal cross section hypothesis, make a few distributions
   * p-value distribution, sample drawn from background model, evaluated on background distribution
   * p-value distribution, sample drawn from signal+background model, evaluated on background distribution
   * p-values calculated from likelihood distribution
   * Draw random numbers from the above 2 distributions, and take the ratio
   * For the expected limit, we take median of the ratio distribution and call it _the_ CLs value
   for this signal cross section hypothesis
   * Similarly for +1sigma, -1sigma, etc.
* Collect the CLs value for different signal hypotheses
   * I was reading one-sided CLs limit, so it's finding the 95% point of this curve starting from low
   cross section, with x axis being cross section and y axis CLs value








