Final project for class FANR 8925: Data management and reproducible science.

Author: Kimberly García. email: kpg59882@uga.edu

# Description of the datasets 

The datasets used for this analyses come from a project I participated as young researcher called "Diversidad taxonómica y funcional de grupos selectos de artrópodos Coleoptera y Arachnida) 
en fragmentos de Bosque Seco Tropical en el Caribe colombiano”" Associated to the research program “70531 - Diversidad genética, taxonómica y funcional 
y algunos aspectos poblacionales de grupos taxonómicos con importancia para la conservación del bosque seco tropical en los Montes de María y la serranía de 
Piojo en el Caribe colombiano” of the 852-2019 CONVOCATORIA DE PROGRAMAS CONECTANDO CONOCIMIENTO 2019 funded by Minciencias (Colombia). This data is in process of publication.

We sampled during 4 months in 4 plots located in five localities in the Caribbean of Colombia, which are as follows: 

RM: Reserva la Montaña (Atlántico);
SC: Santa Catalina (Atlántico);
LR: Los Rosales (Atlántico);
SFFC: Santuario de Flora y Fauna los Colorados (Bolívar);
RLF: Reserva La Flecha (Bolívar).

Additionally, in the SFFC we compared between two different types of habitat, forest and a recovering buffer zone. 

The data represents Cerambycidae beetles collected in five fragments of Tropical Dry Forest. The specimens were collected with a variety of sampling traps, including: light traps, 
fruit-baited traps, and entomological beating sheet. 

The identification of the specimens was made by Kimberly García and Lady Montes, with the help of the reference collection at the Universidad del Atlántico (Colombia)
and Museu de Zoologia da Universidade de Sao Paulo (Brazil). Experts were also consulted to confirm identification.   

#Files and variables

## File: data/raw/Final_project.csv

## Variables

* X: Locality, it includes month of sampling and plot number. Structure example "SFFC M1 P1",SFFC (Santuario de Flora y Fauna los Colorados), 
M1 (Month 1) and P1 (Plot 1). All the localities follow this structure.

* C...insulana: This and the following columns are Cerambycidae species names, with genus and species separated by .., the genus is represented by its first letter. C..insulana 
is Ceragenia insulana. These names are further completed during data cleaning. 

## File: data/raw/Biomass.csv

## Variables

* Species: Species name separating genus and specific epithet by "_"
* Locality: Locality and habitat (buffer zone or forest) where the species was collected, separated by "_". Example: SFFC_buffer_zone
* biomass: Biomass was measured as mean biomass of 10 individuals per species, when possible. The individuals were chosen by 5 males 
and 5 females, considering the greatest variation possible.

## File: data/raw/Subfamilies.csv

## Variables

* Subfamilies: Subfamily of the species. Subfamily assesment was made following the accepted taxonomic names according to Tavakilian & Chevillote (2024).
* Species: Species name separating genus and specific epithet by "_"

# Code/software

All analysis took place in RStudio 2025.09.1 and R version 4.4.2 (2024-10-31 ucrt). Data was compiled in Microsoft excel and saved as .csv.

The code was saved as a Markdown document and an HTML file was knitted to produce the report 

##File: Scripts/R_Final_project.Rmd

This document contains all the codes and files used for this project. It was made on RStudio 2025.09.1 and R version 4.4.2 (2024-10-31 ucrt). The code contains details
about each step and it is structured accordingly. The main purpose of this document was to produce a report, and hence it has both text and code. 
.12.0. All analysis for the manuscript are contained within this file.

##File: Scripts/R_Final_project.html

This document presents the knitted report. It showcases all the plots and tables, along with the output of inline code to describe the results and conclusions. It was
organized to present the data ordered by the headers: Introduction, Data exploration, Data summary, AI disclosure and References. 
It also contains subheaders for organization of the report, separating the analysis of all five localities, and exclusively in SFFC habitats. 

#References
The present readme file was done following the structure presented by Ashe-Jepson et al. (2025) readme file.
The development of this project was done following the topics learned in the class FANR 8925: Data management and Reproducible Science, Fall 2025 by Dr. Claire S Teitelbaum,
and the use of the bookdown available at: https://cteitel.github.io/DataMgmt_book/index.html
All references used in the analyses and conclusions are presented in the report. 