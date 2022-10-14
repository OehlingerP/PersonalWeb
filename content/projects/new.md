---
title: "My Project"
date: 2022-09-01T10:17:19+08:00
draft: false
cover: "https://d33wubrfki0l68.cloudfront.net/698bdaa040744ec373f18fc5f1811f709883d686/bb0c0/themes/hugo-theme-onelou/screenshot_hu2ad82ecd1b89cace345447ca44b2b73d_21459_750x500_fill_catmullrom_top_3.png"
---

# Idea

Following the *KISS* principle of modeling I start with the simplest
model possible to investigate shock amplifications in the global trade
network. The question is how shocks at the micro/sector level may
trigger major global economic shocks.

## Supply Chain 1

    ## Loading required package: dplyr

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

    ## Loading required package: extrafont

    ## Registering fonts with R

    ## Loading required package: ggplot2

    ## Loading required package: igraph

    ## 
    ## Attaching package: 'igraph'

    ## The following objects are masked from 'package:dplyr':
    ## 
    ##     as_data_frame, groups, union

    ## The following objects are masked from 'package:stats':
    ## 
    ##     decompose, spectrum

    ## The following object is masked from 'package:base':
    ## 
    ##     union

    ## Loading required package: lubridate

    ## 
    ## Attaching package: 'lubridate'

    ## The following objects are masked from 'package:igraph':
    ## 
    ##     %--%, union

    ## The following objects are masked from 'package:base':
    ## 
    ##     date, intersect, setdiff, union

    ## Loading required package: officer

    ## Loading required package: openxlsx

    ## Loading required package: rvg

    ## Loading required package: tidyr

    ## 
    ## Attaching package: 'tidyr'

    ## The following object is masked from 'package:igraph':
    ## 
    ##     crossing

    ## 
    ## Attaching package: 'Rphd'

    ## The following object is masked from 'package:dplyr':
    ## 
    ##     collapse

![Simple one good two country economy. A 10% percent shock in China will
lead to a 10% reduction of output in the U.S. Thus, there is no shock
amplification.](new_files/figure-markdown_strict/supply-chain1-1.png)

Let’s start with the simplest trade model possible and look at a world
with only one good and two countries, let’s say China and the United
States, where China is the supplier of raw materials and the U.S. uses
these materials to produce consumption goods for U.S. citizens. In this
model (see figure ), shocks evolve linear (no amplification) and affect
each country equally.

## Supply Chain 2

If we add a second good to the economy (see figure ), things may change.
Let’s say the U.S. needs 75 of good 1 and 25 of good 2 to produce 100 of
good 3. Assume another 10% shock hits the Chinese economy, however, the
crisis only affects good 2. Hence, output of good 2 drops from 25 to 15.
While the total shock for China is still 10%, things changed
considerably for the United States as output drops by 40% (10/25 = 40%).

![Simple two good two country economy. A 10% percent shock in China’s
good 1 sector will lead to a larger reduction of output in the U.S.
depending on the production input ratio. Thus, there is an amplification
of the shock.](new_files/figure-markdown_strict/supply-chain2-1.png)

## Supply Chain 3

*Supply chain 2* is a simple example of how sector-specific shocks in
one country may amplify. What we also see is that countries at the end
of the supply chain are more vulnerable than countries at the beginning
as they depend on many more countries. To see this we do one more simple
example of probability of default. Let’s assume at each link in figure
has a probability of default of 5%. This results in the following
default probabilities: India = 5%, France
 → 1 − 0.95<sup>2</sup> = 9.8%, and the U.S.
 → 1 − 0.95<sup>3</sup> = 14.3%.

![Simple 4-player supply chain. The default probability grows with each
link in the network. Thus, producers at the end of the supply chain face
higher risks.](new_files/figure-markdown_strict/supply-chain3-1.png)

## Conclusion and what is missing

-   Shocks may amplify depending on which industries and countries are
    affected.
-   Later stages of the supply chain bear higher risks.
-   If available, good 2 can be sourced from other suppliers, hence, the
    shock would be dampened. Prices might go up.
-   A shock can be (temporarily) mitigated by domestic stocks.
-   There will be repercussions. If the U.S. experiences a dramatic drop
    in economic output industry 2 will also be affected. Hence, the
    shock will also hit China stronger than initially expected.
