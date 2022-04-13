
<!-- README.md is generated from README.Rmd. Please edit that file -->

# modds

<!-- badges: start -->
<!-- badges: end -->

An example showcasing modern data science tools in R.

## Pipeline

``` r
tar_target(raw_data, airquality)
#> Establish _targets.R and _targets_r/targets/raw-data.R.
```

``` r
tar_target(response_data, clean_raw_data(raw_data))
#> Establish _targets.R and _targets_r/targets/response-data.R.
```

``` r
cat(c("```mermaid", tar_mermaid(), "```"), sep = "\n")
```

``` mermaid
graph LR
  subgraph Legend
    outdated([Outdated]):::outdated --- stem([Stem]):::none
  end
  subgraph Graph
    raw_data([raw_data]):::outdated --> response_data([response_data]):::outdated
  end
  classDef outdated stroke:#000000,color:#000000,fill:#78B7C5;
  classDef none stroke:#000000,color:#000000,fill:#94a4ac;
  linkStyle 0 stroke-width:0px;
```
