# 7321 (September 26, 2011) #

## Plot making ##

* Redo fit result plots with legend and with CMS prelimiary and with better binning and with better minimum
and larger point size
    * <strike>WJet fit</strike>
    * <strike>Top fit</strike>
    * <strike>QCD fit</strike>
    * <strike>Electron overlay plots</strike>
    * <strike>Hadronic overlay plots</strike>
* <strike>Plot that shows improvement when we select higher threshold for b-jet counting</strike>
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

* <strike>Re-read and make sure of the algorithm to generate limits - expected limits for now</strike>

## Others ##

* Skim events with delta phi around zero
* Skim events in the signal region and start scanning by eye

## Recap of current understanding of the CLs "official tool" ##

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
    * I was reading one-sided CLs limit, so it's finding the 1-95% point of this curve starting in the high
    cross section part, with x axis being cross section and y axis CLs value
* For observed limit I think it is evaluating the CLs number for the "data" for different cross section
hypothesis, and then on the cross section-CLs graph find the 1-C.L. point



# 7322 (September 27, 2011) #

## Todo's left over from before ##

* Redo the fits with systematic uncertainties
    * Mix in JER uncertainty while doing the JES fit
* <strike>Make the new yield table</strike>
* Swap top and W in the background estimation process
* <strike>Better spaghetti plots</strike>
* Read through note again and again and again and again and again

## Limit rebuilding ##

* Do a few toy studies to learn about properties of the CLs
    * Background-only model seems to do fine
    * S+B is taking a very long time - which I have no idea why
* Build similar S+B and B models in RooFit compared to the official code

## New todo's to potentially improve stuff ##

* Make data/MC comparisons for tight tag
* Same comparison with cut on delta phi
* Get the runs with negative numbers, make comparison excluding those runs



# 7323 (September 28, 2011) #

## Todo's left over from before ##

* Finish running on the missing 3 runs (totalling 169 /pb)
    * Having problems....
* <strike>Make comparisons excluding the three runs</strike>
    * The noise peak is still there in the R distribution....
    * No good
* Start fixing texts in the analysis note
* Prevent people from looking at this private logbook
* How do things look when we add in a delta phi cut?
    * Similar....  well we don't really cut out that many

## Notes on relaxing R2 0.5 cut and adding delta phi cut ##

* Not much has chnaged
* Redid the main fits
    * Electron box result looks suspicious
    * Hadronic ones are fine
* Discovered a bug in the event cleaning list
    * electron and muon ones are not cleaned, unfortunately
    * Made a new list for Artur to run on
* Limit seems to be improved by quite a bit



# 7324 (September 29, 2011) #

## Miscellaneous list ##

* Start implementing systematic uncertainties
* Realized that the normalization-type ones are not needed.  Fewer fits to do!



# 7341 (October 10, 2011) #

## Action items until the end of next week ##

* Upgrade PAS and analysis note
* Fix electron ID and re-make simulation files
* Request more official samples (for different mass points)
* Book tickets to Rome and Paris (and place to stay, etc.)
* Explain difference between data/simulation
* Try to fit to get PDF from electrons, then apply to muon dataset
* Check if all data is used
* Re-interpret limit with non-100-percent branching fraction
* Bias from jet/MET type












