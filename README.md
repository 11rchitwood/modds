
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
tar_mermaid()
#>  [1] "graph LR"                                                                         
#>  [2] "  subgraph Legend"                                                                
#>  [3] "    outdated([Outdated]):::outdated --- stem([Stem]):::none"                      
#>  [4] "  end"                                                                            
#>  [5] "  subgraph Graph"                                                                 
#>  [6] "    raw_data([raw_data]):::outdated --> response_data([response_data]):::outdated"
#>  [7] "  end"                                                                            
#>  [8] "  classDef outdated stroke:#000000,color:#000000,fill:#78B7C5;"                   
#>  [9] "  classDef none stroke:#000000,color:#000000,fill:#94a4ac;"                       
#> [10] "  linkStyle 0 stroke-width:0px;"
```
