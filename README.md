# MilkweedWarming2024

**Authors:** 
Ragonese, Isabella (1,2); Brandon, Christopher (3); Chavez, Joselyne (4); de Roode, Jacobus (5); Hall, Richard (2); Altizer, Sonia (2)  

*Author affiliations*  
(1) University of Massachusetts Amherst
(2) University of Georgia
(3) Colorado State University
(4) Brown University
(5) Emory University  

**See also: Dryad Digital Repository** https://doi.org/10.5061/dryad.prr4xgxx7 

## Overview  
Contained here are datasets describing monarch performance, parasite infection outcomes, and plant traits from a field experiment manipulating milkweed host plant species and temperature. The code used to perform statistical analysis and visualize results is also included.  
Statistical analyses were completed in R (version 4.4.1). Code was implemented using loaded packages: tidyverse, dplyr, ggplot2, lme4, lubridate, stats, MuMIn, rstatix, MASS, Hmisc, ggpubr, car, DescTools, sjplot, and emmeans  

## Files  
### "MWwarming_2021.Rproj"  
R project that bundles the relevant scripts and data files used for the analysis.  
* Save project file in the same folder as the above data (.csv) files and the markdown (.rmd) files below. Open the project in R Studio and then access the markdown files within the project.

### "MW_warming_Jul_2025.rmd"
Updated version of "MW_warming_Nov_2024.rmd" Data analysis for a 2021 field experiment exploring the effects of elevated temperature, milkweed host plant species, and the interaction between milkweed and temperature on monarch traits and infection. This version contains the most up-to-date figures.
### "MW_warming_Nov_2024.rmd"
Data analysis for a 2021 field experiment exploring the effects of elevated temperature, milkweed host plant species, and the interaction between milkweed and temperature on monarch traits and infection.

#### inputs: 
- temperature data: "per_ibutton_avgtemps_full.csv" ; 
- monarch data: "MWwarming_comp_May16.csv"
- plant data: "UGA_Cardenolide_Analysis_March2023_tropical.csv"

### "ibutton_temp.rmd"
Mean daily temperature (C) comparsion and repeated ANOVAs for ambient vs. temperature-elevated plots

### "ibutton_humidity.rmd"
Mean daily relative humidity (%) comparison and repeated ANOVAs for ambient vs. temperature-elevated plots


### "UGA_Cardenolide_Analysis_March2023_tropical.csv"
Description: This file contains the cardenolide toxin measures for the subset of tropical milkweeds sampled from the field  

### "AverageAmbient_TEMP2.csv"
Description: Temperature (C) reading for each of the ibuttons in ambient plots in all timesteps across the experiment. Calculated mean and standard deviation of temperature for each timestep. (Date/Time is the exact value from ibutton H1; other ibuttons recorded temperature within 10 minutes of H1)  

### "AverageAmbient_RelHum.csv"  
Description: Relative Humidity (%) reading for each of the ibuttons in ambient plots in all timesteps across the experiment. Calculated mean and standard deviation of RH for each timestep. (Date/Time is the exact value from ibutton H1)

### "AverageElevated_RelHum.csv"  
Description: Relative Humidity (%) reading for each of the ibuttons in elevated temperature plots in all timesteps across the experiment. Calculated mean and standard deviation of RH for each timestep. (Date/Time is the exact value from ibutton H2)  

### "AverageElevated_TEMP.csv"  
Description: Temperature (C) reading for each of the ibuttons in elevated temperature plots in all timesteps across the experiment. Calculated mean and standard deviation of temperature for each timestep. (Date/Time is the exact value from ibutton H2; , other ibuttons recorded within 10 minutes of H2)  

### "per_ibutton_avgtemps_full.csv"  
Description: Mean, standard deviation, and standard error of recorded temperatures for each ibutton  

### "MWwarming_comp_May16.csv"  
Description: Comprehensive data table with monarch performance and infection metrics in addition to plant measures for the subset of milkweed plants sampled  

*Variables*  
ID: unique identification number for each monarch  
Plant_ID: unique identification number for each host plant  
Temp: ambient or elevated  
OE_treatment: infected or uninfected control  
Milkweed: tropical or swamp  
Lineage: monarch genetic lineage (A, B, C or E)  
Strain: parasite genetic strain (WV1 or E6) or C for control  
PlotNum: number representing physical location in the field plot  
ibutton: unique name of ibutton data logger  
Surv_pupa: survival to pupation (1/0) 1=yes, 0=no  
Surv_adult: survival to adult (1/0) 1=yes, 0=no  
PupalMass: mass of pupa (g); "NA" if monarch died prior to pupal stage  
Date_inoculated: date larva fed inoculum or sham  
Date_into_pint: date pupa removed from field and placed in individual pint container  
PupalScore: For all inoculated monarchs, pupae were scored on a 0-5 scale for signs of OE infection (level of black spotting); "NA" = not applicable (monarch was dead or in the control group, and therefore not assessed); "missed" = monarch eclosed before scoring  
Date_PupScore: date pupa was scored for OE; "NA" if monarch died prior  
Eclosion_Date: date adult monarch emerged; "NA" if monarch died prior  
Sex: M or F (determined at adult stage); "NA" if monarch died prior  
OE_tape_score: for uninoculated control monarchs, we checked for OE contamination by pressing clear plastic tape to adult abdomens and checking for OE under the microscope. We also checked inoculated monarchs with low pupal scores, scoring them on a scale from 0-5. "NA" if not sampled  
InfectionStatus: binary presences/absence of OE (1/0); 1=yes, 0=no  
Death_date: date adult monarch died; "NA" if monarch died prior to adult stage  
Notes: including observations on stage/cause of death, empty cell if nothing was noted  
Inoc_to_pupa: time in days from inoculation to pupa (averaged for the two caterpillars on each plant if they pupated on different days);  "NA" if monarch died prior to pupation  
AdultLongevity: days monarchs survived in the adult stage at 12C;  "NA" if monarch died prior to adult stage  
AvgOE_corner: average number of OE spores in one grid square of hemocytometer (used in infection intensity calculation), not applicable ("NA") for control monarchs or those that died prior to the adult stage  
OE_5ml: Spore load (calculated number of spores per monarch based on "AvgOE_corner")  
LogOE: Log10 transformation~ ~of "OE_5ml"  
ForewingLength.mm.: length of forewing measured with calipers (mm); "NA" if monarch died prior to adult stage  
CtoN: Carbon to Nitrogen ratio of the host plant (only forthe subset of sampled plants; "NA" if not)  
CtoN_Jul: Carbon to Nitrogen ratio of plants (only if resampled at end of experiment; "NA" if not)  

