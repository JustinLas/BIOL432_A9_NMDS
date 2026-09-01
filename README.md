# BIOL 432 — Assignment 9: Floristic Survey and NMDS

This is my Assignment 9 work for **BIOL 432: Computation and Big Data in Biology** at Queen's University.

## What I did

For this assignment I looked at plant communities inside and outside garlic mustard plots. I used NMDS to visualize community composition and species richness to compare the number of species at each site.

I also used a two-way ANOVA to look at the effects of Location and Population on the first NMDS axis.

## Main methods

- R
- `vegan`
- Bray-Curtis distance
- NMDS using `metaMDS()`
- Two-way ANOVA
- Species richness

## Files

- `A9_Lasrado_20283881.Rmd` — main analysis
- `FloristicSurvey.csv` — data used in the analysis

## Results

The Inside and Outside sites were mixed in the NMDS plot, with no clear separation between the two locations. Location was also not significant in the ANOVA (F = 0.35, p = 0.562), while Population had a strong effect (F = 49.59, p = 1.43e-07).

The analysis suggests that differences between populations were much larger than differences associated with the presence or absence of garlic mustard in this dataset.

## Note on the analysis

The original analysis used an ANOVA on NMDS1. Since NMDS represents multivariate community data, PERMANOVA would be a more direct way to test overall community-composition differences. The ANOVA is kept here because it matches the original course analysis.

## Running the analysis

Open the R Markdown file in RStudio and make sure `FloristicSurvey.csv` is in the same folder. The required package is `vegan`.
