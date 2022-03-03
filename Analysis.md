Report on CS Freshmen in 202110 to 202120
================
Akhil Kadarla
3/2/2022

This report is to show how many students continued to be freshmen in
fall of 2021 to spring of 2022 and predict how many did we loose as CS
major. Data of the freshmen in fall of 2021 and spring of 2022 has been
used for this project.

**Data of freshmen in Fall of 2021(202110):**

``` r
library("readxl")
Data202110FR<-read_excel('Data202110FR.xlsx')
Data202110FR
```

    ## # A tibble: 170 x 24
    ##         ID NAME   LEVEL CLASS `ACAD STDG` `COLL 1` `DEGC CODE` `MAJR 1` `MINR 1`
    ##      <dbl> <chr>  <chr> <chr> <chr>       <chr>    <chr>       <chr>    <chr>   
    ##  1 1201471 ABTAH~ UG    FR    11          SC       ID          CS       <NA>    
    ##  2 1111068 ADAM,~ UG    FR    11          SC       ID          CS       <NA>    
    ##  3 1212177 ADESU~ UG    FR    11          SC       ID          CS       <NA>    
    ##  4 1212973 AGUIR~ UG    FR    21          SC       ID          CS       <NA>    
    ##  5 1204765 AKEL,~ UG    FR    11          SC       ID          CS       <NA>    
    ##  6 1208740 ALHAS~ UG    FR    11          SC       ID          CS       <NA>    
    ##  7 1163364 AQUIN~ UG    FR    21          SC       ID          CS       <NA>    
    ##  8 1209542 ARMST~ UG    FR    11          SC       ID          CS       <NA>    
    ##  9 1205416 BAAH,~ UG    FR    21          SC       ID          CS       <NA>    
    ## 10 1181554 BALIS~ UG    FR    31          SC       ID          CS       <NA>    
    ## # ... with 160 more rows, and 15 more variables: MINR 2 <lgl>, EMAIL <chr>,
    ## #   INST HRS <dbl>, TRANSFER HRS <dbl>, TERM HRS <dbl>, OVERALL GPA <dbl>,
    ## #   LADDERS <chr>, LEARN COMM <chr>, GRADE FORGV <chr>, MAJR 1 CONC 1 <lgl>,
    ## #   COLL 2 <lgl>, SC MAJR 1 <lgl>, SC MINR 1 <lgl>, Year <dbl>, Exist <lgl>

There are 170 Freshmen who joined as CS majors in the Fall of
2021(202110).

**Data of freshmen in Spring of 2021(202120):**

``` r
library("readxl")
Data202120FR<-read_excel('Data202120FR.xlsx')
Data202120FR
```

    ## # A tibble: 149 x 23
    ##         ID NAME   LEVEL CLASS `ACAD STDG` `COLL 1` `DEGC CODE` `MAJR 1` `MINR 1`
    ##      <dbl> <chr>  <chr> <chr> <lgl>       <chr>    <chr>       <chr>    <chr>   
    ##  1 1201471 ABTAH~ UG    FR    NA          SC       ID          CS       <NA>    
    ##  2 1111068 ADAM,~ UG    FR    NA          SC       ID          CS       <NA>    
    ##  3 1204765 AKEL,~ UG    FR    NA          SC       ID          CS       <NA>    
    ##  4 1208740 ALHAS~ UG    FR    NA          SC       ID          CS       <NA>    
    ##  5 1163364 AQUIN~ UG    FR    NA          SC       ID          CS       <NA>    
    ##  6 1183034 ARAGO~ UG    FR    NA          SC       ID          CS       <NA>    
    ##  7 1209542 ARMST~ UG    FR    NA          SC       ID          CS       <NA>    
    ##  8 1217826 ATKIN~ UG    FR    NA          SC       ID          CS       <NA>    
    ##  9 1181554 BALIS~ UG    FR    NA          SC       ID          CS       <NA>    
    ## 10 1211192 BARRE~ UG    FR    NA          SC       BSCS        CS       <NA>    
    ## # ... with 139 more rows, and 14 more variables: MINR 2 <lgl>, EMAIL <chr>,
    ## #   INST HRS <dbl>, TRANSFER HRS <dbl>, TERM HRS <dbl>, OVERALL GPA <dbl>,
    ## #   LADDERS <chr>, LEARN COMM <chr>, GRADE FORGV <chr>, MAJR 1 CONC 1 <lgl>,
    ## #   COLL 2 <lgl>, SC MAJR 1 <lgl>, SC MINR 1 <lgl>, Year <dbl>

There are 149 Freshmen who joined as CS majors in the spring of
2021(202120).

**Data of students who continued as freshmen from 202110 to 202120:**

``` r
library("readxl")
Freshmen2021_22<-read_excel('Freshmen2021-22.xlsx')
Freshmen2021_22
```

    ## # A tibble: 119 x 24
    ##         ID NAME   LEVEL CLASS `ACAD STDG` `COLL 1` `DEGC CODE` `MAJR 1` `MINR 1`
    ##      <dbl> <chr>  <chr> <chr> <chr>       <chr>    <chr>       <chr>    <chr>   
    ##  1 1201471 ABTAH~ UG    FR    11          SC       ID          CS       <NA>    
    ##  2 1111068 ADAM,~ UG    FR    11          SC       ID          CS       <NA>    
    ##  3 1204765 AKEL,~ UG    FR    11          SC       ID          CS       <NA>    
    ##  4 1208740 ALHAS~ UG    FR    11          SC       ID          CS       <NA>    
    ##  5 1163364 AQUIN~ UG    FR    21          SC       ID          CS       <NA>    
    ##  6 1209542 ARMST~ UG    FR    11          SC       ID          CS       <NA>    
    ##  7 1181554 BALIS~ UG    FR    31          SC       ID          CS       <NA>    
    ##  8 1211192 BARRE~ UG    FR    11          SC       BSCS        CS       <NA>    
    ##  9 1203173 BELAC~ UG    FR    21          SC       ID          CS       <NA>    
    ## 10 1200410 BELIZ~ UG    FR    11          SC       ID          CS       <NA>    
    ## # ... with 109 more rows, and 15 more variables: MINR 2 <lgl>, EMAIL <chr>,
    ## #   INST HRS <dbl>, TRANSFER HRS <dbl>, TERM HRS <dbl>, OVERALL GPA <dbl>,
    ## #   LADDERS <chr>, LEARN COMM <chr>, GRADE FORGV <chr>, MAJR 1 CONC 1 <lgl>,
    ## #   COLL 2 <lgl>, SC MAJR 1 <lgl>, SC MINR 1 <lgl>, Year <dbl>, Exist <lgl>

**Data of students who joined as freshmen 202120:**

``` r
library("readxl")
Freshmen_202120<-read_excel('New_joinings.xlsx')
Freshmen_202120
```

    ## # A tibble: 30 x 24
    ##         ID NAME   LEVEL CLASS `ACAD STDG` `COLL 1` `DEGC CODE` `MAJR 1` `MINR 1`
    ##      <dbl> <chr>  <chr> <chr> <lgl>       <chr>    <chr>       <chr>    <lgl>   
    ##  1 1183034 ARAGO~ UG    FR    NA          SC       ID          CS       NA      
    ##  2 1217826 ATKIN~ UG    FR    NA          SC       ID          CS       NA      
    ##  3 1208333 BERHA~ UG    FR    NA          SC       ID          CS       NA      
    ##  4 1193044 BIGSB~ UG    FR    NA          SC       ID          CS       NA      
    ##  5 1196762 BROWN~ UG    FR    NA          SC       ID          CS       NA      
    ##  6 1166856 CAMPB~ UG    FR    NA          SC       ID          CS       NA      
    ##  7 1226804 FUENT~ UG    FR    NA          SC       BSCS        CS       NA      
    ##  8 1216465 GAMBL~ UG    FR    NA          SC       ID          CS       NA      
    ##  9 1214398 GLEAS~ UG    FR    NA          SC       BSCS        CS       NA      
    ## 10 1176833 HARRI~ UG    FR    NA          SC       ID          CS       NA      
    ## # ... with 20 more rows, and 15 more variables: MINR 2 <lgl>, EMAIL <chr>,
    ## #   INST HRS <dbl>, TRANSFER HRS <dbl>, TERM HRS <dbl>, OVERALL GPA <dbl>,
    ## #   LADDERS <chr>, LEARN COMM <chr>, GRADE FORGV <chr>, MAJR 1 CONC 1 <lgl>,
    ## #   COLL 2 <lgl>, SC MAJR 1 <lgl>, SC MINR 1 <lgl>, Year <dbl>, Exist <lgl>

Above is the list of students who continued as freshmen to the next
semester.

From the data , we can see that there were 170 students as freshmen in
the fall of 2021 and 149 students students as freshmen in the spring of
2021. 30 joined as freshman in Spring of 2021. 119 continued to as
freshmen from fall 2021 to spring 2021. There is a difference of 51
students when compared.This could be either the students have changed
their major or left the university.

**Note**: A cross check has been done by comparing the data of freshmen
in 202110 with the sophomores in 202120 to check if the students have
moved to a higher class. The list of freshmen in 202110 and list of
sophomores in 202120 are included in the repository for reference.
